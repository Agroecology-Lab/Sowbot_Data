# Sowbot ↔ RTU v4 MAVLink Bridge — Architecture

## Overview

```
Sowbot stack (Nav2, TSM row-following, F2C)
        │
        ▼  cmd_vel (Twist)
devkit_mavlink_bridge
        │
        ├──▶  SET_POSITION_TARGET_LOCAL_NED  ──▶  RTU Master Controller
        │                                          (ArduPilot Rover, GUIDED mode, armed)
        │
        ▲
        │  GPS_INPUT
        │
Sowbot's dual F9P + BNO085 → FusionCore EKF
```

## Outbound: navigation → motors

Nav2 / TSM / F2C produce `cmd_vel` as usual. `devkit_mavlink_bridge` subscribes to `cmd_vel` and republishes it to the RTU as `SET_POSITION_TARGET_LOCAL_NED` over MAVLink. The RTU's Master Controller runs ArduPilot Rover firmware and only acts on this while armed and in GUIDED mode.

## Inbound: localisation

Sowbot's existing localisation stack — dual F9P RTK GNSS, BNO085 IMU, FusionCore UKF — runs unchanged. The bridge takes FusionCore's fused pose output and sends it to the RTU as `GPS_INPUT`, feeding the RTU's own onboard EKF. The RTU navigates on Sowbot's fix; its onboard RTK2 receiver is not used for this purpose.

## Bridge node responsibilities

| Direction | ROS side | MAVLink message |
|---|---|---|
| Out | `cmd_vel` (Twist) | `SET_POSITION_TARGET_LOCAL_NED` |
| In | FusionCore fused pose | `GPS_INPUT` |
| In (optional, monitoring only) | — | `HEARTBEAT`, battery/estop status |

No wheel-odometry topic (`/odom`, `/odom/wheels`) is required by this design.

## Confirmed from ArduPilot Rover source (`GCS_MAVLink_Rover.cpp`, `mode_guided.cpp`, `AP_GPS_MAV.cpp`)

**`SET_POSITION_TARGET_LOCAL_NED` — exact fields the bridge must set for a differential-drive `cmd_vel`:**
- `type_mask`: POS_IGNORE and ACC_IGNORE bits **must** be set — if ACC_IGNORE is not set, ArduPilot rejects the whole message and takes no action (confirmed at the handler's `acc_ignore` check). VEL_IGNORE and YAW_RATE_IGNORE bits must be **clear**; YAW_IGNORE set.
- `vx` = `cmd_vel.linear.x`, `vy` = 0, `yaw_rate` = `cmd_vel.angular.z`.
- This exact combination (`vel` present, `yaw` ignored, `yaw_rate` present) is the only branch that maps directly onto differential/skid-steer `cmd_vel` — it calls `set_desired_turn_rate_and_speed()`. Other field combinations map to heading-hold or heading-only control, not what Sowbot needs.
- The handler **no-ops silently** (returns with no error) if the vehicle isn't in GUIDED mode, or if `AHRS` has no EKF origin yet — so a valid EKF origin (which requires at least one accepted GPS fix, i.e. `GPS_INPUT` must have already landed and been accepted) is a precondition for velocity control to do anything at all, not just for position control.
- GUIDED mode has a watchdog: `GUID_TIMEOUT` (default **3.0 s**) — if no new setpoint arrives within that window the rover auto-stops and logs a warning. The bridge must republish at a rate comfortably faster than 3 s, not just on `cmd_vel` change.

**`GPS_INPUT` — exact mechanism:**
- Handled by `AP_GPS_MAV`, ArduPilot's real driver for "GPS data from an external companion computer" (its own description).
- The message includes a `gps_id` field which must match the GPS *instance* the parameter `GPS1_TYPE` (or `GPS2_TYPE`) is set to type `14` (`GPS_TYPE_MAV`) — confirmed enum value in `AP_GPS.h`. Without that parameter set on the RTU, incoming `GPS_INPUT` messages are simply ignored by every other GPS backend.
- This is therefore not just a bridge-code question as previously flagged — it's a **one-time ArduPilot parameter change on the RTU** (`GPS1_TYPE=14`), which also means the RTU's onboard RTK2 receiver would need to sit on the *other* GPS instance (or be disabled) rather than being silently overridden by priority — ArduPilot doesn't automatically prefer one GPS source over another without blending/priority configuration.

## Open items

1. **Physical MAVLink port** on the RTU Master Controller — still not documented in the RTU v4 spec, which only lists RTK2, RC receiver, and the internal 115200 baud link to the traction units. Nothing found so far resolves this; still needs asking Robotriks directly.
2. **FusionCore output rate/format** — needed to fix the `GPS_INPUT` publish rate (and to confirm it can sustain a rate well inside the 3 s `GUID_TIMEOUT` window for the velocity side too).
3. ~~ArduPilot GPS parameter configuration~~ — **resolved above**: set `GPS1_TYPE` (or whichever instance is free) to `14` on the RTU, and either disable the onboard RTK2 or move it to the other instance so the two sources don't collide.
4. **New, from this pass:** need to confirm how EKF origin gets set on first boot when the only GPS source is `GPS_INPUT` — if the RTU has no other GPS to establish origin, the bridge may need to send an initial `GPS_INPUT` burst before GUIDED commands will be accepted at all.
5. **New, from this pass:** `mavros`'s own `setpoint_velocity` plugin may not set the ACC_IGNORE bit the way this integration needs by default — if reusing mavros rather than a bespoke node, its type_mask construction needs checking against the exact branch above, not assumed compatible.
