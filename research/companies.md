
## Confirmed GitHub presence, most relevant first

| Company | GitHub | ROS status | Why it's relevant to Sowbot |
|---|---|---|---|
| Nature Robots | [github.com/naturerobots](https://github.com/naturerobots) | Heavy ROS 1/2 | `mesh_navigation`/`mesh_tools` does 3D-mesh terrain navigation instead of 2D grid maps — directly on point for the terrain/`caatinga-dev` branch work. `move_base_flex` is a close architectural cousin to `NavigationGateway`. |
| Sabanto | [github.com/sabantoag](https://github.com/sabantoag) | Heavy ROS 1, looks historic | RTK-GPS driver patterns (`ublox_f9p`, `ntrip_ros`) and `gps_goal_server` are close cousins of the dual-F9P RTK setup and `GPS_INPUT`-style bridging. |
| JABAS.AI | [github.com/jabasai](https://github.com/jabasai) | Heavy ROS 2 | `topological_navigation` is graph-based nav specifically for crop-row layouts — same problem space as `sowbot_row_follow`/TSM. |
| BlueWhite | [github.com/bw-robotics](https://github.com/bw-robotics) | Heavy ROS 1/2 | Forks of `kiss-icp` and `robot_localization` for tractor state estimation sit close to what FusionCore's UKF + wheel-slip detection is doing. |
| CHCNAV (Huace) | [github.com/HuaceNav](https://github.com/HuaceNav) | ROS drivers | Drivers for RTK-GNSS receivers and CGI-610 INS units — directly relevant to the dual-F9P GNSS and geofence-device u-blox F9P work. |
| Bonsai Robotics | [github.com/BonsaiRobotics](https://github.com/BonsaiRobotics) | Heavy ROS 2 | Amiga SDK, GNSS drivers, drive-by-wire kit, general ROS 2 tooling and `rosbag2` handling — broad overlap with the devkit stack. |
| Avular | [github.com/avular-robotics](https://github.com/avular-robotics) | ROS 2 (SDK level) | Nav2, behaviour trees, perception examples — useful as an architecture reference for the ROS 2 stack generally. |
| Blue Robotics | [github.com/bluerobotics](https://github.com/bluerobotics) | Not ROS (own stack) | Their ArduSub fork is the same ArduPilot lineage as the (now superseded) MAVLink bridge work — relevant as prior art even though the plan has moved to Cerebri/Zephyr. |
| Twisted Fields | [github.com/Twisted-Fields](https://github.com/Twisted-Fields) | Not ROS | Acorn is the closest thing on this list to an open-hardware Sowbot peer — KiCad PCB designs and RP2040 motor controller firmware, genuinely open. |
| ClearPath Robotics | [github.com/clearpathrobotics](https://github.com/clearpathrobotics) | Heavy ROS/ROS 2 | 300+ repos of general ROS 2 platform infrastructure — useful as a reference for patterns, less so for ag-specific code. |
| TerraClear | [github.com/TerraClear](https://github.com/TerraClear) | ROS 1, unmaintained | `move_base` local planner and GNSS driver for an ag robot, but stale and mixed with unrelated repos. |
| FarmWise | [github.com/FarmWise](https://github.com/FarmWise) | ROS 1, all archived | Ag-robot ROS packages, but archived and no longer maintained. |
| Naïo Technologies | [github.com/NaioTechnologies](https://github.com/NaioTechnologies) | Not ROS-native | Ag-robot competitor, but own proprietary protocol with only a stale ROS-adjacent fork — reference value only. |
| AgriRobot | [github.com/AgriRobotAI](https://github.com/AgriRobotAI) | Unconfirmed | PyTorch/YOLO weed-detection scripts — tangential to the plant-disease-detection YOLOX work, not crop-row nav. |
| Bosch / Bosch Research | [github.com/bosch](https://github.com/bosch), [github.com/boschresearch](https://github.com/boschresearch) | Heavy ROS 1/2 | `usb_cam` is a generic ROS camera driver — useful if a plain V4L2 camera node is ever needed, not ag-specific. |
| Boston Dynamics | [github.com/boston-dynamics](https://github.com/boston-dynamics), [github.com/bdaiinstitute](https://github.com/bdaiinstitute) | AI Institute arm has `spot_ros2` | General ROS 2 reference only — Spot isn't a wheeled ag platform. |
| Opentrons | [github.com/Opentrons](https://github.com/Opentrons) | Not ROS, not agricultural | Included for completeness — lab-automation robot, no direct overlap with Sowbot. |
| Agtonomy | [github.com/agtonomy](https://github.com/agtonomy) | Not ROS | `trellis` is a non-ROS middleware alternative — worth knowing about, not directly usable. |
| Wingtra | [github.com/wingtra](https://github.com/wingtra) | PX4, not ROS | Drone autopilot, different vehicle class and ecosystem entirely. |
| Hexagon | [github.com/hexagon-geo-surv](https://github.com/hexagon-geo-surv) | Not ROS | Almost entirely upstream mirrors (Zephyr, u-boot) with no custom application code — only relevant as confirmation that Zephyr is used in production elsewhere. |
| aitronik | [github.com/aitronik](https://github.com/aitronik) | Unclear | Student/thesis SLAM repos, not agricultural. |
| dailyrobotics | [github.com/dailyrobotics](https://github.com/dailyrobotics) | No ROS | Manipulation/robot-learning research, unrelated to field robotics. |
| RobotMakers | [github.com/robotmakers](https://github.com/robotmakers) | Unknown | No public repos — nothing to draw on. |
| Topcon | [github.com/Topcon](https://github.com/Topcon) | Contradictory data | One repo called `empty`; contradictory secondary source. Not usable as-is. |

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
| AnyBotics | No corporate org — only individual employees' personal GitHub accounts with forked robotics tooling. |
| Saga Robotics (Thorvald) | No corporate org found. Software was originally published as ROS packages via NMBU academic research (2018 paper), but no current public repo located. |
| EarthSense (TerraSentia) | No corporate org. Platform is widely used in academic ROS research (University of Illinois ROS-bag datasets, crop-row navigation papers) even though EarthSense's own code isn't public. |
| WindBorne Systems | No corporate org. Data/forecast API is partner-only; one unaffiliated fan-made visualisation project exists on GitHub. |
| SailDrone | No corporate org. Public Mission API is the only open surface; a few unrelated academic/NOAA repos process Saildrone-collected data. |
| Nauticus Robotics | No GitHub presence — closed-source cloud/autonomy software for subsea robots. |
| Hullbot | No GitHub presence. |
| Ocean Aero | No GitHub presence. |
| Teledyne Marine | No GitHub presence for the marine robotics division specifically. |
| Genrobotic Innovations | No GitHub presence — closed-source, Bandicoot manhole-cleaning robot. |
| Dendra Systems | No GitHub presence — closed-source RestorationOS platform (aerial seeding, ecology ML). |
| Pyka | No GitHub presence — proprietary autonomous electric aircraft stack. |
| Taranis | No GitHub presence — closed SaaS crop-intelligence platform. |
| TreeSwift | No GitHub presence — UPenn GRASP Lab spinoff, but SwiftCruise's code isn't public. |
| Outreach Robotics | No GitHub presence found. |
| Q-Bot | No GitHub presence found. |
| ARIX Tech | No GitHub presence found. |
| ZenRobotics | No GitHub presence — acquired by Terex in 2022, closed-source sorting AI. |
| Recycleye | No GitHub presence found. |
| AMP Robotics (AMP) | No GitHub presence — closed-source AMP Vision/Neuron waste-sorting AI. |
| Kubota Corporation | No GitHub org. Publishes OSS license-compliance pages only, no actual repos. |
| Aigen | No GitHub presence — proprietary solar-powered weeding robot. |
| Outrider | No GitHub presence — autonomous yard-truck logistics, closed-source. |
| Built Robotics | No GitHub presence found. |
| Icefin (Georgia Tech / Cornell) | No public repo found, despite being a long-running, well-documented academic AUV project. |
| OceanOneK (Stanford) | No public repo found — Stanford's tactile underwater humanoid robot project. |
| Impossible Metals | No GitHub presence — proprietary seabed-mining AUV (Eureka series). |
| Hydromea | No GitHub presence — proprietary underwater drones and optical comms. |

## Still outstanding

Roughly 190 rows remain unchecked from the original ~250-company climate-robotics spreadsheet.
