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

Nav2 / TSM / F2C produce `cmd_vel` as usual. `devkit_mavlink_bridge` subscribes to `cmd_vel` and republishes it to the RTU as `SET_POSITION_TARGET_LOCAL_NED` over MAVLink. The RTU's Master Controller runs ArduPilot Rover firmware and only acts on this while armed and in GUIDED mode (mode number 15).

## Inbound: localisation

Sowbot's existing localisation stack — dual F9P RTK GNSS, BNO085 IMU, FusionCore UKF — runs unchanged. The bridge takes FusionCore's fused pose output and sends it to the RTU as `GPS_INPUT`, feeding the RTU's own onboard EKF. The RTU navigates on Sowbot's fix; its onboard RTK2 receiver is not used for this purpose.

## Bridge node responsibilities

| Direction                      | ROS side              | MAVLink message                       |
| ------------------------------- | ---------------------- | --------------------------------------- |
| Out                              | `cmd_vel` (Twist)      | `SET_POSITION_TARGET_LOCAL_NED` (#84) |
| In                               | FusionCore fused pose  | `GPS_INPUT` (#232)                    |
| In (optional, monitoring only)  | —                      | `HEARTBEAT` (#0), `SYS_STATUS` (#1)   |

No wheel-odometry topic (`/odom`, `/odom/wheels`) is required by this design.

## `SET_POSITION_TARGET_LOCAL_NED` — fields for a differential-drive `cmd_vel`

| Field | Value | Notes |
|---|---|---|
| `coordinate_frame` | `MAV_FRAME_BODY_NED` (8) | Makes `vx` = forward, `yaw_rate` = turn rate in the rover's own frame. **Confirmed**: Rover's own [Guided Mode MAVLink docs](https://ardupilot.org/dev/docs/mavlink-rover-commands.html) list frame 8 explicitly for Rover — "Velocity are relative to the vehicle's current heading. Use this to specify the speed forward or backwards." |
| `type_mask` | `1511` (`0x5E7`) | **Confirmed, not 1479.** Rover's docs list this exact value as the named combo "Vel+Yaw Rate" (position ignored, VX/VY used, VZ ignored, acceleration ignored, yaw ignored, yaw_rate used) — i.e. VZ_IGNORE *is* set. 1479 isn't a documented Rover combination; don't use it. |
| `vx` | `cmd_vel.linear.x` | — |
| `vy` | `0` | — |
| `yaw_rate` | `cmd_vel.angular.z` | — |

This field combination (vel present, yaw ignored, yaw_rate present) calls `set_desired_turn_rate_and_speed()` — the only branch that maps onto differential/skid-steer control. Any other combination maps to heading-hold or heading-only control.

**Preconditions (both fail silently, no error message):**
- Vehicle must be in GUIDED mode.
- AHRS must have an EKF origin — requires at least one accepted `GPS_INPUT` fix first. So a valid GPS fix is a precondition for velocity control to do anything at all, not just position control.

**Watchdog:** `GUID_TIMEOUT` (default 3.0 s) — no new setpoint within that window and the rover auto-stops. Bridge must republish comfortably faster than 3 s, not just on `cmd_vel` change.

## `GPS_INPUT` — required configuration

Handled by `AP_GPS_MAV` (ArduPilot's driver for "GPS data from an external companion computer").

- `gps_id` must match a GPS instance whose `GPS1_TYPE` (or `GPS2_TYPE`) parameter is set to `14` (`GPS_TYPE_MAV`). Without that, every other GPS backend ignores incoming `GPS_INPUT`.
- One-time RTU parameter change required: `GPS1_TYPE=14`.
- RTU's onboard RTK2 receiver must sit on the other GPS instance, or be disabled — ArduPilot doesn't auto-prioritise between GPS sources without explicit blending/priority config.

## What needs to happen

1. **Get the physical MAVLink port on the RTU Master Controller.** Not in the RTU v4 spec (which lists only RTK2, RC receiver, and the internal 115200 baud link to the traction units). Ask Robotriks directly.
2. **Pin down FusionCore's output rate and ROS message type.** Needed to set the `GPS_INPUT` publish rate and confirm it comfortably beats the 3 s `GUID_TIMEOUT`. Not yet specified — check the actual FusionCore node before assuming a number or message type.
3. **Confirm EKF origin behaviour on first boot** when `GPS_INPUT` is the RTU's only GPS source. May need the bridge to send an initial `GPS_INPUT` burst before GUIDED commands will be accepted at all.
4. ~~Check `type_mask` against `mode_guided.cpp` directly~~ — **done**. `type_mask=1511`, `coordinate_frame=MAV_FRAME_BODY_NED (8)`, both confirmed against Rover's own MAVLink Guided Mode docs (see table above). `Rover/mode_guided.cpp` on master has a distinct `SubMode::TurnRateAndSpeed` and a 3s no-update auto-stop, consistent with `set_desired_turn_rate_and_speed()` and `GUID_TIMEOUT` as described above — worth a full read of that file once hardware's in hand, but nothing here contradicts the design.
5. **If reusing mavros:** check its `setpoint_velocity` plugin actually sets ACC_IGNORE the way this integration needs — don't assume compatibility.
6. **Set `GPS1_TYPE=14` on the RTU** and move/disable the onboard RTK2 receiver so it doesn't collide with `GPS_INPUT`.
