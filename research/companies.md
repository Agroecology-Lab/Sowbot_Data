# Climate/Crop Robotics Companies — Merged GitHub Summary

## Confirmed GitHub presence

| Company | GitHub | ROS status | Notes |
|---|---|---|---|
| Bonsai Robotics | [github.com/BonsaiRobotics](https://github.com/BonsaiRobotics) | Heavy ROS 2 | Amiga SDK, ROS 2 tooling, DDS middleware work, GNSS drivers, drive-by-wire kit. Genuine engineering org. |
| Avular | [github.com/avular-robotics](https://github.com/avular-robotics) | ROS 2 (SDK level) | Nav2, behaviour trees, perception examples for their Origin and Vertex One robots. |
| Nature Robots | [github.com/naturerobots](https://github.com/naturerobots) | Heavy ROS 1/2 | Maintain `move_base_flex` and `mesh_navigation` (mesh-based terrain nav), plus CANopen drivers. |
| BlueWhite | [github.com/bw-robotics](https://github.com/bw-robotics) | Heavy ROS 1/2 | LiDAR-inertial-visual odometry, sensor calibration, forks of `kiss-icp`/`robot_localization` for tractors. |
| JABAS.AI | [github.com/jabasai](https://github.com/jabasai) | Heavy ROS 2 | Topological nav for crop rows, rosbag tooling, GNSS/LiDAR driver forks. |
| Sabanto | [github.com/sabantoag](https://github.com/sabantoag) | Heavy ROS 1, looks historic | RTK-GPS drivers, coordinate translation, full autonomy/teleop/Gazebo sim for drive-by-wire tractors. |
| Bosch / Bosch Research | [github.com/bosch](https://github.com/bosch), [github.com/boschresearch](https://github.com/boschresearch) | Heavy ROS 1/2 | `boschresearch/usb_cam` is the standard ROS V4L2 camera driver used widely regardless of vendor. |
| CHCNAV (Huace) | [github.com/HuaceNav](https://github.com/HuaceNav) | ROS drivers | Drivers for RTK-GNSS receivers and CGI-610 INS units. |
| Naïo Technologies | [github.com/NaioTechnologies](https://github.com/NaioTechnologies) | Not ROS-native, one stale ROS-adjacent fork | Own proprietary stack (ApiCodec/ApiClient protocol, simulatoz simulator). Only ROS tie is a stale fork of `kacanopen` (a CanOpen-to-ROS bridge). Org looks dormant — last real activity ~2022. |
| Agtonomy | [github.com/agtonomy](https://github.com/agtonomy) | Not ROS | `trellis`: custom C++ pub/sub middleware built as an alternative to ROS 2/DDS. |
| Hexagon | [github.com/hexagon-geo-surv](https://github.com/hexagon-geo-surv) | Not ROS | Almost entirely upstream mirrors/forks (Zephyr, u-boot, trusted-firmware, v8) — internal build infrastructure for Leica Geosystems, not custom application code. |
| TerraClear | [github.com/TerraClear](https://github.com/TerraClear) | ROS 1, unmaintained | `move_base` local planner, GNSS driver, ROSbot model. Mixed with unrelated JS/React Native repos. |
| FarmWise | [github.com/FarmWise](https://github.com/FarmWise) | ROS 1, all archived | `image_common`, an IMU driver (`sbg_ros_driver`). No longer maintained. |
| Wingtra | [github.com/wingtra](https://github.com/wingtra) | PX4, not ROS | Drone autopilot stack (fork of PX4-Autopilot, RTKLIB). Different ecosystem entirely. |
| AgriRobot | [github.com/AgriRobotAI](https://github.com/AgriRobotAI) | Unconfirmed | Looks like PyTorch/YOLO weed-detection scripts, not ROS infrastructure. |
| aitronik | [github.com/aitronik](https://github.com/aitronik) | Unclear | Student/thesis projects, some SLAM repos (`fastlio`, `rovio`) typically run inside ROS but not confirmed. |
| dailyrobotics | [github.com/dailyrobotics](https://github.com/dailyrobotics) | No ROS | Robot-learning/manipulation research (RoboAgent, ALOHA). Possibly not agricultural — worth double-checking it's the right org. |
| RobotMakers | [github.com/robotmakers](https://github.com/robotmakers) | Unknown | No public repos. |
| Topcon | [github.com/Topcon](https://github.com/Topcon) | Contradictory data | One direct check found a single repo called `empty`. A separate unverified source called it "SDK-focused" with no repos to back that up. Needs a manual recheck. |
| Boston Dynamics | [github.com/boston-dynamics](https://github.com/boston-dynamics), [github.com/bdaiinstitute](https://github.com/bdaiinstitute) | Not ag-related; AI Institute arm has `spot_ros2` | Two distinct orgs: the product SDK (Spot C++ SDK) and the separate Boston Dynamics AI Institute research arm. |
| Blue Robotics | [github.com/bluerobotics](https://github.com/bluerobotics) | Not ROS (own stack) | 78 repos, open-source-first: BlueOS, Cockpit, ping-protocol, a fork of ArduSub (ArduPilot for underwater vehicles). |
| ClearPath Robotics | [github.com/clearpathrobotics](https://github.com/clearpathrobotics) | Heavy ROS/ROS 2 | 300+ repos — `clearpath_common`, `cpr_gazebo`, drivers, mecanum drive controller. One of the most active ROS orgs found. |
| Twisted Fields | [github.com/Twisted-Fields](https://github.com/Twisted-Fields) | Not ROS | Acorn precision farming rover — Apache 2.0, Python + KiCad PCB designs, RP2040 motor controller firmware. Genuinely open-hardware. |
| Opentrons | [github.com/Opentrons](https://github.com/Opentrons) | Not ROS, not agricultural | Lab-automation robot (pipetting), extensively open: robot firmware, API, buildroot fork, app. Included for reference, not a crop-robotics company. |

## No public GitHub found / unrelated

| Company | Notes |
|---|---|
| Cerea | Unrelated — GitHub presence is an academic fluid-dynamics lab, not Cerea Autosteer. |
| Uncrewed | Unrelated — resolves to university drone-club repos, not a company. |
| FarmDroid (Farmdroid) | Org exists, zero public repositories. |
| BudBreak | No public repositories. |
| Croptimal | No public repositories. |
| AVL Motion | No public repositories. |
| Agmove-Robotics | Guessed org login doesn't resolve — wrong slug or private/deleted. |
| Asteria Aerospace | No GitHub org tied to the actual company found. |
| Microdrones | No GitHub org tied to the actual company found. |
| Skyfront | No GitHub org tied to the actual company found. |
| TensorField Ag | No GitHub org tied to the actual company found. |
| Carbon Robotics | No GitHub presence — proprietary, closed-source (LaserWeeder, "Carbon AI" Large Plant Model). |
| Garford | Traditional machinery manufacturer, no public engineering presence. |
| Hagie | Traditional machinery manufacturer, no public engineering presence. |
| Lemken | Traditional machinery manufacturer, no public engineering presence. |
| Autopickr | No GitHub org tied to the actual company found. |
| Agrobotics Inc | No GitHub org tied to the actual company found. |
| Monarch Tractor | No official corporate org. Company has largely ceased operations (assets acquired piecemeal by Caterpillar, April 2026); a community-run GitHub group has sprung up independently to keep existing MK-V tractors running. |
| AnyBotics | No corporate org — only individual employees' personal GitHub accounts with forked robotics tooling, consistent with ANYmal being closed-source. |
| Saga Robotics (Thorvald) | No corporate org found. Software was originally published as ROS packages via NMBU academic research (2018 paper), but no current public repo located. |
| EarthSense (TerraSentia) | No corporate org. Platform is widely used in academic ROS research (University of Illinois ROS-bag datasets, crop-row navigation papers) even though EarthSense's own code isn't public. |
| WindBorne Systems | No corporate org. Data/forecast API is partner-only; one unaffiliated fan-made visualisation project exists on GitHub. |
| SailDrone | No corporate org. Public Mission API is the only open surface; a few unrelated academic/NOAA repos process Saildrone-collected data. |
| Nauticus Robotics | No GitHub presence — closed-source cloud/autonomy software for subsea robots. |
| Hullbot | No GitHub presence. |
| Ocean Aero | No GitHub presence. |
| Teledyne Marine | No GitHub presence for the marine robotics division specifically (not checked: other Teledyne divisions, e.g. FLIR). |
| Genrobotic Innovations | No GitHub presence — closed-source, Bandicoot manhole-cleaning robot. |

## Still outstanding (from the larger climate-robotics spreadsheet, not yet checked)

The rest of the ~250-company source list — roughly 220 companies across the Aerial Robot, Ocean Robot, Robotic Arm, and long-tail Ground Robot categories — hasn't been checked yet.
