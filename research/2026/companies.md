# Crop Robotics Companies — GitHub Summary

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
| Naïo Technologies | [github.com/NaioTechnologies](https://github.com/NaioTechnologies) | Not ROS-native, one ROS-adjacent fork | Own proprietary stack (ApiCodec/ApiClient protocol, simulatoz simulator). Only ROS tie is a stale fork of `kacanopen` (a CanOpen-to-ROS bridge). Org looks dormant — last real activity ~2022. |
| Agtonomy | [github.com/agtonomy](https://github.com/agtonomy) | Not ROS | `trellis`: custom C++ pub/sub middleware built as an alternative to ROS 2/DDS. |
| Hexagon | [github.com/hexagon-geo-surv](https://github.com/hexagon-geo-surv) | Not ROS | Zephyr RTOS and firmware/GNSS-LiDAR tooling, embedded rather than ROS. |
| TerraClear | [github.com/TerraClear](https://github.com/TerraClear) | ROS 1, unmaintained | `move_base` local planner, GNSS driver, ROSbot model. Mixed with unrelated JS/React Native repos. |
| FarmWise | [github.com/FarmWise](https://github.com/FarmWise) | ROS 1, all archived | `image_common`, an IMU driver (`sbg_ros_driver`). No longer maintained. |
| wingtra | [github.com/wingtra](https://github.com/wingtra) | PX4, not ROS | Drone autopilot stack (fork of PX4-Autopilot, RTKLIB). Different ecosystem entirely. |
| AgriRobot | [github.com/AgriRobotAI](https://github.com/AgriRobotAI) | Unconfirmed | Looks like PyTorch/YOLO weed-detection scripts, not ROS infrastructure. |
| aitronik | [github.com/aitronik](https://github.com/aitronik) | Unclear | Student/thesis projects, some SLAM repos (`fastlio`, `rovio`) typically run inside ROS but not confirmed. |
| dailyrobotics | [github.com/dailyrobotics](https://github.com/dailyrobotics) | No ROS | Robot-learning/manipulation research (RoboAgent, ALOHA). Possibly not agricultural — worth double-checking it's the right org. |
| RobotMakers | [github.com/robotmakers](https://github.com/robotmakers) | Unknown | No public repos. |
| Topcon | [github.com/Topcon](https://github.com/Topcon) | Contradictory data | One direct check found a single repo called `empty`. A separate unverified source called it "SDK-focused" with no repos to back that up. Needs a manual recheck. |
| Cerea | — | Unrelated | GitHub presence is an academic fluid-dynamics lab, not Cerea Autosteer. |
| Uncrewed | — | Unrelated | Resolves to university drone-club repos, not a company. |
| No public repos | FarmDroid, BudBreak, Croptimal, AVL Motion | — | Orgs exist, zero public repos. |
| Not found | Agmove-Robotics, Asteria Aerospace, Microdrones, Skyfront, TensorField Ag, Carbon Robotics, Garford, Hagie, Lemken, Autopickr, Agrobotics Inc | — | No GitHub org tied to the actual company could be found. Most of these (Garford, Hagie, Lemken) are traditional machinery manufacturers with no public engineering presence; Autopickr, Carbon Robotics, Skyfront, TensorField Ag, Microdrones and Asteria Aerospace are real companies but either keep code private or have no discoverable org. |

## Flags

- Naïo, Topcon and TerraClear carry real but weak or contradictory ROS signal — worth a manual recheck.
- "dailyrobotics" doesn't read as an agricultural company at all — worth confirming it's even the right org before including it.

---------------
List sourced from image also in 2026 folder by Mixing bowl

**Navigation & Autonomy**
Agtonomy, Bonsai Robotics, RobotMakers, GOtrack, Ecorobotix(?), BlueWhite, GPX, farm(x), AgriCulture, Reichhardt, Avular, Nivavi, Aitronik, FieldBee, Sveaverken, Survey (unclear), Nature Robots, Move On, Agres, LACOS, JABAS.AI, FJDynamics, ProTracker, Mojow, Singular XYZ, TeeJet, MACH, Phenix, Hexagon, PTx Trimble, Topcon, Steyr, CHCNAV, Ag Leader, ASI, Sabanto, GINT, Raven, SDF, AgriRobot, Cerea, FarmNavigator, Cognitive Pilot, Bosch, Kingman Ag

**Platform/Carrier**
Uncrewed, Rotates, Xmachines, AGAR, Exobotic, Farmdroid, FieldWorkers, Orbita Robotics, TerraCroft, BCM, Naïo Technologies, Ponchon, Boson, All.Land, AgMove Robotics, Farm Robo, Ant Robotics, EOX Tractors, Robotrack

**Scouting**
Budbreak, H2L Robotics, Wingtra, Croptimal, Quantum Systems, IFT, Eagle Ray, Asteria Aerospace, Microdrones, Agtom, Terraclear, Skyfront, Eorobots

**Physical Weeding & Thinning**
TOR, TensorField, Carbon Robotics, Garford, Odbot, Tiefgrün, Error, SeedSpider, K.U.L.T., FarmWise, Photoneyler, Thorvald, Osiris, Tigo/Nigo, Zechtronik, Bbleap, Dynamo, Kilter, Hagie, Savefarm, Red Barn Engineering, F Poulsen Engineering, Eco-Bot, E-Terry, Pixel Farming Robotics, Aùwien, Harvested, Tillet & Hague, Feldklasse, Escaroa, CyanForce, Terra Robotics, Amazone, Arvatec, Cyclair, IWN, Newgreen, Oliver, Bednar, Andela, Lemken, Rivermeland, Drimac, Sinbelt, Farming Revolution, Agrobots, Pottinger, Kratzer, Aigen

**Field Harvesting**
Lommers, SAMI, Upp, AVL Motion, Harvest Croo Robotics, Cutlye, DailyRobotics, Prefiro, Autopickr, MiFood, Sylektis, Agrobot, Synphony

