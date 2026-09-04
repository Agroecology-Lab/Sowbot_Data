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

## Open items

1. **Physical MAVLink port** on the RTU Master Controller — not documented in the RTU v4 spec, which only lists RTK2, RC receiver, and the internal 115200 baud link to the traction units.
2. **FusionCore output rate/format** — needed to fix the `GPS_INPUT` publish rate and message population.
3. **ArduPilot GPS parameter configuration** (e.g. `GPS1_TYPE`) — required to confirm the RTU's EKF actually prioritises `GPS_INPUT` over its onboard RTK2.
