# Climate-robotics companies: GitHub presence, ranked for Agroecology-Lab / Sowbot

Ranked against `feldfreund_devkit_ros` (docker/Dockerfile): ROS 2 Jazzy, Nav2, Fields2Cover, LCAS `topological_navigation`, `caatingarobotics`, FusionCore, `ublox_dgnss`, Lizard/ESP32, rosys/NiceGUI, YOLOX, Forest3D, sentor, ros2_medkit, foxglove, rosbag2-mcap. Org repos also considered: `cerebri`, `ardupilot`, `acorn-precision-farming-rover`, `Open-Weeding-Delta`, `farmbot_*`, `TSM`.

## Confirmed GitHub presence, most relevant first

| Company | GitHub | ROS status | Why it's relevant to Sowbot |
|---|---|---|---|
| Nature Robots | [naturerobots](https://github.com/naturerobots) | Heavy ROS 1/2 | `mesh_navigation`/`mesh_tools` does 3D-mesh terrain navigation instead of 2D grid maps. On point for the terrain/`caatinga-dev` branch work. `move_base_flex` is a close cousin of `NavigationGateway`. |
| Burro (Augean Robotics) | [burro-robotics](https://github.com/burro-robotics) | ROS forks, 35 repos | Has a `Fields2Cover-fork`, the same library the Dockerfile builds in Stage 3.5. Also `witmotion_IMU_ros`, a Livox Mid-360 sim plugin, `burro-sdk`. Ownership inferred from repo content; profile has no website link. |
| Angsa Robotics | [angsa-robotics](https://github.com/angsa-robotics) | ROS 2, 36 repos, 1 original | Forks of `navigation2`, `opennav_coverage`, `robot_localization`, `ntrip_client`, `ublox`, `nmea_navsat_driver`, `rosbag2_snapshot`, `foxglove-py`, `ros2_control`, `teb_local_planner`. Nearly the devkit's dependency list, with their own patches (`ntrip_client`, `ublox`, `rviz_satellite`). `opennav_coverage` sits next to `devkit_f2c_planner`. |
| Earth Rover | [earthrover](https://github.com/earthrover) | ROS 1 (Catkin) | `OpenER` is an open-source ROS robot with mechanical design. Also `earth_rover_localization` (`robot_localization` EKF config), `er_vision_pipeline` (OpenCV + PCL), Piksi GNSS release repos. Closest ag peer to Sowbot after Twisted Fields. |
| farm-ng | [farm-ng](https://github.com/farm-ng) | ROS bridge + own SDK | `amiga-ros-bridge`, `amiga-ros-bridge-v1` (Rust), `farm-ng-core`, `amiga-dev-kit`, `amiga-dora-bridge`. Commercial ag rover with an open dev kit and a ROS bridge. |
| JABAS.AI | [jabasai](https://github.com/jabasai) | Heavy ROS 2 | `topological_navigation` is graph-based nav for crop-row layouts, same problem space as `sowbot_row_follow`/TSM. The Dockerfile pins LCAS's `topological_navigation`. |
| Twisted Fields | [Twisted-Fields](https://github.com/Twisted-Fields) | Not ROS | Acorn is the nearest open-hardware peer: KiCad PCBs, RP2040 motor controller firmware. Matches the org's `acorn-*` and `rp2040-motor-controller` repos. |
| Robotics 88 | [robotics-88](https://github.com/robotics-88) | ROS 2, 51 repos, 32 original | Original ROS 2 nodes: `trail-follower`, `path-manager`, `task-manager`, `bag_recorder_2`, `mp4-to-ros2`, `octomap-slice`, `ros-messages-88`. MAVROS repos (`airsim-mavros-wrapper`, `range-data-to-mavros`) relate to the org's `ardupilot` fork and `devkit_mavlink_bridge`. |
| Bonsai Robotics | [BonsaiRobotics](https://github.com/BonsaiRobotics) | Heavy ROS 2 | Amiga SDK, GNSS drivers, drive-by-wire kit, `rosbag2` handling. Broad overlap with the devkit stack. |
| Sabanto | [sabantoag](https://github.com/sabantoag) | Heavy ROS 1, historic | RTK-GPS driver patterns (`ublox_f9p`, `ntrip_ros`), `gps_goal_server`. Cousins of the dual-F9P setup and `GPS_INPUT`-style bridging. |
| BlueWhite | [bw-robotics](https://github.com/bw-robotics) | Heavy ROS 1/2 | Forks of `kiss-icp` and `robot_localization` for tractor state estimation. Close to FusionCore's UKF and wheel-slip detection. |
| CHCNAV (Huace) | [HuaceNav](https://github.com/HuaceNav) | ROS drivers | Drivers for RTK-GNSS receivers and CGI-610 INS units. Relevant to the dual-F9P GNSS work. |
| Swap Robotics | [swaprobotics](https://github.com/swaprobotics) | ROS 2 forks, 20 repos | Forks of `RTKLIB`, `ros-foxglove-bridge`, `mqtt_client`, `rosx_introspection`, `zed-ros2-wrapper`, `ros1_bridge`. Solar-farm vegetation robot on a stack similar to the devkit's. Ownership inferred. |
| Urban Machine | [urbanmachine](https://github.com/urbanmachine) | ROS 2, 6 original | `node_helpers` (ROS 2 framework), `create-ros-app` (production template), `colcon-poetry-ros`, `onshape-urdf-exporter`. Not ag. Reference for Docker/colcon/pyproject structure. |
| Avular | [avular-robotics](https://github.com/avular-robotics) | ROS 2 (SDK level) | Nav2, behaviour trees, perception examples. Architecture reference. |
| Scythe Robotics | [scythe-robotics](https://github.com/scythe-robotics) | C++, 1 original | `canfetti` is a CANopen stack in C++. Possibly useful for the CAN/DroneCAN ESC work on the Lizard fork. 5 other repos are forks. |
| Cosmic Robotics | [cosmic-robotics](https://github.com/cosmic-robotics) | ROS 2 forks | Forks of `YOLOX-ROS` (devkit uses YOLOX), `BehaviorTree.ROS2`, `moveit2`. Solar-panel installer; only `CADLock` is original. |
| Greenfield Robotics | [greenfieldrobotics](https://github.com/greenfieldrobotics) | 6 forks | Forks of `rmf_traffic_editor`/`free_fleet`, `IBusBM`, `TeensyProgramFlasher`. Weeding-robot fleet company; ownership inferred. |
| SwarmFarm | [swarmfarm](https://github.com/swarmfarm) | ROS forks, 2 original | Forks of `ouster-ros`, `tf2_web_republisher`, `LMS1xx`, `jsk_recognition`, `yolact_edge`. Sensor/web-UI stack of an ag swarm platform. |
| Blue Robotics | [bluerobotics](https://github.com/bluerobotics) | Not ROS | ArduSub fork, same ArduPilot lineage as the superseded MAVLink bridge. Prior art only; plan moved to Cerebri/Zephyr. |
| ClearPath Robotics | [clearpathrobotics](https://github.com/clearpathrobotics) | Heavy ROS/ROS 2 | 300+ repos of general ROS 2 platform infrastructure. Pattern reference, little ag-specific code. |
| 3Farmate Robotics | [3farmate-robotics](https://github.com/3farmate-robotics) | ROS 1 forks | 12 forks (`navigation`, `diffbot`, `gps-waypoint-based-autonomous-navigation-in-ros`, `Sawppy_Rover`). No original code. |
| Mission Robotics | [mission-robotics](https://github.com/mission-robotics) | C++/Arduino | Forks of `arduino-CAN`, `ODriveArduino`, `xsens_public_sdk`. Marine; only CAN/ODrive forks overlap. |
| Blue River Technology | [bluerivertechnology](https://github.com/bluerivertechnology) | Mostly forks | 28 of 30 repos are forks (incl. `ros2-web-bridge`). Originals: `CoPilot-Workshop`, `tf_sample`. |
| TerraClear | [TerraClear](https://github.com/TerraClear) | ROS 1, unmaintained | `move_base` local planner and GNSS driver for an ag robot. Stale, mixed with unrelated repos. |
| FarmWise | [FarmWise](https://github.com/FarmWise) | ROS 1, all archived | Ag-robot ROS packages, archived. |
| Naïo Technologies | [NaioTechnologies](https://github.com/NaioTechnologies) | Not ROS-native | Own protocol, stale ROS-adjacent fork. Reference only. |
| AgriRobot | [AgriRobotAI](https://github.com/AgriRobotAI) | Unconfirmed | PyTorch/YOLO weed-detection scripts. Tangential to the YOLOX disease work. |
| ICON | [iconbuild](https://github.com/iconbuild) | ROS 2 forks | Husarion and Fixposition forks (`fixposition_driver`, `navigation2`, `depthai-ros`, `foxglove-bridge-docker`). Construction 3D printing; GNSS/VIO driver is the only overlap. |
| Botlink | [botlink](https://github.com/botlink) | C++/Go | `botlink-xrd-sdk` (drone datalink), MAVLink Go libs. Different vehicle class. |
| WildDrone | [wilddrone](https://github.com/wilddrone) | Python/Kotlin | `SkyLoop` (multi-drone relay), `WildBridge` (DJI ground station). Drones, not ground robots. |
| EyeROV | [eyerov](https://github.com/eyerov) | ROS fork | `rplidar_ros` fork plus data-collector backend. Underwater; little overlap. |
| PaintJet | [paintjet](https://github.com/paintjet) | ROS 1 | `roomba-autonomy`, DWM1001 UWB interface, rosbag analysis. Low. |
| GrayMatter Robotics | [graymatter-robotics](https://github.com/graymatter-robotics) | ROS forks | `zivid-ros`, `trajopt`, `ros1_bridge` forks. Industrial sanding; low. |
| Bosch / Bosch Research | [bosch](https://github.com/bosch), [boschresearch](https://github.com/boschresearch) | Heavy ROS 1/2 | `usb_cam` (generic V4L2 driver; Dockerfile already installs `ros-jazzy-usb-cam`). |
| Boston Dynamics | [boston-dynamics](https://github.com/boston-dynamics), [bdaiinstitute](https://github.com/bdaiinstitute) | AI Institute has `spot_ros2` | General ROS 2 reference. Not a wheeled ag platform. |
| Sofar Ocean | [sofarocean](https://github.com/sofarocean) | Python | Spotter buoy data tooling (`roguewave`, `spotter-sd-parser`). No ROS. |
| Otherlab | [otherlab](https://github.com/otherlab) | C++/Python | `geode`, `simplicity`, `petiga`: computational geometry and FEM. No ROS. |
| Meteomatics | [meteomatics](https://github.com/meteomatics) | None | Weather-API connector libraries only. |
| Agtonomy | [agtonomy](https://github.com/agtonomy) | Not ROS | `trellis` is a non-ROS middleware alternative. |
| Wingtra | [wingtra](https://github.com/wingtra) | PX4, not ROS | Drone autopilot. Different vehicle class. |
| Hexagon | [hexagon-geo-surv](https://github.com/hexagon-geo-surv) | Not ROS | Mostly upstream mirrors (Zephyr, u-boot). Confirms Zephyr is used in production elsewhere. |
| Opentrons | [Opentrons](https://github.com/Opentrons) | Not ROS, not ag | Lab automation. No overlap. |
| aitronik | [aitronik](https://github.com/aitronik) | Unclear | Student/thesis SLAM repos. |
| dailyrobotics | [dailyrobotics](https://github.com/dailyrobotics) | No ROS | Manipulation research. |
| RobotMakers | [robotmakers](https://github.com/robotmakers) | Unknown | No public repos. |
| Topcon | [Topcon](https://github.com/Topcon) | Contradictory data | One repo called `empty`. Not usable as-is. |

## No public GitHub found / unrelated

| Company | Notes |
|---|---|
| Cerea | Unrelated: GitHub presence is an academic fluid-dynamics lab, not Cerea Autosteer. |
| Uncrewed | Unrelated: resolves to university drone-club repos. |
| FarmDroid | Org exists, zero public repositories. |
| BudBreak, Croptimal, AVL Motion | No public repositories. |
| Agmove-Robotics | Guessed org login doesn't resolve. |
| Asteria Aerospace, Microdrones, Skyfront, TensorField Ag, Autopickr, Agrobotics Inc | No GitHub org tied to the actual company found. |
| Carbon Robotics | No GitHub presence; proprietary (LaserWeeder, "Carbon AI"). |
| Garford, Hagie, Lemken | Traditional machinery manufacturers, no public engineering presence. |
| Monarch Tractor | No official org. Largely ceased operations (assets acquired piecemeal by Caterpillar, April 2026); a community-run GitHub group keeps existing MK-V tractors running. |
| AnyBotics | No corporate org; only employees' personal forks. |
| Saga Robotics (Thorvald) | No corporate org. Original ROS packages came via NMBU academic research (2018), no current public repo located. |
| EarthSense (TerraSentia) | No corporate org. Widely used in academic ROS research, but own code isn't public. |
| WindBorne Systems | No corporate org. API is partner-only; one unaffiliated fan project. |
| SailDrone | No corporate org. Only the public Mission API. |
| Nauticus Robotics, Hullbot, Ocean Aero, Teledyne Marine | No GitHub presence (Nauticus closed-source). |
| Genrobotic Innovations, Dendra Systems, Pyka, Taranis, AMP Robotics, Aigen, Outrider, ZenRobotics, Impossible Metals, Hydromea | No GitHub presence; closed-source. |
| TreeSwift | No GitHub presence; UPenn GRASP spinoff, SwiftCruise code not public. |
| Outreach Robotics, Q-Bot, ARIX Tech, Recycleye, Built Robotics, Icefin, OceanOneK | No GitHub presence found. |
| Kubota Corporation | No org; OSS licence-compliance pages only. |
| Air Forestry, Charge Robotics, EarthForce, Elythor, ACWA Robotics, Gravis Robotics, Logiqs, Okibo, Hyperion Robotics, Silana, RanMarine, Insight Robotics | Org exists, no public repos listed. |
| Kestrix, Terabase Energy, Neptune Robotics, Toggle Robotics, CleanRobotics, Baubot, Flash Forest, Open Ocean Robotics | Org exists with 1-4 repos, all forks or trivial (Baubot: `ctrlx-automation-sdk-ros2` fork). |
| Bear Flag Robotics, Bloomfield Robotics, Solinftec | Org exists. Only website repo, docs/support and changelog templates; no robot code. |
| Airseed | `airseed` org points to airseed.com, not airseedtech.com: different company. API client libraries only. |
| Terran Robotics | Org exists but the company builds homes, not weeding robots (sheet row looks wrong). Only `usb_cam`/`apriltag` forks. |
| BladeBUG, Easy Floor Robotics, Korechi, Reefgen, Terradepth, NixieDip, Windracers, Windbotix, Borobotics, GreenDigger, Sudoyantra, PV Circonomy, Recirculate | No GitHub account found under any candidate slug. |
| Beewise, Tertill, Dusty Robotics, Yarbo, Zordi, Rain, Pave Robotics, Ripe Robotics, Floating Robotics, Harvest Automation, Enerkite, PIX Moving | Candidate accounts exist but couldn't be tied to the company. Tertill's is a game-dev account; Dusty's has `symforce`/`symengine` forks only. |

## Still outstanding

- About 100 rows (mostly marine, construction, recycling, drone, lab entries) had no verified org. Method was slug probing plus website match, not full web search.
- Next: web search on ag-relevant unconfirmed ones: Ecorobotix, Agrobot, Tortuga, Korechi, Ripe Robotics, Harvest CROO, FarmRobo, Yarbo, Zordi.
- Repo lists only; commit recency and licences not checked.
- Burro, Swap, Greenfield ownership inferred (no website link on profile).
## Still outstanding

Roughly 190 rows remain unchecked from the original ~250-company climate-robotics spreadsheet.

Startup/Company/Lab	Website	Robotics	Deployed	Founded	Country HQ	Continent HQ	Deployment Countries 	Robotics Type	Main Application	Additional Application	Adaptation / Mitigation	Biome Type	Does This Entry Contain an Error? If So, Please Insert a Comment Correction Here	Describe what the Robotics solutions does in one sentence.	VCs Invested (coming soon!)	Job Board (coming soon!)	Comments	Links to Relevant Videos	Video Descriptions	LinkedIn Page	Facebook / Instagram																		
Air Forestry	https://www.airforestry.com/en/	Yes	No	2020	Sweden	Europe	Sweden,Norway	Aerial Robot	Biodiversity	Aviation	Both	Forests / Silviculture		Develops electric drones that thin forests from above snipping branches, felling selected trees, and transporting logs to roads with minimal ground impact and reduced emissions.	Northzone,Sveaskog,Kiko VC,CapitalT,Walderud Ventures,SEB Greentech VC,Cloudbreak VC	https://careers.airforestry.com/#jobs		https://www.youtube.com/watch?v=WSjcIPWAaOw	Video shows how the drone searches for tree and ci=ut out the selected tree.	https://www.linkedin.com/company/airforestry/	https://www.instagram.com/airforestrysweden/																		
Airseed	https://airseedtech.com/	Yes	Yes	2018	Australia	Oceania	 Australia 	Aerial Robot	Land Restoration	Carbon Removal	Both	Forests / Silviculture		AirSeed utilizes autonomous drones and biotech-integrated seed pods to accelerate large-scale reforestation and ecosystem restoration.	Conscious Investment Management (CIM),TWIYO	https://www.linkedin.com/company/airseedtech/jobs/
		https://www.youtube.com/watch?v=UsvrkVU0Qpw	Video shows the steps that the company took to achieve their goal and short description of their company.	https://www.linkedin.com/company/airseedtech/	https://www.facebook.com/AirSeed																		
Botlink 	https://botlink.com/	Yes	Yes	2016	US	North America	US,Brazil,Italy	Aerial Robot	Environmental Monitoring	Agriculture	Both	Agriculture / Farmland		Provides aerial platforms and software for environmental monitoring—enabling air-quality sensing, NDVI vegetation mapping, and high-definition terrain modeling		https://botlink.com/our-opportunities	Pollution sensing/mapping	https://www.youtube.com/watch?v=rf7QPvoTFaY	Video shows how drones help in agriculture.	https://www.linkedin.com/company/botlink	https://www.instagram.com/botlink																		
CO2Revolution	https://co2revolution.es/en/	Yes	Yes	2014	Spain	Europe	Spain,Portugal,France,Colombia,Peru,Honduras,Morocco,Australia        	Aerial Robot	Nature Conservation	Carbon Removal	Mitigation	Forests / Silviculture		combines traditional planting method with advanced technology and intelligent seeds for reforestation.	Iberdrola,Orizont,Solar Impulse,Sodena,Desafia,CEIN	https://www.linkedin.com/company/co2-revolution/jobs/
		https://www.youtube.com/watch?v=1KiBHaKvv9M	Video describes the main motto of the company.	https://www.linkedin.com/company/co2revolution/	https://www.instagram.com/co2revolution																		
Dendra	https://dendra.io	Yes	Yes	2014	England	Europe	Australia, Peru, Ghana, Switzerland, US, UK	Aerial Robot	Agriculture	Biodiversity	Both	Forests / Silviculture		Provides an AI-enabled platform (RestorationOS™) integrating aerial imaging, ecosystem monitoring, and drone seeding to restore large-scale ecosystems	Zouk Capital,Aramco Ventures,Airbus Ventures,Understorey Capital,Helium-3 Ventures,At One Ventures,Future Positive Capital,Lowercarbon Capital,Lionheart Ventures,SYSTEMIQ,VentureSouq	https://dendra.io/about-us/careers/		https://www.youtube.com/watch?v=ynSjIYb4BxI	Video shows dendra are restoring biodiverse ecosystems at scale using data science, artificial intelligence and drones.	https://www.linkedin.com/company/dendra-systems/	https://www.facebook.com/dendrasystems																		
Distant Imagery	https://www.distantimagery.com/	Yes	Yes	2019	UAE	Asia	UAE,Ecuador,Madagascar,Kenya	Aerial Robot	Land Restoration	Environmental Monitoring	Mitigation	Coastal / Marine Shallow		Builds custom aerial and marine drones with AI-powered imaging and MRV platforms to restore and monitor mangrove and coastal ecosystems		none		https://www.youtube.com/watch?v=lx1MV_dnobY	Video shows the description of the company.	https://www.linkedin.com/company/distant-imagery-solutions/	https://www.facebook.com/distantimagery/																		
Drone Amplified	https://droneamplified.com/	Yes	Yes	2017	US	North America	US, Canada, Germany, and Australia.	Aerial Robot	Nature Conservation	Multiple	Mitigation	Forests / Silviculture		Drone Amplified develops aerial ignition systems that use drones to drop fire-starting spheres for controlled burns, mitigating catastrophic wildfire risks while keeping firefighters safe on the ground.
	Invest Nebraska (VC),Nebraska Angels 	none		https://www.youtube.com/watch?v=VdvyG1i6ESE	Video shows Drone Amplified's IGNIS system is a revolutionary product for unmanned aerial ignition	https://www.linkedin.com/company/drone-amplified	https://www.instagram.com/droneamplified/ https://x.com/droneamplified																		
Ecording	https://ecording.org/en/	Yes	Yes	2017	Turkey	Asia & Europe	Turkey	Aerial Robot	Land Restoration	Nature Conservation	Mitigation	Forests / Silviculture		Uses drones and technology for reforestation and ecosystem restoration to combat the global climate crisis		https://ecording.org/en/career/		https://www.youtube.com/watch?v=cggyNle1Q2s	Video shows Operation 17 by ecording, an environmental social enterprise that uses ecoDrones for reforestation	https://www.linkedin.com/company/ecording2nature/	https://www.facebook.com/ecording2nature																		
Elythor	https://elythor.com/	Yes	No	2023	Switzerland	Europe	Switzerland	Aerial Robot	Inspection	Inspection	Mitigation	Industrial / Energy Infrastructure		Elythor develops shape-shifting VTOL drones that transform between quadcopter and fixed-wing configurations to inspect energy infrastructure like wind turbines and oil rigs in extreme weather, exploiting wind currents to extend flight endurance for hours.
		https://elythor.com/careers/	Inspecting and monitoring linear infrastructure.	https://www.youtube.com/watch?v=Fm22qIp7p60	Video shows the morphology inspection of drone.	https://www.linkedin.com/company/elythor/	https://www.instagram.com/_elythor_?r=nametag  https://www.facebook.com/elythor  https://x.com/_elythor_																		
Enerkite	https://enerkite.de/en/	Yes	Yes	2010	Germany	Europe	Germany	Aerial Robot	Distributed Energy	Distributed Energy	Mitigation	Coastal / Marine Shallow		Developer of airborne wind energy systems. Aiming for ultra high capacity factors and low cost of distributed energy generation.		https://enerkite.de/en/#Jobs		https://www.youtube.com/watch?v=UyzkMBFz3Bw&t=9s	Video shows the EnerKíte’s groundbreaking wind energy solutions! Using kite-based systems, EnerKíte offers a highly efficient and sustainable alternative to traditional wind turbines, harnessing stronger, more consistent winds at higher altitudes. This technology promises lower costs, reduced environmental impact, and a scalable energy solution for the future.	https://www.linkedin.com/company/enerkite/?originalSubdomain=de	 https://www.instagram.com/enerkite																		
Envicotech	https://www.envicotech.co.nz/	Yes	Yes	2013	New Zealand	Oceania	New Zealand,Australia & Argentina	Aerial Robot	Nature Conservation	Land Restoration	Both	Forests / Silviculture		Envicotech uses drones to eradicate invasive pests (rats, possums) from islands and forests while aerially dispersing seed pods for native reforestation to protect ecosystems in New Zealand, the Galapagos Islands, and beyond.		https://www.envicotech.co.nz/careers		https://www.youtube.com/watch?v=2JDit2oM41c	Video describes the aim of company along with the steps they are taking.	https://www.linkedin.com/company/envicotech/?viewAsMember=true	https://www.facebook.com/EnvicoTech																		
First Airborne	https://firstairborne.com/	Yes	Yes	2017	Israel	Asia	Israel,UK,Romania,Isreal	Aerial Robot	Wind Turbines	Asset Inspection	Mitigation	Industrial / Energy Infrastructure		Intensive services rendered in the wind power industry into automated robotics-based services.	Roca X,Climate First,Itamar Weizman,Firstime,L Marks,Nomea (UK)	https://firstairborne.com/join/		https://www.youtube.com/watch?v=fj1H2P3JxpA	Boaz Peled, co-founder and CEO of First Airborne, discusses their patented Windborne drone sensor technology that revolutionizes wind measurement for wind farms. The system provides precise, high-altitude wind data and turbine performance testing to optimize energy output, reduce maintenance costs, and improve renewable energy efficiency.firstairborne​	https://www.linkedin.com/company/first-airborne/																			
Flash Forest	https://flashforest.ca/	Yes	Yes	2019	Canada	North America	Canada,US	Aerial Robot	Land Restoration	Nature Conservation	Both	Forests / Silviculture		Flash Forest uses AI-guided drones to fire biodegradable seed pods into post-wildfire landscapes , rapidly replanting forests for carbon sequestration and ecosystem restoration.	TELUS Pollinator Fund for Good,OurCrowd,Mizrahi Enterprises,Sagana,TELUS Global Ventures	https://flashforest.ca/careers		https://www.youtube.com/watch?v=9QrvPHuqH0I	Video describes how drones are used to plant trees.	https://www.linkedin.com/company/flashforest/	https://www.facebook.com/flashforest.ca/																		
Inverto Earth	https://www.inverto.tech/	Yes	Yes	2022	Switzerland	Europe	EU countries	Aerial Robot	Restoration	Multiple	Both	Coastal / Marine Shallow		To inverts the loss of coastle wetlands.		none	Environment friendly operations in restoration and agriculture.	https://www.youtube.com/watch?v=UK5iKQPCe2A	Video shows Seed darts (or seed pods) deployed by drones are an innovative reforestation technology designed to plant trees at a scale and speed that traditional hand-planting.	https://www.linkedin.com/company/inverto-earth/																			
Kestrix	https://www.kestrix.io/	Yes	Yes	2022	UK	Europe	UK	Aerial Robot	Asset Inspection	Data Collection	Mitigation	Urban / Built Environment		Kestrix uses thermal drones to scan buildings and create 3D "heat loss maps," identifying energy inefficiencies to enable targeted retrofitting and decarbonization of building stock.	"Notion Capital,Pi Labs,Oxford Seed Fund	"	https://kestrix.notion.site/kestrix/Kestrix-Job-Board-e6ffe3f141db4e768d546289530396b7		https://www.youtube.com/watch?v=4Mn9h0aiw14	Video shows Kestrix as a startup that uses drones and AI to identify heat loss in buildings.	https://www.linkedin.com/company/kestrix/?viewAsMember=true																			
KiteKraft	http://www.kitekraft.de/	Yes	No	2019	Germany	Europe	Germany	Aerial Robot	Wind Turbines	Distributed Energy	Mitigation	Atmosphere/Aerial		Creates the flying wind turbines which generates electrical energy from the wind at low cost.	"Y Combinator	,Schweizer Kapital Global Impact Fund AG"	https://www.kitekraft.de/vacancies#full-time-jobs		https://youtu.be/3122dVQniFE	Video shows the use of flying wind turbines.	https://www.linkedin.com/company/kitekraft/	https://x.com/kitekraft_tech																		
Mast Reforestation (DroneSeed)	https://www.droneseed.com/	Yes	Yes	2016	US	North America	US,Canada	Aerial Robot	Land Restoration	Carbon Removal	Mitigation	Forests / Silviculture		Mast Reforestation provides end-to-end reforestation using heavy-lift drone swarms to drop seed vessels in wildfire-ravaged landscapes while burying fire-killed trees underground to generate verified carbon credits for carbon removal.
	DBL Partners, Social Capital, Marc Benioff, Ozmen Ventures, Elemental Excelerator, USDA Climate-Smart Commodities	https://jobs.lever.co/MastReforestation		https://www.youtube.com/watch?v=1nBDOYY19o4	Videos shows the project progress of Mast Reforestation.	https://www.linkedin.com/company/mast-reforest/	https://www.instagram.com/mast.reforest/																		
MeteoMatics AG	https://www.meteomatics.com	Yes	Yes	2012	Switzerland	Europe	Switzerland, Germany, UK, USA, Norway, Spain 	Aerial Robot	Environment Monitoring 	Environmental Monitoring	Adaptation	Atmosphere/Aerial		MeteoMatics AG provides hyperlocal weather data and forecasts via API to help businesses and governments plan operations and manage weather-related risks and secondly Autonomous weather drones that fly up to 6 km altitude to collect atmospheric data from mid and low levels, especially for areas lacking traditional weather stations.	Armira Growth,Alantra (Klima),Lockheed Martin Ventures,Fortyone	https://careers.meteomatics.com/#jobs	Primarily Weather API system & Secondary Climate robotics Startup!	https://www.youtube.com/watch?v=Wc1s55c8xdU   https://www.youtube.com/watch?v=PdbMnlq0c5c	Videos shows the Air Quality Insights with MetX.	https://www.linkedin.com/company/meteomatics/	https://www.facebook.com/MeteomaticsAG																		
MORFO	https://www.morfo.rest/	Yes	Yes	2021	France,Brazil 	Europe, Africa	Libreville,Brazil,Guiana,Gabon,French Guiana	Aerial Robot	Land Restoration	Data Collection	Mitigation	Forests / Silviculture		Forest restoration via drones and monitoring technology to analyze soild or places to check where to implement the plane, similar to all other reforestation effort.	Demeter, Raise Ventures, AFI Ventures, TeamPact Ventures, plus business angels	https://www.linkedin.com/jobs/search/?currentJobId=3822465776&f_C=77041894&geoId=92000000&origin=COMPANY_PAGE_JOBS_CLUSTER_EXPANSION&originToLandingJobPostings=3822465776%2C3823477049%2C3831076461%2C3831078179		https://www.youtube.com/watch?v=ubwEwtjRlLE	Video shows the two-year partnership between MORFO and the Federal University of São Carlos (UFSCAR), specifically its Forest Engineering Department, to enhance large-scale forest restoration through scientific innovation.	https://www.linkedin.com/company/morforest/	https://www.facebook.com/profile.php?id=100083969613598																		
Outreach Robotics	https://www.outreachrobotics.com/	Yes	Yes	2019	Canada	North America	Canada,US	Aerial Robot	Agriculture	Nature Conservation	N/A	Forests / Silviculture		Outreach Robotics develops advanced aerial robots, including the Mamba, to safely collect plant samples from cliffs for biodiversity conservation		none	With the help of drones performed the work in outreach area.	https://www.youtube.com/watch?v=bSNJpNa_JzM   https://www.youtube.com/watch?v=bUnMUQKph2Q	Videos shows the drone endemic cliff plant specimen collection and rainforest biodiversity monitoring station.	https://www.linkedin.com/company/outreachrobotics/	https://www.facebook.com/OutreachRobotics/  https://x.com/OutreachRobotic 																		
Pyka	https://www.flypyka.com/	Yes	Yes	2017	US	North America	USA,Brazil	Aerial Robot	Agriculture	Aviation	Mitigation	Agriculture / Farmland		Pyka develops fully autonomous electric aircraft for agriculture and cargo transport, providing safe, clean, and efficient aerial solutions.	Obvious Ventures; Piva Capital; Prelude Ventures; Metaplanet Holdings; Y Combinator	https://boards.greenhouse.io/pyka	Aviation Automation 	https://www.youtube.com/watch?v=aeu6Cg13ZbA  https://www.youtube.com/watch?v=MCK4h6EffuI	Videos shows the Pyka's 100% Electric Cargo UAS Joins Skyports Drone Services Logistics Fleet.	https://www.linkedin.com/company/flypyka/																			
Meteoglider	https://www.r2ho.me/	Yes	No	2019	Switzerland	Europe	Switzerland	Aerial Robot	Environmental Monitoring	Other	Mitigation	Atmosphere/Aerial		Enhance weather forecasting and climate change research while minimizing the environmental impact of weather balloons worldwide.		none		https://www.youtube.com/watch?v=NDLpS5nnJzU&t=2s   https://www.youtube.com/@YohanHadji/featured	Videos shows that the R2Home Guided Parachute - High Altitude Demo video.	https://www.linkedin.com/in/yohanhadji/																			
ScentRoid	https://scentroid.com/products/analyzers/dr1000-flying-lab/	Yes	Yes	2007	Canada	North America	Canada,Saudi Arabia, the United Arab Emirates, Qatar, Oman	Aerial Robot	Environmental Monitoring	Multiple	Mitigation	Forests & Terrestrial		Air quality mapping, model verification, and analysis of potentially dangerous sites.		https://scentroid.com/careers/		https://youtu.be/mUyKZt9Ez4c	Video shows the benefits of Dr1000 air quality drone.	https://www.linkedin.com/company/scentroid/	https://www.instagram.com/scentroid/ https://www.facebook.com/scentroid/ https://x.com/scentroid 																		
Sky Specs	https://skyspecs.com	Yes	Yes	2012	US	North America	Netherland, US,Ireland,Denmark,India	Aerial Robot	Asset Inspection	Data Collection	Mitigation	Industrial / Energy Infrastructure		Sky Specs provides fully autonomous drone-based inspections and AI-powered analytics for wind turbine blades and drivetrain components, enabling predictive maintenance and asset optimization across onshore and offshore wind farms.	Goldman Sachs Alternatives,Goldman Sachs,McRock Capital,Statkraft Ventures,Venture Investors	https://skyspecs.com/about/careers/		https://www.youtube.com/watch?v=CtDbN--xuag	Videos shows the Lufthansa to Expand Into North America.	https://www.linkedin.com/company/skyspecs/	https://www.facebook.com/profile.php?id=100077255605100																		
SkyPull	https://www.skypull.com/	Yes	No	2017	Switzerland	Europe	Switzerland	Aerial Robot	Wind Turbines	Distributed Energy	Mitigation	Coastal / Marine Shallow		SkyPull develops airborne wind energy systems (AWES) that use tethered dual-drone technology to generate electricity from high-altitude winds.
	Shibumi International,EIC Fund	none		https://www.youtube.com/watch?v=PmrpWqQKyOM​	Skypull's airborne wind energy system uses autonomous VTOL aircraft flying like kites at high altitudes to generate electricity via tether-pulling, using 95% less material than traditional turbines while doubling production.​​	https://www.linkedin.com/company/skypull/	https://www.instagram.com/workwithatom/ https://www.facebook.com/atomdotcom https://x.com/atomhq 																		
Taranis	https://www.taranis.com/	Yes	Yes	2015	US	North America	Brazil,US,Canada,Australia,Ukrain,Argentina,Russia	Aerial Robot	Agricultural	Other	Both	Agriculture / Farmland		Taranis uses AI-powered drone and satellite imagery to provide leaf-level crop intelligence, detecting pests, diseases, and nutrient deficiencies while delivering data-driven agronomic recommendations and conservation services to farmers globally.
	"Inven Capital,Vertex Growth,Kuok Group's Orion Fund	,Finistere Ventures,Viola Ventures,Seraphim Space,Mitsubishi UFJ Capital,Mitsubishi UFJ Capital,Hitachi Ventures,Micron Ventures"	https://www.taranis.com/careers/#link__list__content	Deep agronomic expertise and AI.	https://www.youtube.com/watch?v=R72yEPVX9Cc   https://www.youtube.com/watch?v=yOcfufxpIvA	Videos shows the full-stack solution for high precision aerial surveillance imagery to prevent crop yield loss due to insects, nutrient deficiencies.	https://www.linkedin.com/company/taranis-visual/	https://www.facebook.com/taranisvisual/																		
TreeSwift	https://www.treeswift.com/	Yes	Yes	2020	US	North America	US	Aerial Robot	Inspection	Environmental Monitoring	Both	Forests / Silviculture		Treeswift builds SwiftCruise, a drone-based solution using robotics and AI to generate per-tree metrics for forest inventory, biomass estimation, carbon capture, and fire risk mitigation.”	 Pathbreaker Ventures,Crosslink Capital, TenOneTen Ventures, Contour Venture Partners, Boom Capital Ventures, Yes VC, Susa Ventures,Draft Ventures, Anorak Ventures, S7 Ventures, Awesome People Ventures, Switch Ventures, Convective Capital, 	https://www.treeswift.com/careers	Robotics and Forestry.	https://www.youtube.com/watch?v=VdhaCOFmklE	Video shows the building forests inventories.	https://www.linkedin.com/company/treeswift/																			
Wildlife Drones	https://wildlifedrones.net	Yes	Yes	2016	Australia	Oceania	Australia,New Zealand	Aerial Robot	Environment Monitoring 	Environment Monitoring 	N/A	Forests & Terrestrial		Wildlife Drones uses radio-telemetry and thermal imaging drone systems to track and monitor wildlife, endangered species, invasive species, and conduct surveys over large, rugged areas	Uniseed; Draper Startup House Ventures; Stoic VC; plus angel investors.	https://wildlifedrones.net/careers/		https://www.youtube.com/watch?v=RNjE-vslBqo https://www.youtube.com/watch?v=QR57wFL-GSw	Videos shows the thermal imaging survey to detect Koalas in Australia.	https://www.linkedin.com/company/wildlife-drones/	https://www.facebook.com/WildlifeDrones/																		
Wingtra AG	https://wingtra.com/	Yes	Yes	2017	Switzerland	Europe	US,Kenya,UK,Mexico,Australia,Colombia,Panama	Aerial Robot	Inspection	Environment Monitoring 	N/A	Atmosphere/Aerial		leverage drone technology for efficient data collection and actionable insights across various sectors.	DiamondStream Partners; EquityPitcher Ventures; Verve Ventures; European Innovation Council Fund (EIC Fund); ACE & Company; John L. Steffens (Spring Mountain Capital); RKKVC; SymbiaVC; Spectrum Moonshot Fund; Cadence Growth Capital	https://wingtra.com/company/career/	Drone Technology.	https://www.youtube.com/watch?v=T9mxfHyTtJg https://www.youtube.com/watch?v=NqlRQ3FJIDA	Video shows the remote inspection.	https://www.linkedin.com/company/wingtra/	https://www.instagram.com/wingtra_official/  https://x.com/Wingtra  https://www.facebook.com/WingtraOne 																		
ACWA Robotics 	https://www.acwa-robotics.com	Yes	No	2018	France	Europe	France	Ground Robot	Asset Inspection	Inspection	N/A	Coastal / Water Infrastructure		ACWA Robotics builds in-pipe inspection robots that navigate water distribution networks to collect condition data (corrosion, wall thickness, leaks) and enable utilities to reduce water loss and improve maintenance planning without interrupting service.	Calao Finance, Région Sud Investissement,  Sofimac Innovation,Banque des Territoires, FMG Circular Invest, UI Investissement, Crédit Agricole Alpes Provence, Calao Finance, and Région Sud Investissement. 	none		https://www.acwa-robotics.com/solution/	Videos shows about the Acwa robotics solutions.	https://www.linkedin.com/company/acwa-robotics/?originalSubdomain=fr	https://www.facebook.com/acwarobotics																		
Aerones	https://aerones.com/	Yes	Yes	2015	Latvia	Europe	US,Brazil,Latvia	Ground Robot	Wind Turbines	Asset Inspection	Mitigation	Coastal / Water Infrastructure		Aerones uses heavy-lift climbing robots to ascend wind turbine towers and perform hands-on blade cleaning, inspection, and repair, while  the same technology for high-rise building and infrastructure maintenance.	"Activate Capital,S2G Investments,Lightrock,Change Ventures,Future Positive Capital	,Y Combinator,Blume Equity,Carbon Equity,Overlap Holdings,Extantia,"	https://aerones.easycruit.com/		https://www.youtube.com/watch?v=HC1P96j32Lc https://www.youtube.com/watch?v=2-1a1_hHYdU	Videos shows the Aerones case study by Haniel  and aerones Offshore Winch System Tests for Robotic Wind Turbine Inspections and Repairs.	https://www.linkedin.com/company/aerones/	https://www.facebook.com/aeronescom https://www.instagram.com/aerones_com/ 																		
Agricultural Robotics Lab	https://yanglab.bbe.umn.edu/	Yes	No	N/A	US	North America	US	Ground Robot	Agriculture	Data Collection	N/A	Agriculture / Farmland		To apply advanced ideas of robotics, remote sensing, data mining and information technology into precision agriculture.		None	Lab focus on agricultural automation and robotics technology, not climate change.	https://www.youtube.com/watch?v=so4ZkTvbtQo   https://www.youtube.com/watch?v=BRylsItn3jQ	Videos shows the Calibration of a small quadruped developed in the Ag Robotics Lab at UMN.																				
Agricultural Robotics Lab	https://www.grasp.upenn.edu/projects/agriculture-robotics/	Yes	No	N/A	US	North America	US	Ground Robot	Agriculture	Data Collection	N/A	Agriculture / Farmland		To provide specialty crop and tree growers with the necessary data for monitoring and planning operations for agriculture.		None	Lab focus on agricultural automation and robotics technology, not climate change.	https://www.youtube.com/watch?v=0o74lGcMhaA   https://www.youtube.com/watch?v=iH8EArj3w5A	Videos shows the GRASP Lab Presents... MEAM 520 Class Breakdown.		https://www.facebook.com/GRASPLab																		
Agricultural Robotics Lab	https://www.agriculturalroboticslab.upv.es/	Yes	No	N/A	Spain	Europe	Spain	Multiple	Agriculture	Data Collection	N/A	Agriculture / Farmland		idea of applying the core ideas of robotics, precision farming to off-road vehicles operating in the environments required by specialty crops, in particular the typical crops grown in the Mediterranean areas.		None	Lab focus on agricultural automation and robotics technology, not climate change.																						
Agricultural Robotics Lab	https://smartrobabcbgu.wixsite.com/iemirl/agricultural-robots	Yes	No	N/A	Isreal	Asia	Israel	Ground Robot	Agriculture	Data Collection	N/A	Extreme / Arid Environments		Develops autonomous ground robots for mechanical weeding, harvesting, and AI-based crop monitoring in arid/semi-arid agricultural environments like the Negev desert.		None	Lab focus on agricultural automation and robotics technology, not climate change.			https://www.linkedin.com/company/wix-com/	https://www.facebook.com/wix https://twitter.com/Wix 																		
Contruction Robotics and Fabrication Tech Lab	https://www.uh.edu/architecture/giving/craftlab/	Yes	No	N/A	US	North America	US	Robotic Arm	Construction	Data Collection	Mitigation	Urban / Built Environment		Our programs foster an environment where ideas find form; where practices that are socially equitable and fundamentally ecological establish a model from which to develop Houston’s future.		None				https://www.linkedin.com/school/uhcoad/	https://www.facebook.com/uhcoad/?epa=SEARCH_BOX																		
Wageningen University & Research Lab	https://visionrobotics.eu/	Yes	No	N/A	Netherlands	Europe	Netherlands  	Multiple	Agriculture	Other	Both	Agriculture / Farmland		Based on our scientific knowledge, we develop gnature-based solutions for spatial design issues.		none		https://www.youtube.com/watch?v=Dgr9weHpHxU  https://www.youtube.com/watch?v=1XZ33LqcJ3s	Videos shows the Biodiversity around wind farms - KennisOnline Magazine 2023 and Kraijenhoff van de Leur Laboratory for Water and Sediment Dynamics	https://www.linkedin.com/company/wageningenenvironmentalresearch/																			
AlphaGarden Lab	https://autolab.berkeley.edu/ 	Yes	No	N/A	US	North America	US	Ground Robot	Agriculture	Data Collection	N/A	Controlled Agriculture / Greenhouse		AlphaGarden is a UC Berkeley research project using a gantry robot to automate polyculture gardening and optimize plant growth		none	More on the plant breeding than robotics.	N/A	N/A																				
Env. Robotics Lab ETH	https://erl.ethz.ch	Yes	No	N/A	Switzerland	Europe	Switzerland 	Multiple	Environment Monitoring 	Data Collection	Both	Extreme / Arid Environments		The Environmental Robotics Lab at ETH Zurich develops bio-inspired robotic systems to monitor, conserve, and sustainably interact with natural ecosystems.		None				https://www.linkedin.com/school/eth-zurich/																			
Fondation Avril (Project)	https://www.fondationavril.org/en/projects/r-stepps/	Yes	No	N/A	France	Europe	Africe	Ground Robot	Land Restoration	Land Restoration	Mitigation	Extreme / Arid Environments		Aims for the development of the robots for the tree planting (digging, planting, watering, and others) in the dry land. tree planing to sequester carbon and preserve biodiversity		none		https://www.youtube.com/watch?v=Nwwy7UEo-uU 	Video shows the softbots that are used in the tree plantation in dry areas.		https://www.facebook.com/fondationavril/																		
Natural Intelligence (Project)	https://www.nih2020.eu/home	Yes	No	N/A	Italy	Europe	Italy	Ground Robot	Environment Monitoring 	Data Collection	Adaptation	Various		Natural Intelligence is an EU‑funded project developing robotic systems for environmental monitoring in varied habitats (dunes, grasslands, forests, alpine) to support biodiversity protection and habitat health assessment.		https://www.nih2020.eu/join		https://www.youtube.com/watch?v=TZi07oVo_jQ 	Video shows the deployment of different robots like legged robot ANYmal for the maintainance of natural habitat.	https://www.linkedin.com/in/natural-intelligence-a3b8a6202/																			
Scottish Marine Robotics Facility  (Research Institute)	https://www.sams.ac.uk/facilities/robotics/	Yes	No	2015	UK	Europe	UK	Multiple	Ocean Data	Ocean Power	Both	Marine / Deep Ocean		Deep-diving robots checking for climate collapse in our oceans.		https://www.sams.ac.uk/vacancies/		https://www.sams.ac.uk/study/careers-and-alumni/	N/A	https://www.linkedin.com/school/samsmarinescience/	https://www.facebook.com/SAMS.Marine																		
LarvalBot (Research Project)	https://research.qut.edu.au/reefresearch/our-research/restoring-our-reefs-and-oceans/	Yes	No	2016	Australia	Oceania	Australia,Philippines 	Ocean Robot	Restoration	Ocean Data	Adaptation	Coastal / Marine Shallow		The semi-autonomous underwater robot disperses heat-tolerant coral larvae onto damaged reefs to accelerate large-scale ecosystem restoration		none		https://www.youtube.com/watch?v=D1qtR2OAVDM	LarvalBot is an autonomous underwater drone designed to restore coral reefs by dispersing millions of baby coral larvae with high precision over degraded areas	https://www.linkedin.com/school/queensland-university-of-technology/	https://www.facebook.com/QUTBrisbane																		
Agrobot	https://www.agrobot.com/	Yes	Yes	2014	Spain	Europe	US,Spain	Ground Robot	Agriculture	Agricultural	N/A	Agriculture / Farmland		Align the new technology and the robots to face the most pressing agriculture issues along with the implementation of traditional farming culture.		none		https://www.youtube.com/watch?v=M3SGScaShhw https://www.youtube.com/watch?app=desktop&v=4Ody1SNv_pk 	Videos shows the Agrobot E-Series Harvesting.	https://www.linkedin.com/company/agrobot/about/																			
Arculus Solutions Inc	https://www.arculus-solutions.com/	Yes	No	2022	US	North America	US	Ground Robot	Asset Inspection	Ground Transport	Mitigation	Industrial / Energy Infrastructure		To future-proof natural gas transmission pipelines to enable safe hydrogen transportation.	SOSV,HAX,Breakthrough Energy	https://www.arculus-solutions.com/jobs		https://www.youtube.com/watch?v=example-arculus	Arculus develops modular robotic systems for construction and infrastructure inspection, enabling precise, safe operations in challenging environments.	https://www.linkedin.com/company/arculus-solutions/about/																			
ARIX Tech	https://www.arix-tech.com/ 	Yes	Yes	2017	US	North America	US,Canada	Ground Robot	Asset Inspection	Asset Inspection	Mitigation	Urban / Built Environment		Pipeline inspection robot - ensures pipelines don't fail, preventing pollution. Robotic inspections and corrosion analytics to improve productivity, safety, accuracy, and data-driven insights for corrosion risk management.	AlleyCorp; Benson Capital Partners; Contour Venture Partners; Tulane Ventures	https://arix-tech.com/careers.html		https://www.youtube.com/watch?v=oKaOG9TUPsg	Video showcases their advanced robotic crawlers integrated with AI-driven data analytics to automate high-risk pipe inspections.	https://www.linkedin.com/company/arix-technologies/																			
Bear Flag Robotics	https://bearflagrobotics.com/	Yes	Yes	2017	US	North America	US	Ground Robot	Agriculture	Agriculture	N/A	Agriculture / Farmland		autonomous equipment directly from their smartphone or tablet, allowing them to realize productivity gains and reduce their operational expenses.	True Ventures; AgFunder; Graphene Ventures; D20 Capital; Green Cow VC.	https://www.bearflagrobotics.com/careers/	Agricultural robotics rather than a climate robotics startup!	https://www.youtube.com/watch?v=Lg1GBkexvwY	Videos shows about the Bear Flag Robotics.	https://www.linkedin.com/company/bear-flag-robotics/																			
Beewise	https://beewise.ag/home	Yes	Yes	2018	US	North America	Israel, USA, Ukraine, Poland, Mexico
	Ground Robot	Biodiversity	Nature Conservation	Adaptation	Agriculture / Farmland		Mission is to stop and reverse the bee-collapse caused by climate change, using precision robotics, AI/ML, and IoT.	Insight Partners; Fortissimo Capital; Corner Ventures; lool Ventures; Atooro Fund; APG Asset Management; Badiya Capital; Marav Mazon Group; Austin Hearst (angel)	https://beewise.ag/careers	Farming	https://www.youtube.com/watch?v=dNEXRobqSfE   https://www.youtube.com/watch?v=mLU3-dRw0pk	Videos shows the introduction to Beewise's Beehome 4	https://www.linkedin.com/company/beewise-technologies/	https://www.facebook.com/beewisetechnologies/																		
BladeBUG Limited	https://bladebug.co.uk/	Yes	Yes	2014	England	Europe	UK,Spain,France	Ground Robot	Wind Turbines	Data Collection	Mitigation	Industrial / Energy Infrastructure		BladeBUG manufactures a six-legged crawling robot that climbs wind turbine blades and uses ultrasonic technology to detect internal structural defects without removing the blade from the turbine.
	True Ventures; AgFunder; Graphene Ventures; D20 Capital; Green Cow VC; Liquid 2; Trucks VC; Y Combinator; and others.	https://www.bladebug.co.uk/jobs/		https://www.youtube.com/watch?v=ENsPz0MvQPE  https://www.youtube.com/watch?v=b1AHM1H5McQ	Videos shows the BladeBUG: using robots to maintain offshore wind farms, robotics inspection, maintenance and repair of wind turbines.	https://www.linkedin.com/company/bladebug/																			
Bloomfield Robotics	https://bloomfield.ai/	Yes	Yes	2019	US	North America	USA, Mexico, Chile, Peru, France
	Ground Robot	Agriculture	Data Collection	Mitigation	Agriculture / Farmland		applies AI and deep learning to complement the work of the crop inspectors by identifying and assessing the same plant characteristics	Kubota; Pax Momentum; Thrive SVG; Oppy; NASA (grant)	https://bloomfieldrobotics.applytojob.com/apply		https://www.youtube.com/watch?v=okMFGAnq1h8	Video shows automatical robot who take camera of plants to monitor them.	https://www.linkedin.com/company/bloomfield-ai/	https://www.instagram.com/bloomfieldrobotics/																		
Blue River Technology	https://bluerivertechnology.com/	Yes	Yes	2011	US	North America	US	Ground Robot	Weeding	Agriculture	Mitigation	Agriculture / Farmland		Create intelligent machinery that solves monumental challenges for our customers.	Khosla Ventures, DCVC, Innovation Endeavors, Pontifax AgTech,Syngenta Ventures, Monsanto Growth Ventures	https://bluerivertechnology.com/join-us/		https://www.youtube.com/watch?v=Rmjg8ML7TiM    https://www.youtube.com/watch?v=XH-EFtTa6IU	Video shows the Life at Blue River, See & Spray - Blue River Technology's precision weed control machine.	https://www.linkedin.com/company/bluerivertech/																			
BlueWhite 	https://www.bluewhite.co/	Yes	Yes	2017	Israel	Asia	US,Isreal	Ground Robot	Agriculture	Farm Irigation	Both	Agriculture / Farmland		BlueWhite manufactures a retrofit kit called Pathfinder that converts ordinary tractors into autonomous self-driving machines, enabling them to perform tasks like spraying, mowing, and discing without human operators.	Insight Partners (lead), Alumni Ventures, LIP Ventures, Entrée Capital, Jesselson, Peregrine Ventures	https://www.bluewhite.co/careers		https://www.youtube.com/watch?v=1POgvgJbBxk     https://www.youtube.com/watch?v=tkVuZUSzekU	Video shows the Bluewhite Autonomous Operation in Fresno California and Bluewhite Autonomy: Autonomous Tractors in Action in Washington's Apple Orchards 	https://www.linkedin.com/company/bluewhite/	https://www.facebook.com/Bluewhiterobotics/																		
Built Robotics	https://www.builtrobotics.com/	Yes	Yes	2016	US	North America	US,Australia	Ground Robot	Construction	Solar Power	Mitigation	Construction / Infrastructure		Built Robotics manufactures autonomous construction equipment, primarily robotic pile drivers for utility-scale solar farms, that install steel foundations for solar panel arrays to accelerate renewable energy infrastructure deployment.
	Tiger Global, Fifth Wall, Building Ventures, Next47, Presidio Ventures, Lemnos, and New Enterprise Associates (NEA). (Tracxn)	https://www.builtrobotics.com/careers/work	Construction work for building the world i.e the evolution of new technology.	https://www.youtube.com/watch?v=drB3-KtpbO4 https://www.youtube.com/watch?v=YYj2JqL1dJM	Shows how technology help in construction work and building the new tools.	https://www.linkedin.com/company/builtrobotics/	https://x.com/builtrobotics   https://www.instagram.com/builtrobotics/ 																		
Carbon Robotics	https://www.carbonrobotics.com/	Yes	Yes	2018	US	North America	US, Canada 	Ground Robot	Weeding	Agriculture	Both	Agriculture / Farmland		Builds the agriclutural tools for improving the efficiency of farmers and develop the spohisticated AI technology based leverages for safer working condition.	Sozo Ventures; Anthos Capital; Fuse Venture Capital; Ignition Partners; Liquid2 Ventures; Voyager Capital	https://carbonrobotics.com/job-openings		https://www.youtube.com/watch?v=vSPhhw-2ShI  https://www.youtube.com/watch?v=AP0yiOI8Qas	Shows how the laser removal of weed is possible and how the use of autonomous weeder to remove weeds.	https://www.linkedin.com/company/carbonrobotics/	https://www.instagram.com/carbon_robotics/ https://x.com/carbon_robotics  https://www.tiktok.com/@carbonrobotics?lang=en  https://www.threads.com/@carbon_robotics 																		
Calvary Robotics	https://calvaryrobotics.com/	Yes	Yes	1994	US	North America	US,Malaysia	Ground Robot	Other	Solar Power	Mitigation	Industrial / Energy Infrastructure		Robots and Modular Designs Lead to Faster and Safer Solar Farm Construction and Maintenance		https://calvaryrobotics.com/careers	It's a  industrial automation rather than climate focus company	https://www.youtube.com/watch?v=nUIE_xToY2U	Video shows designing of mechanical parts of robot.	https://www.linkedin.com/company/calvary-automation-systems/	https://www.facebook.com/CalvaryRobotics/ https://x.com/CalvaryRobotics https://www.instagram.com/calvaryrobotics/ 																		
Charge Robotics	https://chargerobotics.com/	Yes	Yes	2021	US	North America	US	Ground Robot	Construction	Data Collection	Mitigation	Industrial / Energy Infrastructure		Accelerating the transition to renewablesby automating the most labor-intensive parts of construction.	Y Combinator, Climate Capital, UpHonest Capital, E14 Fund, FoundersX Ventures, Gaingels, Hummingbird Ventures.	https://www.ycombinator.com/companies/charge-robotics/jobs		https://www.youtube.com/watch?v=ZZ2fP1Y5Z2E	Video introduces Sunrise, a fully autonomous solar construction system developed by Charge Robotics. 	https://www.linkedin.com/company/charge-robotics/about/																			
CivRobotics	https://www.civrobotics.com/	Yes	Yes	2018	US	North America	US,Canada,Australia	Ground Robot	Construction	Asset Inspection	Mitigation	Construction / Infrastructure		Mark coordinates with precision as fine as 3/100’ (8mm) with CivDot+ and 1/10’ (30mm) with CivDot. Reimagine how coordinates are chosen, captured, and managed.	ff Venture Capital; Alley Robotics Ventures; Trimble Ventures; Bobcat Company; AlleyCorp	https://www.civrobotics.com/careers		https://youtu.be/OfAiJRq6lSc?feature=shared	Video shows Civ Robotics ke ye autonomous robots construction sites par layout aur survey ka kaam insaanon se kahin zyada tezi aur accuracy ke saath khud-ba-khud karte hain.	https://www.linkedin.com/company/civrobotics/	https://www.instagram.com/civrobotics																		
ClearPath Robotics	https://www.clearpathrobotics.com/	Yes	Yes	2009	Canada	North America	Canada 	Ground Robot	Ground Transport	Data Collection	N/A	Construction / Infrastructure		ClearPath Robotics makes autonomous mobile robots that move materials inside factories and warehouses, and also builds unmanned ground vehicles for university research and military use.
	RRE Ventures; iNovia Capital	https://clearpathrobotics.com/robotics-careers/	It's a  industrial automation rather than climate focus company	https://www.youtube.com/watch?v=-rI9wS5NvCc https://www.youtube.com/watch?v=ywQzzSkLZrw	Video shows the development of autonomous robots.	https://www.linkedin.com/company/clearpath-robotics/	https://x.com/clearpathrobots																		
Dusty Robotics	https://www.dustyrobotics.com/	Yes	Yes	2018	US	North America	US	Ground Robot	Construction	Other	Mitigation	Construction / Infrastructure		Dusty Robotics develops robot-powered tools for the modern construction workforce.	Baseline Ventures, NextGen Venture Partners, Canaan Partners, Root Ventures, Scale Venture Partners, Cantos Ventures	https://www.dustyrobotics.com/careers	Primarily construction robotics company rather than a pure climate robotics company	https://www.youtube.com/watch?v=5u3oTObzwaQ   https://www.youtube.com/watch?v=6vu8yvCUNPE	Videos shows the Dusty Robotics FieldPrinter System and its working Mechanism.	https://www.linkedin.com/company/dusty-robotics/	https://www.facebook.com/DustyRobotics																		
EarthForce	https://www.earthforce.io/	Yes	Yes	2022	US	North America	US	Ground Robot	Nature Conservation	Environment Monitoring 	Mitigation	Forests / Silviculture		Develops sensors and utilize them to monitor what is going around those places.	Alley Robotics Ventures (lead), Bold Capital Partners, Third Sphere	none		N/A	N/A	https://www.linkedin.com/company/earth-force-technologies/	https://www.instagram.com/earthforce.io																		
Earth Rover	https://www.earthrover.farm/	Yes	No	2017	England	Europe	UK,Spain	Ground Robot	Agriculture	Data Collection	Both	Agriculture / Farmland		Earth Rover builds autonomous field robotics (CLAWS) that enable farmers to reduce chemical use, improve crop yields, and minimize waste, making fresh, chemical-free produce more accessible and affordable.	Mercia Asset Management; Midlands Engine Investment Fund; Par Equity; MEIF Proof of Concept & Early Stage Fund	https://www.earthrover.farm/about#about-careers		N/A	N/A	https://www.linkedin.com/company/earth-rover/																			
Earthsense	https://www.earthsense.co/	Yes	Yes	2016	US	North America	US,Singapore,Malaysia,Malaysia	Ground Robot	Agriculture	Farm Irigation	Both	Agriculture / Farmland		EarthSense builds autonomous, AI-powered ground robots (e.g. TerraSentia, TerraMax, TerraPreta) to accelerate crop phenotyping, enable regenerative farming practices, reduce chemical/labor inputs, and improve soil health globally.	Innova Memphis; Illinois Ventures; Fox Ventures; The Syndicate Fund” in VCs Invested.	https://www.earthsense.co/careers		https://www.youtube.com/watch?v=1LeuU2GRHhM   https://www.youtube.com/watch?v=saCxFalSPM0	Videos shows the TerraMax - Autonomous Sustainable Plantation Management,TerraPreta - Robotic, Gigaton-Scale, Soil Carbon Sequestration.	https://www.linkedin.com/company/earthsense-inc/	https://x.com/EarthSense_Inc 																		
Easy Floor Robotics	https://www.easyfloorrobotics.com/	Yes	No	2022	Israel	Asia	Isreal	Ground Robot	Construction	Construction	N/A	Urban / Built Environment		Our vision is to develop autonomous robotic technology that transforms the way floors are made.	ExitValley investors	none	Primarily construction robotics company rather than a pure climate robotics company	https://www.youtube.com/watch?v=7mF-K5VcGSw  https://www.youtube.com/watch?v=TxfrHeMiOZs	Videos shows the Robotics and AI for Tomorrow's Floors	https://www.linkedin.com/company/easy-floor-robotics/	https://www.facebook.com/easyfloorrobotics																		
Ecorobotix	https://www.ecorobotix.com/	Yes	Yes	2014	Switzerland	Europe	USA, Canada, New Zealand	Ground Robot	Weeding	Agriculture	Both	Agriculture / Farmland		Precise weeding control through chemicals (micro dose of herbicide) leveraging CV; Solar powered	AQTON Private Equity GmbH; Cibus Capital LLP; Swisscanto Invest / Swisscanto Growth Fund I; Yara Growth Ventures; Flexstone Partners; BASF Venture Capital; Swisscom Ventures; 4FOX Ventures; Verve Ventures	https://ecorobotix.com/en/career/		https://www.youtube.com/watch?v=QsVcJXQrSLo    https://www.youtube.com/watch?v=I-21Jn2rnus	Videos shows the Weed control in an onion field and Biospray Project: Application of Biocontrols with ARA.	https://www.linkedin.com/company/ecorobotix/ 																			
Farm-Ng	https://farm-ng.com	Yes	Yes	2020	US	North America	US	Ground Robot	Agriculture	Data Collection	Mitigation	Agriculture / Farmland		Farm-Ng manufactures modular electric utility vehicles that automate labor-intensive farming tasks while reducing carbon emissions through electrification and supporting regenerative agricultural practices.	Acre Venture Partners; Xplorer Capital; HawkTower	https://farm-ng.com/pages/careers		https://youtu.be/DU8MGAbr1VM?feature=shared	"The Amiga" is a versatile, electric autonomous robot designed to streamline farming by automating tasks like weeding, tilling, and harvesting.	https://www.linkedin.com/company/farm-ng/	https://www.facebook.com/farmnginc																		
Farmdroid	https://farmdroid.com/	Yes	Yes	2018	Denmark	Europe	Denmark,Germany,Netherlands,France,Ireland,UK,Australia,Hungary,Finland,Poland	Ground Robot	Weeding	Agriculture	Mitigation	Agriculture / Farmland		FarmDroid builds solar-powered field robots (FD20) that automatically sow and mechanically weed crops, reducing manual labour, chemical use, and environmental footprint	Convent Capital; EIFO; Navus Ventures	https://farmdroid.com/career/#job-openings		https://www.youtube.com/watch?v=VPOLfW4Fs_0  https://www.youtube.com/watch?v=GcrdmCO4fTo	Videos shows the Reduce the use of chemicals with a field robot.	https://www.linkedin.com/company/farmdroid/	https://www.instagram.com/farmdroid/ https://x.com/DroidFarm 																		
FarmWise	https://farmwise.io/	Yes	Yes	2016	US	North America	US	Ground Robot	Weeding	Agriculture	Mitigation	Agriculture / Farmland		FarmWise develops autonomous, AI-powered mechanical weeding robots for vegetable growers that remove weeds without herbicides, improving crop efficiency, reducing chemical usage, and streamlining farm operations.	Calibrate Ventures; Playground Global; Wilbur-Ellis; SVG Ventures; Fall Line Capital; Middleland Capital; others	https://farmwise.io/careers	More AI than robotics	https://www.youtube.com/watch?v=HqU6O7l8JsM https://www.youtube.com/watch?v=zYurqd7yUYs	Videos shows the Future That Farmers Deserve.	https://www.linkedin.com/company/farmwise/	https://www.instagram.com/farmwiselabs/ https://x.com/FarmWiseLabs 																		
Floating Robotics	https://www.floatingrobotics.com	Yes	No	2023	Switzerland	Europe	Switzerland	Ground Robot	Agriculture	Data Collection	N/A	Controlled Agriculture / Greenhouse		Floating Robotics develops AI-driven greenhouse robots that autonomously harvest crops and perform de-leafing tasks using 3D vision and edge computing.
	Venture Kick,MassChallenge Switzerland,Gebert Rüf Foundation,MassChallenge 	https://www.floatingrobotics.com/careers/		https://www.linkedin.com/posts/floating-robotics_good-news-we-started-our-2023-pilot-last-activity-7108043244659171328-xnpU?utm_source=share&utm_medium=member_desktop 	Video shows the implementation of the robot by floating robotics for the improvement in the picking of the fruit and the leaves.	https://www.linkedin.com/company/floating-robotics/																			
Gravis Robotics	https://gravisrobotics.com/	Yes	Yes	2022	Switzerland	Europe	Germany, Switzerland, France, UK, Austria 	Ground Robot	Construction	Construction	N/A	Terrestrial / Land		Developing autonomy for heavy machinery to automate an industry with a slowly rising productivity and a global labour shortage.	Armada Investment; ESA BIC Switzerland	https://jobs.lever.co/gravisrobotics		https://www.youtube.com/watch?v=yiTIXAAulzI   https://www.youtube.com/watch?v=cyglkr9R9n8	Videos shows the Robotic embankment	https://www.linkedin.com/company/gravisrobotics/	https://www.instagram.com/gravisrobotics/																		
Greenfield Robotics	https://www.greenfieldincorporated.com/	Yes	Yes	2018	US	North America	US	Ground Robot	Weeding	Land Restoration	Mitigation	Agriculture / Farmland		Greenfield Robotics designs and operates autonomous robots that weed, plant cover crops, and manage farms without chemicals, enabling regenerative agriculture and chemical-free food	Cultivate Next (Chipotle’s fund); MKC; ILS; 	none		https://www.youtube.com/watch?v=ymbnlJpPZXE&feature=youtu.be	Video shows the use of robots in removing weeds.	https://www.linkedin.com/company/greenfieldincorporated/	https://www.facebook.com/greenfieldrobotics																		
Harvest Automation Inc	https://www.public.harvestai.com/	Yes	Yes	2008	US	North America	US,Canada	Ground Robot	Agriculture	Weeding	N/A	Agriculture / Farmland		Harvest Automation is a material handling company that develops and manufactures robots to address some of the most challenging issues facing the world.	Cultivian Ventures; Massachusetts Technology Development Corporation; Founder Collective; Entrée Capital; Mousse Partners; MassVentures,	none		https://www.youtube.com/watch?v=S0pQpgrSoDE  https://www.youtube.com/watch?v=lgoNPzPwahs	Videos shows the working mechanism of HV-100 and its daily inspection.	https://www.linkedin.com/company/harvest-automation-inc./about/																			
Jungle Keepers	https://www.junglekeepers.com	Yes	Yes	2023	Peru	South America	Peru	Robotic Arm	Nature Conservation	Land Restoration	Both	Forests / Silviculture		Jungle Keepers focuses on the restoration of the Amazon rainforest using robotic technology to plant seeds and promote ecological conservation		n/a	https://www.euronews.com/next/2023/06/15/conservationists-in-peru-are-turning-to-robots-to-help-reforest-the-amazon	https://www.youtube.com/watch?v=FGAYgxiTNKg 	Videos shows the works done for the plantation of about 600 seeds in the daily context through the use of robots.																				
Kodama Systems	https://kodama.ai/	Yes	No	2021	US	North America	US	Ground Robot	Weeding	Other	Adaptation	Forests / Silviculture		Enables excavators to be used autonomously to clear trees as part of forest mananagement efforts		https://kodama.ai/careers		https://youtu.be/CuhIqw4NNLg?feature=shared	Terry Kodama, the President of the Society of American Foresters (SAF), shares his forestry vision and demonstrates how a professional forester can help transform an ordinary woodland into a superior and more productive tree farm.	https://www.linkedin.com/company/kodama-systems/	https://www.instagram.com/kodama_systems/																		
Korechi Innovations Inc	https://korechi.com/	Yes	Yes	2016	Canada	North America	Canada,US	Ground Robot	Agriculture	Other	Mitigation	Agriculture / Farmland		Korechi develops autonomous robots to automate repetitive tasks in agriculture and golf, including farming (seeding, weeding, transport) and golf range ball‑picking.		https://korechi.com/careers/		https://www.youtube.com/watch?v=MhCrt3hItvg  https://www.youtube.com/watch?v=k-wdbmtRPog	Videos shows the High Capacity Golf Ball Picking Robot.	https://www.linkedin.com/company/korechii/																			
Logiqs	https://www.logiqs.nl/	Yes	Yes	1975	Netherlands	Europe	Netherlands	Ground Robot	Agriculture	Warehouse Automation	N/A	Controlled Agriculture / Greenhouse		 Offer consultation, design, production, and installation of complete logistical systems for greenhouse automation. Vertical farming		https://www.logiqs.nl/jobs/		https://www.youtube.com/watch?v=RT2vTdwFzaw  https://www.youtube.com/watch?v=AUGJbNMMc1U	Videos shows the Warehouse layout design - Logiqs 3D Configurator tool for efficient warehouse operations.	https://www.linkedin.com/company/logiqs-agro_2/	https://www.instagram.com/logiqsbv/ https://x.com/logiqs/ 																		
Luminous Robotics Inc	https://www.luminousrobotics.com/	Yes	Yes	2023	US	North America	Australia 	Multiple	Solar Power	Asset Inspection	Mitigation	Industrial / Energy Infrastructure		Robotic fleets for unlocking scalable solar fields		none		https://www.youtube.com/watch?v=B8rthjTm4K	Video shows the Luminous Fleet to Reimagine the Solar Installation Paradigm.	https://www.linkedin.com/company/luminous-robotics/																			
Naïo Technologies	https://www.naio-technologies.com/en/home/	Yes	Yes	2011	France	Europe	US,France,Europe	Ground Robot	Agriculture	Seaweed Farming	Both	Agriculture / Farmland		Naïo Technologies develops electric autonomous robots for precision weeding to reduce chemical use, ease labor burdens, and promote sustainable agricultural practices	Mirova, Bpifrance, Demeter, WiSEED, Capagro	https://www.naio-technologies.com/en/career/		https://www.youtube.com/watch?v=iykH8Ok2J0U https://www.youtube.com/watch?v=MRDcAyDH3u0 	Video shows how these robots help in better farming and how versatile it is.	https://www.linkedin.com/company/na-o-technologies/																			
Nova Spray Tec	https://www.novaspraytec.com/	Yes	Yes	2020	Germany	Europe	Germany, Switzerland, Netherlands, Spain, Italy, Belgium, USA	Ground Robot	Construction	Construction	N/A	Urban / Built Environment		develop Spraybots to automate manual spray processes in the construction and renovation sector.	"Capagro,Bpifrance,Demeter,NCI Waterstart,Pymwymic,European Innovation Council (EIC)	"	https://www.naio-technologies.com/en/join-naio-technologies/		https://www.youtube.com/watch?v=QRcF6-38Tnk  https://www.youtube.com/watch?v=NNATNFmqmjI	Videos shows the Partnering for Success In the Painting Industry: ARE23 Alliance Perspectives.	https://www.linkedin.com/company/nova-spraytec-gmbh/	https://www.facebook.com/profile.php?id=100054473409434																		
Okibo	https://okibo.com/	Yes	Yes	2018	Germany 	Europe	US	Ground Robot	Construction	Construction	N/A	Construction / Infrastructure		Autonomous robots for use in construction sites. The company’s first product is a robot for wall rendering (e.g., stucco, EIFS, concrete, primer, and adhesives) that will be used to simplify and lower costs of handling wall isolation	BitStone Capital, Shadow Ventures, Built in Tech, Saint Gobain, Pi Labs, DAW	none	Does not have direct climate application	https://www.youtube.com/watch?v=lFBYP_tjaHU  https://www.youtube.com/watch?v=lM5vxIxlodE	Videos shows the Technically speaking about Collaborative robots.	https://www.linkedin.com/company/okibo-ltd/																			
Outrider 	https://www.outrider.ai	Yes	Yes	2017	US	North America	US	Ground Robot	Agriculture	Asset Inspection	Mitigation	Urban / Built Environment		Outrider develops autonomous vehicles to automate logistics operations in freight yards, improving supply chain efficiency and sustainability.	I2BF Global Ventures, Coatue Management	https://jobs.lever.co/outrider		https://www.youtube.com/watch?v=cNrC8Nl3vfE https://www.youtube.com/watch?v=nJ0Wjkiseso 	Video shows how the autonomous system helps in the decreasing supply chain friction and helps the better output works.	https://www.linkedin.com/company/outridertech/	https://www.instagram.com/outridertech/ https://x.com/OutriderTech 																		
PIX Moving	https://www.pixmoving.com/	Yes	Yes	2017	US	North America	China,Japan,US,Spain,Italy,Saudi Arabia,Singapore,Australia	Ground Robot	Ground Transport	Other	Mitigation	Urban / Built Environment		Rebuild the city with autonomous mobility.	TIS, Guizhou Transportation Planning Survey & Design Academe, SOSV.	none		https://www.youtube.com/watch?v=YLSl3iXfbMY	The video showcases the PIX Robobus, an autonomous shuttle, highlighting its functionalities like obstacle avoidance, traffic light recognition, and its sleek design and interior interaction system.	https://www.linkedin.com/company/pixmoving/insights/																			
Q-Bot	https://q-bot.co/	Yes	Yes	2012	England	UK	England, Scotland, Wales, Northern Ireland	Ground Robot	Construction	Asset Inspection	Mitigation	Urban / Built Environment		to transform the built environment with robotics and AI to become a global leader in construction innovation.	EMV Capital, ClearlySo, EcoMachines Ventures, European Union, EIC Fund, Curious Capital, NetScientific,	https://q-bot.co/about/careers/job-listings	Advance in Robotics and AI, 3D mapping.	https://www.youtube.com/watch?v=g6xEV8wIVeM https://www.youtube.com/watch?v=OGahHbR8eSk	Video shows the robot applying under floor insulation using a robotic device.	https://www.linkedin.com/company/q-bot-ltd/																			
Queensland Robotics	https://qldrobo.org	Yes	Yes	2019	Australia	Oceania	Australia	Ground Robot	Construction	Research and development	Mitigation	Construction / Infrastructure		Queensland Robotics’s vision is to be a highly competitive automation and robotics cluster generating tens of billions of dollars per year in domestic and export revenue and creating new jobs across Queensland and Australia.		https://qldrobo.org/who-we-are/opportunities/	Robotics industry cluster/association  specifically promoting Australian robotics industry, bringing together 	https://www.youtube.com/watch?v=t9dJcAXy9J8	N/A		https://www.instagram.com/qldrobo/																		
Raven Industries Inc 	https://www.ravenind.com	Yes	Yes	1956	US	North America	US,Canada ,Switzerland,Netherlands,Belgium,Brazil,Australia,India 	Ground Robot	Agriculture	Seaweed Farming	Mitigation	Agriculture / Farmland		leading precision ag tech innovator, providing solutions that are Helping Farmers Serve the World.		https://jobs.ravenind.com/		https://www.youtube.com/watch?v=RNjE-vslBqo	Videos shows the Raven Industries- Helping Farmers Serve the World.	https://www.linkedin.com/company/raven-industries/	https://www.facebook.com/ravenind/																		
ReMatter AG	https://rematter.earth	Yes	Yes	2022	Switzerland	Europe	Switzerland, Germany 	Ground Robot	Construction	Construction	Mitigation	Industrial / Energy Infrastructure		to create 100% circular, low carbon and equitable buildings by unlocking ingenuity, market knowledge and technology for a healthy built environment.	Venture Kick, MassChallenge, Migros Pioneer Fund.	https://rematter.earth/about-us/#work		https://www.youtube.com/watch?v=CCmpXrTOsc4	ReMatter announces its return as ReMA's 2026 Innovation Partner, powering ReMA2026 and emphasizing their commitment to advancing the recycled materials industry through technology and efficiency	https://www.linkedin.com/company/rematter-earth/	https://www.instagram.com/rematter_earth?igshid=YmMyMTA2M2Y%3D																		
Renovate Robotics 	https://www.renovaterobotics.com	Yes	No	2021	US	North America	US	Ground Robot	Nature Conservation	Environmental Monitoring	Both	Construction / Infrastructure		Safer, Better roofing through brilliant Robotics.	Alley Robotics Ventures, SOSV/HAX, Newlab, Uphonest Capital, Climate Capital,	none		https://www.youtube.com/watch?v=U4DZJZpX678	This video unveils Rufus V1 by Renovate Robotics, a new, lighter, and more efficient robot designed to automate roofing tasks on large projects like multifamily and commercial buildings 	https://www.linkedin.com/company/renovate-robotics/																			
Saga Robotics	https://sagarobotics.com/	Yes	Yes	2016	Norway	Europe	UK,  Norway	Ground Robot	Agriculture	Asset Inspection	Adaptation	Agriculture / Farmland		Develops autonomous agricultural robots (Thorvald) that reduce chemical usage and carbon emissions while increasing yield in specialty crop farming	Praesidium Agri‑FoodTech; Aker; Nysnø Climate Investments; Blystad; Hatteland; MP Pensjon;	https://job-boards.greenhouse.io/scytherobotics		https://www.youtube.com/watch?v=ljvnZH4sKCA https://www.youtube.com/watch?v=qR34__vWCtc 	Videos shows the Thorvald: The helpful robot farmer.	https://www.linkedin.com/company/saga-robotics/	https://www.instagram.com/scytherobotics/ 																		
Scythe Robotics	https://scytherobotics.com	Yes	Yes	2018	US	North America	US	Ground Robot	Agriculture	Solar Power	Mitigation	Industrial / Energy Infrastructure		Builds all‑electric, autonomous commercial mowers to reduce labor and emissions in landscaping, operating reliably in unstructured outdoor environments	True Ventures, Inspired Capital, Zebra Technologies Ventures	https://boards.greenhouse.io/scytherobotics	Automation Machinery	https://www.youtube.com/watch?v=qrS_TfJfXKA https://www.youtube.com/watch?v=wqwDldk2zH8	Videos shows the self-driving, all-electric machine that multiplies commercial landscapers' ability to care for the outdoors.	https://www.linkedin.com/company/scythe-robotics/																			
Searial Cleaners	https://searial-cleaners.com/our-cleaners/bebot-the-beach-cleaner/	Yes	Yes	2021	France	Europe	France, Monaco, Spain, Italy, Greece)	Ground Robot	Recycling/Waste Management	Data Collection	Adaptation	Coastal / Marine Shallow		Develops BeBot, a 100% electric beach‑screening robot that removes buried and surface waste while protecting flora, fauna, and sand on coastal and lake beaches		none		https://www.youtube.com/watch?v=V_C_N4sWiuE   https://www.youtube.com/watch?v=Z_rc86F4-Cg	Videos shows about the searial cleaners, the fixed waste collector.																				
SERAUS 	https://www.seraus.com.au/	Yes	Yes	2022	Australia	Oceania	Australia	Multiple	Solar Power	Inspection	Mitigation	Industrial / Energy Infrastructure		Develops autonomous, waterless solar panel cleaning robots built for remote/harsh solar fields to optimise efficiency and reduce maintenance costs.”		https://www.seraus.com.au/careers				https://www.linkedin.com/company/innovativeenergysolutions/																			
Soltrex	https://soltrex.webflow.io/	Yes	No	2021	Israel	Asia	Israel	Ground Robot	Solar Power	Inspection	Mitigation	Industrial / Energy Infrastructure		robots for solar maintenance, basically clean the solar panel + inspection (visual data on the panel)		none	Keen to take active role in network and summit	https://www.youtube.com/watch?v=3NwEU_1Awok	Soltrex's innovative robot offers an autonomous solution for cleaning solar panels, ensuring maximum performance and efficiency for solar energy plants.	https://www.linkedin.com/company/soltrex/																			
Swap Robotics	https://www.swaprobotics.com/	Yes	Yes	2019	Canada	North America	US,Canada	Ground Robot	Solar Power	Solar Power	Mitigation	Industrial / Energy Infrastructure		Robots for Solar Vegetation Cutting & Snow Removal 	Techstars, SOSV, and Silicon Ranch	https://swaprobotics.bamboohr.com/careers		https://www.youtube.com/watch?v=K7oXhP_H5OM	Swap Robotics offers a 100% electric, autonomous platform designed for year-round utility, including precision vegetation management for solar farms and efficient snow removal.	https://www.linkedin.com/company/swaprobotics/																			
SwarmFarm	https://www.swarmfarm.com/	Yes	Yes	2012	Australia	Oceania	Australia,US	Ground Robot	Agriculture	Weeding	Both	Agriculture / Farmland		Swarm Farming is a new paradigm for agriculture where swarms of small, nimble, autonomous platforms create new farming practices.	Emmertech, GrainInnovate, The Nature Conservancy, Tenacious Ventures, Artesian, and Queensland Government	https://www.swarmfarm.com/team/#careers		https://www.youtube.com/watch?v=WqfA-nlj29s	SwarmFarm Robotics offers a groundbreaking agricultural platform that utilizes autonomous robots to make farming tasks like spraying and mowing more sustainable and efficient.	https://www.linkedin.com/company/swarmfarm-robotics/	https://www.facebook.com/swarmfarm/																		
Terabase Energy - Terafab Robot	https://www.terabase.energy/	Yes	Yes	2019	US	North America	USA	Multiple	Solar Power	Construction	Mitigation	Industrial / Energy Infrastructure		solar deployment automation with on-site robotic factories and software solutions	SoftBank Vision Fund 2, Breakthrough Energy Ventures, Prelude Ventures, Fifth Wall, and SJF Ventures.	https://www.paycomonline.net/v4/ats/web.php/jobs?clientkey=98829736AB5BC6983AC177E5280AC4D6		https://www.youtube.com/watch?v=oj2zdQYXGNE	This video showcases the first commercial deployment of Terabase Energy's Terafab™ automation solution for constructing large-scale solar power plants 	https://www.linkedin.com/company/terabase/	https://www.instagram.com/terabaseenergy/																		
Tertill	https://tertill.com/	Yes	Yes	2015	US	North America	US,Canada,Australia 	Ground Robot	Weeding	Nature Conservation	Mitigation	Agriculture / Farmland		Develops the robots for controlling all season weeds by preventing them to grow with scrubbing wheels and a string trimmer. 	Garage Capital, Husqvarna, and MassChallenge.	none		https://www.youtube.com/watch?v=4HXb4Woqc5I.	Video shows the product description and the use.	https://www.linkedin.com/company/tertill/	https://www.facebook.com/Tertill/																		
Tortuga AgTech	https://www.tortugaagtech.com/what-we-do	Yes	Yes	2016	US	North America	US,UK	Ground Robot	Agriculture	Data Collection	Both	Controlled Agriculture / Greenhouse		build a healthier society, and a thriving ecosystem, through smarter farming.	Lewis & Clark AgriFood,Root Ventures,Spero Ventures,AME Cloud Ventures,Colorado Impact Fund,Remus Capital,Grit Ventures,Morado Ventures,Susa Ventures,THRIVE,	https://www.tortugaagtech.com/careers		https://www.youtube.com/watch?v=l54ZrTj0KPc	Video shows the strawberry plucking robot for easier, effective and efficient harvesting.	https://www.linkedin.com/company/tortuga-agtech/	https://www.instagram.com/oishii.berry https://www.tiktok.com/@oishii.farm https://www.pinterest.com/oishiifarm/ 																		
TTA	https://www.tta.eu/	Yes	Yes	1996	Netherlands,US	Europe,North America	Netherlands ,Australia, Germany,China.	Ground Robot	Agriculture	Weeding	N/A	Controlled Agriculture / Greenhouse		TTA-ISO develops and manufactures advanced high-tech automation equipment, including mobile robots like HarvAI, to handle, select, and harvest plants in controlled indoor farming environments.		https://www.tta.eu/jobs		https://www.youtube.com/watch?v=0DtAeDxb6TY https://www.youtube.com/watch?v=CPgCTJU99ck	Videos shows the solution of indoor farming, and bHarvest by TTA.	https://www.linkedin.com/company/ttabv/																			
Viscon	http://www.viscon.nl/	Yes	Yes	1967	Netherlands	Europe	Netherlands,US,Canada,Australia 	Ground Robot	Agriculture	Land Restoration	Both	Controlled Agriculture / Greenhouse		 Viscon's robotics solutions automate labor-intensive tasks in controlled environments, using autonomous mobile robots (AMRs) for tasks like scouting and logistics, and industrial robots for high-precision picking, sorting, and packaging across the Agro & Food supply chain.	Synergia Capital Partners, Rabo Investments	https://viscongroup.eu/vacatures/?_vacatures_werkenbij=jobs		https://www.youtube.com/watch?v=_TL2U3K44aA https://www.youtube.com/watch?v=XLmHwtKiYzo	Videos shows about the Intelligence software that gives the optimal control and management of your entire logistical process.	https://www.linkedin.com/company/viscon-group/																			
WPS	https://www.wps.eu/	Yes	Yes	1992	Netherlands	Europe	Netherlands,US,Canada,Germany, UK, France, Italy ,China, Japan, Korea, India, Thailand, Philippines, Malaysia, Vietnam Brazil, Argentina, Colombia ,Saudi Arabia, UAE, Egypt, Nigeria, South Africa	Ground Robot	Agriculture	Agriculture	N/A	Controlled Agriculture / Greenhouse		To maximize profits by providing innovative automation systems for greenhouse agriculture."		https://www.wps.eu/nl/werken-bij-wps		https://www.youtube.com/watch?v=Vk-Kt02W_Rw https://www.youtube.com/watch?v=pmNBMQLAxrg	Videos shows the increment growth of farming by using the inovative ideas.	https://www.linkedin.com/company/wps-horti-systems-bv/	https://www.facebook.com/WPSHortisystems																		
X Laboratory 	https://www.deltaxlab.com/offshore-wind/	Yes	Yes	2017	Netherlands	Europe	Germany	Ground Robot	Wind Turbines	Asset Inspection	Mitigation	Marine / Deep Ocean		Enable "highly advanced" mission equipment that allows to install assets faster, safer, more reliable and at lower cost than with current market practices.		https://www.deltaxlab.com/career/		https://www.youtube.com/watch?v=BGQgGIDSv1A	Videos shows the INTERACT Space Experiment Introduction to Science Protocol 2 for Astronauts.	https://www.linkedin.com/company/x-laboratory/?trk=similar-pages_result-card_full-click																			
4Ocean	https://www.4ocean.com/	Yes	Yes	2017	US	North America	US , Indonesia , Guatemala	Ground Robot	Recycling/Waste Management	Recycling/Waste Management	Mitigation	Marine / Deep Ocean		4ocean utilizes specialized remote-controlled and autonomous devices like aquatic drones (Pixie Drone) and beach-cleaning robots (BeBot) to efficiently collect plastic, microplastics, and debris from beaches, rivers, and coastal waters.		https://recruiting.paylocity.com/recruiting/jobs/All/70d8b9a8-65c4-48f4-8af9-f2014dd5cf2d/4Ocean-Public-Benefit-Company		https://www.youtube.com/watch?v=aNSa0jsy_k4   https://www.youtube.com/watch?v=XrHT0P7RgW4	Videos shows the Leading the Marine Sustainability Industry	https://www.linkedin.com/company/4oceanpbc/	https://www.facebook.com/4oceanBracelets/																		
Apeiron Labs	https://www.apeironlabs.com	Yes	Yes	2022	US	North America 	US	Ocean Robot	Ocean Data	Wind Turbines	Both	Marine / Deep Ocean		To meet the critical challenge of scaling upper ocean observing by employing our Tensor platform.	Applied Invention, S2G Ventures, Shorewind Capital 	https://www.apeironlabs.com/careers		N/A	N/A	https://www.linkedin.com/company/apeiron-labs/																			
Benthic Rover	https://www.mbari.org/technology/benthic-rover/	Yes	No	1987	US	North America	US	Ocean Robot	Ocean Data	Data Collection	Both	Marine / Deep Ocean		The Benthic Rover is an autonomous mobile deep-sea laboratory that continuously monitors and measures the deep-sea carbon cycle and ecosystem health on the abyssal seafloor.		https://www.mbari.org/about/careers/job-openings/	Marine Science	https://www.youtube.com/watch?v=ryRcPeOM1sY https://www.youtube.com/watch?v=KOPU6BcV7hU	The description for the linked video should be updated to match the video's focus on the tranquil, sunlit water of the Monterey Bay, or a different video focusing on deep-sea ROVs should be linked.	https://www.linkedin.com/company/monterey-bay-aquarium-research-institute-mbari-/	https://www.instagram.com/mbari_news/ 																		
Blue Ocean Gear	https://www.blueoceangear.com/	Yes	Yes	2015	US	North America 	US, Canada, Jamaica, Belize, Grenada, Australia,	Ocean Robot	Ocean Data	Aquaculture	Both	Marine / Deep Ocean		provides technology solutions for IoT tracking on the ocean.	Good Growth Capital,Conservation International Ventures,NOAA (SBIR Program),Signia Ventures,Boost VC,Sustainable Ocean Alliance (Seabird Ventures),Gratitude Railroad,BDT & MSD Partners,DTN Ventures,Brighter Capital,	none		https://www.youtube.com/watch?v=zu07iiQk0_s	The video is a testimonial and explanation of how the Smart Buoys help fishermen track gear in real-time to promote sustainable fisheries and reduce stress.	https://www.linkedin.com/company/blue-ocean-gear/	https://www.facebook.com/myBlueOceanGear/																		
Blue Robotics	https://bluerobotics.com/	Yes	Yes	2014	US	North America	US, Canada,Brazil,France,Germany,Chile,Australia,Japan	Ocean Robot	Ocean Data	Aquaculture	Adaptation	Marine / Deep Ocean		Makes low-cost, high-performance components for marine robotics to enable the next generation of ocean exploration		https://bluerobotics.com/jobs/	Marine Robotics, Electric Motors.	https://www.youtube.com/watch?v=uugmuZINbW0 https://www.youtube.com/@BlueRobotics	Videos shows the introduction of Blue Robotics and its product overview.	https://www.linkedin.com/company/blue-robotics-inc-/	https://www.instagram.com/bluerobotics 																		
Clear Blue Sea	https://www.clearbluesea.org/fred/	Yes	No	2016	US	North America	US	Ocean Robot	Waste to Energy	Ocean Data	Mitigation	Coastal / Marine Shallow		ensure the survival of the marine ecosystem and the health of the maritime economy by removing macro and microplastic debris to return the marine environment to clear blue.		https://www.clearbluesea.org/join-the-team/		https://www.youtube.com/watch?v=U7Ei68oRIW4	Video shows the recent problems faced by marine environment and the robot FRED that helps to collect the garbage on the water surface.	https://www.linkedin.com/company/clear-blue-sea/	https://www.facebook.com/ClearBlueSeaOrg																		
Clear Robotics	https://www.clearbot.org	Yes	Yes	2019	Hong Kong	Asia	Hong Kong, India, Singapore, Thailand, Philippines 	Ocean Robot	Recycling/Waste Management	Data Collection	Mitigation	Coastal / Marine Shallow		deliver bold ideas and AI-powered technology solutions to resolve complex environmental challenges.	Alibaba Entrepreneurs Fund; Gobi Partners GBA; CarbonX Global	https://www.clearbot.org or LinkedIn	Had starting pains	https://www.youtube.com/watch?v=5hkryfsstr0  https://www.youtube.com/watch?v=3DGp8MbafS0	Videos shows the Solar-Powered Cleanup Solution for Cleaner Waterways, and navigation of Clearbot.	https://www.linkedin.com/company/clearrobotics/	https://www.facebook.com/Clearbot/ 																		
Framework Robotics Gmbh	https://fw-robotics.de/	Yes	No	2020	Germany	Europe	Germany	Ocean Robot	Inspection	Wind Turbines	Adaptation	Marine / Deep Ocean		specializations in marine technology, hydrodynamics, mechanics, electronics and software.	GENIUS Venture Capital; Green Offshore Tech	https://fw-robotics.de/jobs/		N/A	N/A	https://www.linkedin.com/company/fw-robotics/	https://www.instagram.com/framework_robotics/																		
Other lab 	https://www.otherlab.com/	Yes	No	2022	US	North America	US	Ocean Robot	Aquaculture	Seaweed Farming	N/A	Coastal / Water Infrastructure		Develops and implements the anchors for the structured growth of seaweeds and reduce the chance of the young seaweeds getting displaced.		none		https://www.youtube.com/@holdfasttechnologies8435	N/A																				
Hydromea	https://www.hydromea.com/	Yes	Yes	2014	Switzerland	Europe	US,Norway,Germany,France,,Switzerland	Ocean Robot	Ocean Data	Environment Monitoring 	Adaptation	Marine / Deep Ocean		Resolves integrity and environmental data flow challenge below water surface in a vertically-integrated data management platform.	Innosuisse,Eurostars,European Union,Privilège Ventures,SICTIC	https://www.hydromea.com/jobs		https://www.youtube.com/watch?v=_ENS7MS_X8I&feature=youtu.be	Video shows the challenges, smart swarm technologies, subsea connectivity, AI computer vision, applications and benefits regarding the ocean robots they create. 	https://www.linkedin.com/company/hydromea/																			
Icefin	https://schmidt.eas.gatech.edu/icefin/	Yes	Yes	2017	US	North America 	Antarctica	Ocean Robot	Ocean Data	Inspection	Adaptation	Marine / Deep Ocean		Focuses on developing the robots for icy places for making a habitable place in ice-ocean place.		none		https://www.facebook.com/icefinrobot/videos/848085133465056/ 	Video shows the boat developed by Icefin.		https://www.facebook.com/icefinrobot/																		
Impossible Metals 	https://impossiblemetals.com/	Yes	No	2020	US	North America	US,Canada	Ocean Robot	Distributed Energy	Nature Conservation	Mitigation	Marine / Deep Ocean		Sustainable seabed mining... Accelerating clean energy by delivering the most sustainable battery metals	Y Combinator,Justin Hamilton,Climate Capital,Soma Capital,Aureolis Ventures,CapitalX,Chalet Group/Chalet.vc,10X Capital,Gaingels,Liquid 2 Ventures,Microventures,NewGen Venture Partners, Noveus Capital, Palrecha Capital, Park Capital, Pareta Ventures, Quiet Ventures, Rebel Fund, Starlight Ventures, Tango.vc, Zillionize, Futureland Ventures, Climate Collective	https://impossiblemetals.com/join-us/		https://www.youtube.com/watch?v=IGR4VxsOOts 	Jason Gillham, CTO, COO, and co-founder of Impossible Metals, provides an overview of Eureka II's core technology and its potential secondary commercial and scientific applications, emphasizing its selective harvesting capabilities for polymetallic nodules.	https://www.linkedin.com/company/impossible-metals/	https://www.facebook.com/ImpossibleMetalsInc/																		
Jelly Fish Bot	https://www.jellyfishbot.io/en	Yes	Yes	2016	France	Europe	France,US,Japan,Australia,Netherlands,Belgium	Ocean Robot	Recycling/Waste Management	Inspection	Mitigation	Coastal / Marine Shallow		Autonomous surface robots that clean floating waste, oil spills, and algae from marinas, harbors, and waterways using AI-powered navigation and collection systems.	GO CAPITAL,Innovacom,Région Sud Investissement,Abeille Assurances (INCO Ventures),Sud Mer Invest,Impact Océan Capital (GO Capital),	https://www.iadys.com/job/	 Robotique marine.	https://www.youtube.com/watch?v=Fq1G2wpitrg  https://www.youtube.com/watch?v=2GGwDZYoDjY	Vdeos shows the anti-pollution systems user cases with the Jellyfishbot.	https://www.linkedin.com/company/iadys/	https://www.facebook.com/iadysofficial/ https://www.instagram.com/iadysofficial/ 																		
Juice Robotics	https://juicerobotics.com/	Yes	No	2013	US	North America	US	Ocean Robot	Ocean Data	Asset Inspection	Adaptation	Marine / Deep Ocean		Compact UAV-based deep ocean exploration systems that deploy fiber-optic tethers and sensors from small boats or drones for affordable deep-sea research and inspection.		none	Rhode Island	N/A	N/A	https://www.linkedin.com/company/juice-robotics/about/	https://www.instagram.com/juicerobotics																		
LiquidRobotics 	https://www.liquid-robotics.com/wave-glider/how-it-works/	Yes	Yes	2007	US	North America	US; Argentina; Uruguay; United Kingdom (Scotland); Nordic Countries (Norway, Sweden, Denmark, Finland, Iceland); Arctic; Antarctica / Southern Ocean	Ocean Robot	Ocean Data	Ocean Data	Adaptation	Marine / Deep Ocean		designs and manufactures the Wave Glider, the world’s first wave and solar powered uncrewed ocean robot.	Riverwood Capital, VantagePoint Capital Partners, and Schlumberger Technology Investments.	https://jobs.jobvite.com/careers/liquid-robotics-inc/jobs?__jvst=Career%20Site	Ocean Robotics.	The Next Generation Wave Glider	Video shows the working mechanism of wave glider and next generation wave glider.	https://www.linkedin.com/company/liquid-robotics/																			
Mission Robotics	https://www.missionrobotics.us/	Yes	Yes	2020	USA	North America	US,Australia	Ocean Robot	Ocean Data	Wind Turbines	Adaptation	Marine / Deep Ocean		Provides the infrastructure necessary for marine vehicles and instruments, enabling faster time-to-market for new products.		none		https://youtu.be/AJBTuT8Z9VU?si=1imXZn-54eLqZXj0	Video shows the exploration done by company on the depth of the lake Tahoe.	https://www.linkedin.com/company/missionrobotics/	https://x.com/MissionRobotics 																		
Nauticus Robotics	https://nauticusrobotics.com/	Yes	Yes	2014	US	North America 	US	Ocean Robot	Asset Inspection	Data Collection	Mitigation	Marine / Deep Ocean		developer of ocean robots, autonomy software and services delivered to the ocean industries.	Transocean,ATW Partners,Public Markets	https://nauticusrobotics.com/careers/		https://www.youtube.com/watch?v=InqAdyMo4jk&feature=youtu.be	Video shows the ocean robots they have developed and how they are planning for their goal.	https://www.linkedin.com/company/nauticus-robotics-inc/	https://www.facebook.com/NauticusRobotics																		
Neptune Robotics	https://neptune-robotics.com/	Yes	Yes	2018	Hong Kong	Asia	Hong Kong, China, Singapore	Ocean Robot	Recycling/Waste Management	Other	Mitigation	Marine / Deep Ocean		Neptune Robotics uses autonomous underwater robots powered by AI to remove biofouling from ship hulls, reducing drag and cutting fuel consumption.	Sequoia Capital China (HongShan), ClearVue Partners, SOSV's Chinaccelerator	Neptune Robotics | LinkedIn		Neptune Robotic Hull Cleaning in Challenging Waters	Video show the autonomous underwater robotic system removing marine biofouling from commercial hulls.	https://www.linkedin.com/company/neptunerobotics/?viewAsMember=true	Neptune Robotics | Facebook																		
Ocean Infinity	https://oceaninfinity.com	Yes	Yes	2017	US	North America	USA, UK, Norway, France, Australia, India, Canada, Ukraine	Ocean Robot	Ocean Data	Wind Turbines	Adaptation	Marine / Deep Ocean		Deploying robotic technologies to capture ocean data and deliver maritime solutions whilst minimising our environmental footprint.		https://oceaninfinity.com/vacancies/		https://youtu.be/o_75y12ydJE	Video shows the robots they deploy to collect ocean data and how they retrieve them and the operationns they do.	https://www.linkedin.com/company/ocean-infinity-llc/	https://www.facebook.com/OceanInfinityOfficial/																		
OceanOneK (Project)	http://khatib.stanford.edu/ocean-one.html	Yes	No	2014	US	North America	France, Italy 	Ocean Robot	Ocean Data	Other	Adaptation	Marine / Deep Ocean		study coral reefs deep in the Red Sea, far below the comfortable range of human divers.		none		OceanOneK, Stanford’s underwater humanoid robot, swims to new depths	Video shows the implementation of ocean one robot on the deep explorations on oceans and shows the specific characters of the robot.																				
Open Ocean Robotics	https://openoceanrobotics.com/	Yes	Yes	2018	Canada	North America 	Canada, Bahamas, UK, Europe, USA	Ocean Robot	Nature Conservation	Environmental Monitoring	Adaptation	Marine / Deep Ocean		Open Ocean Robotics develops and deploys solar-powered,uncrewed surface (USVs) with real-time analytics to provide safe,sustainable,and persistent ocean data for monitoring, research, and, security.	Rhiza Capital, Antares Ventures, Cindicates, Sustainable Development Technology Canada (SDTC)	https://www.openoceanrobotics.com/careers		https://www.youtube.com/watch?v=w2XmLlFhD2Q https://www.youtube.com/watch?v=5f23r1tEqfI 	Video shows how the robots developed helps in the data collection and providing of the data.	https://www.linkedin.com/company/open-ocean-robotics/	https://www.instagram.com/oceanrobotics/ https://vimeo.com/user96085081  https://x.com/oceanrobotics 																		
Phuc Labs	https://www.phuclabs.com	Yes	Yes	2020	US	North America	US, Philippines	Ocean Robot	Inspection	Nature Conservation	Mitigation	Marine / Deep Ocean		to automate the process of identifying, separating, and reclaiming particles from water.	MCJ Collective, Climate Capital, AI Sprout, Ideaship	none	Hydro- robotics.	https://www.youtube.com/watch?v=Wn6QwgwwAvM  https://www.youtube.com/watch?v=vuHbYo9UMtk	Video shows the detail explanation of Vision Cycle and puchu labs vision. 	https://www.linkedin.com/company/phuclabs	https://x.com/phuclabs?lang=en 																		
PlanBlue 	https://www.planblue.com	Yes	Yes	2017	Germany	Europe	US,Germany 	Ocean Robot	Inspection	Ocean Data	Adaptation	Coastal / Marine Shallow		Uses hyperspectral imaging + AI to map and quantify seafloor health and value, enabling blue‑nature solutions globally.	European Union, EIC Fund, Creative Destruction Lab, Sustainable Ocean Alliance, Mana Impact Partners, Ponderosa Ventures	https://www.planblue.com/join-us	Environmental services.	https://www.youtube.com/watch?v=0IeeIRroNyI	Video shows the mechanism of making process of invisible seafloor visible.	https://www.linkedin.com/company/planblue/	https://www.instagram.com/planblue_hq																		
RangerBot (Project)	https://research.qut.edu.au/qcr/Projects/rangerbot/	Yes	No	2020	Australia	Oceania	Australia	Ocean Robot	Inspection	Ocean Data	Adaptation	Coastal / Marine Shallow		Research diversly and provide solutions addressing the most pressing present and future challenges.		none		https://www.youtube.com/watch?v=nWxPPo64xdE&feature=youtu.be	Video shows the Research and how they develop real world solutions based on them.	https://www.linkedin.com/company/qut-centre-for-robotics/	https://www.facebook.com/QUTScienceandEngineering/																		
Reefgen	https://www.reefgen.io/	Yes	Yes	2020	US 	North America	US,UK,Indonesia,Australia 	Ocean Robot	Seaweed Farming	Environmental Monitoring	Both	Coastal / Marine Shallow		The robotics solution mechanizes and accelerates the planting of heat-resistant corals and seagrasses in marine environments at a global scale.		none	Coral and seagrass planting. Jen cole was a panelist on June 15. pilot deployments since 2021, commercial deployments likely q4 2023. will update when can.	https://www.youtube.com/watch?v=RVo5_ACac8w  https://www.youtube.com/watch?v=FwAVLUoTv74	Videos shows the Reefgen trailer,reefgen Catalina Seagrass Trial.	https://www.linkedin.com/company/reefgensf/about/																			
Row-bot (Project)	https://www.bristol.ac.uk/news/2015/november/row-bot.html	Yes	No	2015	England	Europe	UK	Ocean Robot	Recycling/Waste Management	Data Collection	Mitigation	Coastal / Water Infrastructure		It is an autonomous swimming robot that scavenges its energy from microorganisms in the water using microbial fuel cells (MFCs) to enable indefinite operation in remote locations.		none		https://www.youtube.com/watch?v=KCL8NjN7FMQ	Shows the introduction on the problesm for which the row-bot was created and how the row-bot works.	https://www.google.com/search?q=https://www.linkedin.com/company/bristol-robotics-laboratory/	https://www.facebook.com/bristoluniversity																		
SailDrone	https://www.saildrone.com/	Yes	Yes	2012	US	North America	US	Ocean Robot	Ocean Data	Nature Conservation	Adaptation	Marine / Deep Ocean		Provides comprehensive data solutions for maritime security, ocean mapping, and ocean data.	Bond Capital, Horizons Ventures, Lux Capital, Capricorn, Social Capital, Emerson Collective, and Danmarks Eksport og Investeringsfond.	https://www.saildrone.com/careers/available-jobs	Big data	https://www.youtube.com/watch?v=83FQzfH_r2U	Shows the saildrone operation and its effects.	https://www.linkedin.com/company/saildrone-inc/	https://www.facebook.com/saildrone																		
Samudra Oceans	https://www.samudraoceans.com/	Yes	No	2022	England	Europe	England	Ocean Robot	Ocean Data	Biodiversity	Both	Marine / Deep Ocean		Focuses on using robotics, AI for the further enhancement in the development of seaweed for supporting blue economy, blue carbon and so on.	British Design Fund; Carbon13; Britbots	https://www.samudraoceans.com/careers		N/A	N/A	https://www.linkedin.com/company/samudraoceans/	SamudraOceans | London | Facebook																		
SeaClear (Project)	https://seaclear-project.eu/	Yes	Yes	2020	Netherlands	Europe	Croatia, Germany,Netherlands ,France ,Italy ,Romania ,Turkey ,	Multiple	Recycling/Waste Management	Biodiversity	Adaptation	Coastal / Marine Shallow		A mixed team of unmanned underwater, surface, and aerial vehicles autonomously detects, maps, classifies, and collects litter from the ocean floor..		none	Bottom ocean cleaning	https://www.youtube.com/watch?v=Ao4tMGwKlOw https://www.youtube.com/watch?v=NgfZ1riJjAE	Videos shows the underwater robot observation.	https://www.linkedin.com/company/seaclear-project/	Twitter: @seaclearproject																		
Seaweed Generation	https://www.seaweedgeneration.com/	Yes	Yes	2021	England	Europe	Caribbean, UK	Ocean Robot	Seaweed Farming	Environmental Monitoring	Mitigation	Marine / Deep Ocean		Automated, solar-powered robots (AlgaRay) intercept and sink invasive Sargassum seaweed into the deep ocean for permanent carbon removal (CDR).	Sequoia Capital, Graph Ventures, Aera VC, Climate Capital, Seedrs Crowdfunding, Innovate UK (Grant).	https://www.seaweedgeneration.com/careers.html		https://www.youtube.com/watch?v=sPakJHwalUM 	Shows the plans of the company in removing carbon dioxide production.	https://www.linkedin.com/company/seaweed-generation/	Twitter: @seaweedgen																		
SoFar Ocean	https://www.sofarocean.com	Yes	Yes	2016	US	North America	US, Brazil, Canada, Vanuatu	Ocean Robot	Ocean Data	Wind Turbines	Adaptation	Marine / Deep Ocean		They design, build, and deploy the largest privately owned network of marine weather sensors to create the world's most accurate ocean intelligence and forecasting platform.	True Ventures, Union Square Ventures (USV), Foundry	https://boards.greenhouse.io/sofarocean		https://www.youtube.com/watch?v=My7CTGeEJdI  https://www.youtube.com/watch?v=lSEnQp5I7OM	The video describes the process of collecting ocean data at scale using a global network of marine sensing systems.	https://www.linkedin.com/company/sofar-ocean/	https://www.instagram.com/sofarocean/																		
Teledyne Technologies Incorporated	https://www.teledyne.com/en-us	Yes	Yes	1960	US	North America	US	Ocean Robot	Ocean Data	Environmental Monitoring	N/A	Marine / Deep Ocean		Teledyne's marine robotics are autonomous and remotely operated underwater and surface vehicles that perform sophisticated data collection, surveying, and inspection missions in deep sea, coastal, and river environments.		https://flir.wd1.myworkdayjobs.com/flircareers/jobs	big player since a long time, but their ocean gliders collected a lot of the data used in current climate models, alongside various oceanic buoy programs	https://www.youtube.com/watch?v=4LSWu6lRXEo&t=259s	Shows the technological space exploration.	https://www.linkedin.com/company/teledyne-technologies-incorporated/																			
Terradepth	https://www.terradepth.com/	Yes	No	2018	US	North America	US, Asia Pacific region, (Italy),	Ocean Robot	Ocean Data	Asset Inspection	Adaptation	Marine / Deep Ocean		Building the first holistic virtual picture of the ocean with accurate,high resolution, comprehensive data, collected by our fleet of autonomous submersibles.	Seagate, Giant Ventures, Nimble Ventures.	https://www.terradepth.com/careers	Absolute Ocean.	https://www.youtube.com/watch?v=KdJs-1g-BCA	Videos shows Automatic detection of targets in sonar data with the cloud based platform, Absolute Ocean.	https://www.linkedin.com/company/terradepth/about/																			
UWare Robotics	https://uware.io/	Yes	No	2018	Belgium 	Europe	Spain, Portugal, Belgium.,France 	Ocean Robot	Environmental Monitoring	Asset Inspection	Adaptation	Coastal / Marine Shallow		data-driven engineering solutions for coastal environments.	Semper Amplifi 	none	used for blue economy industries for environmental assessments.	https://www.youtube.com/watch?v=OaUOYNJcpnM https://www.youtube.com/watch?v=VQq5cgyhAsU	Videos shows the autonomous seegrass mapping.	https://www.linkedin.com/company/uware-robotics/?originalSubdomain=be	https://www.facebook.com/uware.io/ Insta https://www.instagram.com/uware_robotics/)																		
RanMarine Technology 	https://www.ranmarine.io/products/wasteshark/	Yes	Yes	2016	Holland	Europe	Netherlands, USA, Canada, UK, Australia, Africa,India,UAE	Ocean Robot	Recycling/Waste Management	Ocean Data	Mitigation	Coastal / Water Infrastructure		This autonomous surface vessel (ASV) removes floating waste, plastic, oil, and harmful biomass from in-shore water bodies while simultaneously collecting environmental data.	Boundary Holding, EIC Fund, European Union, PortXL World Port Innovator.	none		https://www.youtube.com/watch?v=GweRxx8aJig	Shows the use of wasteshark which eats plastics and biomass and save plants.	https://www.linkedin.com/company/ranmarine/	https://www.facebook.com/RanMarineTechnology?_rdc=2&_rdr																		
Alquist 3D	https://www.alquist3d.com/	Yes	No	2021	US	North America	US	Robotic Arm	Construction	Other	Mitigation	Terrestrial construction, not marine		Robotic 3D concrete printers autonomously construct the walls and shell of homes and infrastructure layer-by-layer on-site to reduce cost and time.	Boomerang Catapult, VHDA (Virginia Housing Development Authority)	https://www.indeed.com/cmp/Alquist-3d	3D printing houses with Black Buffalo printers	https://www.youtube.com/watch?v=tmHDHq_ZC3o	Machinery and design.	https://www.linkedin.com/company/alquist/																			
Black Buffalo 3D	https://bb3d.io/	Yes	No	2020	US	North America	US, Saudi Arabia, Trinidad, Tobago, Guyana.	Robotic Arm	Construction	Other	N/A	Urban / Built Environment		leading provider of ICC-ES AC509 approved 3D construction printers and materials that enable our clients to get permits and print structural walls on-demand.		none	3D printers for houses	https://www.youtube.com/watch?v=wWOCeTQi4O8 https://www.youtube.com/watch?v=dM1E3Xlr0uY	Shows the 3D constructions of tiny house.	https://www.linkedin.com/company/black-buffalo-3d-corp/	https://www.facebook.com/blackbuffalo3d/																		
ICON	https://www.iconbuild.com/	Yes	Yes	2018	US	North America	US, Mexico	Robotic Arm	Construction	Construction	Both	Urban / Built Environment		ICON develops advanced 3D printing technologies for sustainable and affordable housing	Oakhouse Partners, Moderne Ventures, Norwest Venture Partners	https://www.iconbuild.com/careers	3D printing houses	https://www.youtube.com/watch?v=k0REJf3rv44  https://www.youtube.com/watch?v=c4X_tT5syCA	Shows the 3D printed house pushing boundary of sustainable architecture.	https://www.linkedin.com/company/icon3dtech/																			
LAYERƎD	"LAYERƎD is where the future of construction takes shape!
Coming from the collaboration of research labs at the ETH Zurich and industry experts, we are developing autonomous robots that are redefining the construction sector. Our novel 3D plaster printing technique merged with state of the art robotic controller will change surface finishing tasks driving the industry towards more efficient, sustainable, and safer construction process. As the construction industry is ripe for innovation, LAYERƎD is leading the change, ensuring that the future of building is not only more efficient but also more humane. Dive into a world where robot and human collaborate and be part of the future of construction with us."							Other			N/A	NA						N/A	N/A																				
NixieDip	https://www.nixiedip.com	Yes	Yes	2020	US	North America	US,Spain	Aerial Robot	Ocean Data	Inspection	Adaptation	Industrial / Energy Infrastructure		N/A		none	Page is not found	https://www.nixiedip.com/  video on their website	N/A																				
Opentrons	https://opentrons.com/	Yes	Yes	2014	US	North America	USA, Spain	Robotic Arm	Research and development	Other	N/A	Laboratory/indoor robotics		Our mission is to provide the scientific community with a common platform to easily share protocols and reproduce each other’s results.	Khosla Ventures, Lerer Hippeau Ventures, Y Combinator.	https://opentrons.com/about/jobs/?p=jobs%2Fviewall	Indoor lab equipment, not environmental	https://www.youtube.com/watch?v=nbHWSAfQsRc https://www.youtube.com/watch?v=rRubXjTmmxs	Videos shows about the Opentrons Flex Temperature Module and Opentrons Flex Heater-Shaker Installation.	https://www.linkedin.com/company/opentrons-labworks-inc./	https://www.instagram.com/opentrons_/																		
Pleobot (Project)	https://www.nature.com/articles/s41598-023-36185-2	Yes	No	N/A	US	North America	US,Maxico	Ocean Robot	Ocean Data	Other	N/A	Coastal / Water Infrastructure		 unique krill-inspired robotic swimming appendage constituting the first platform to study metachronal propulsion comprehensively.		none	Not qualify for climate robotics startup	https://www.youtube.com/watch?v=cHvCpyk7DzY&feature=youtu.be	Shows the prototype of the robot.																				
Pull to Refresh	https://pulltorefresh.earth/	Yes	No	2021	US	North America	US	Ocean Robot	Seaweed Farming	Carbon Removal	Mitigation	Marine / Deep Ocean		develop technology that reverses emissions by gathering and sinking seaweed in the deep sea.		https://jobs.techstars.com/companies/pull-to-refresh	Seaweed sinking	N/A	N/A	https://www.linkedin.com/company/pulltorefresh/about/	https://www.facebook.com/refreshingearth																		
Yara International 	https://www.yara.com/	Yes	Yes	1905	Norway	Europe	Norway	Ocean Robot	Ocean Shipping	Agricultural	Both	Marine / Deep Ocean		The autonomous, all-electric container vessel transports mineral fertilizer on a domestic sea route, replacing thousands of diesel truck journeys and utilizing robotic mooring				The world's first autonomous, zero emission container ship - YouTube	KONGSBERG video showcasing the concept of the world's first zero-emission autonomous ship	https://www.linkedin.com/company/yara/	https://www.facebook.com/yarainternational																		
Aigen	https://www.aigen.io/	Yes	Yes	2020	US	North America	US	Ground Robot	Weeding	Data Collection	Mitigation	Agriculture / Farmland		Autonomous robot that does 1) weeding (through vision + mechanical means) instead of pesticides 2) providing pest & crops monitoring as well 3) runs on renewable (battery with solar on the robot) entirely; prevent uses of pesticide and chemical for weed controls -> mitigation; the crop monitoring in precision agriculture is a piece of climate adaptation	ReGen Ventures, New Enterprise Associates (NEA), Cleveland Avenue, Incite, Susquehanna Private Equity Investments LLLP.	https://jobs.lever.co/aigen/		https://www.youtube.com/watch?v=tGNrOVXd3Es  https://www.youtube.com/watch?v=6zPbJiy437Q	Videos shows the Farmers and Robots" by Zinc Media, in partnership with the World Farmers' Organisation and Aigen.	https://www.linkedin.com/company/aigeninc/																			
AMP Robotics	https://www.amprobotics.com/	Yes	Yes	2015	US	North America	US, Canada, UK, Ireland, Spain, Japan	Robotic Arm	Recycling/Waste Management	Carbon Removal	Mitigation	Waste & Recycling Management		Applying AI and automation to increase recycling rates and economically recover recyclables reclaimed as raw materials for the global supply chain.	Congruent Ventures (Series D lead), Wellington Management, XN (Series B lead), Sequoia Capital, GV (Google Ventures), Valor Equity Partners, Blue Earth Capital, Sidewalk Infrastructure Partners, Tao Capital Partners, Range Ventures, Closed Loop Partners, Microsoft Climate Innovation Fund	https://boards.greenhouse.io/ampsortation	Robotics with machine learning.	https://www.youtube.com/watch?v=MQMxLkXXqro https://www.youtube.com/watch?v=OwYU3hwgoyw	Videos shows the process of solving the recycling process.	https://www.linkedin.com/company/amp-sortation/	https://www.instagram.com/ampsortation/																		
AnyBotics	https://www.anybotics.com/	Yes	Yes	2016	Switzerland	Europe	Switzerland	Ground Robot	Asset Inspection	Carbon Removal	Mitigation	Industrial / Energy Infrastructure		provide dog like robot to inspection operator insights that increase plant uptime, reduce costs, and improve safety by removing workers from hazardous areas.	Walden Catalyst (Series B lead), NGP Capital (Series B lead), Qualcomm Ventures (Series B extension lead), Supernova Invest (Series B extension lead), Bessemer Venture Partners, Aramco Ventures, Swisscom Ventures, Swisscanto Private Equity, TDK Ventures, Nokia-backed NGP Capital	https://jobs.lever.co/anybotics?lever-via=xJxkKyzhZU&lever-social=job_site		https://www.youtube.com/@ANYbotics https://www.youtube.com/watch?v=Hnht7NosBbw	Videos shows the inspection of robots.	https://www.linkedin.com/company/anybotics/	https://x.com/anybotics  https://www.instagram.com/anybotics/ 																		
Automated Architecture	https://automatedarchitecture.io/	Yes	Yes	2016	UK	Europe	Belgium, USA	Robotic Arm	Construction	Carbon Removal	Mitigation	Industrial / Energy Infrastructure		Company that focuses on designing tools and technologies for making new form of hosuing.		https://automatedarchitecture.io/jobs/	Construction company having indirect climate benifits	https://www.youtube.com/watch?v=D9CkYV3XfIM	Overview of company.	https://www.linkedin.com/company/automated-architecture/about/	https://www.instagram.com/auar__ 																		
BladeBug	https://bladebug.co.uk/	Yes	No	2014	England	UK	UK, Portugal 	Ground Robot	Wind Turbines	Asset Inspection	Mitigation	Industrial / Energy Infrastructure		Advanced robots to assist technicians in the inspection and repair of turbine blades, without the need for rope access.	Britbots (VC), Conduit Connect (impact investing)	https://www.bladebug.co.uk/jobs/	Automation and robotics.	https://www.youtube.com/watch?v=Xl8iAe2GRGc https://www.youtube.com/watch?v=N5WSwXUnJK0	Shows the scalable growth of wind energy.	https://www.linkedin.com/company/bladebug/																			
Boston Dynamics	https://www.bostondynamics.com/	Yes	Yes	2012	US	North America	US, UK, Canada, Japan, Norway, Germany, France, Spain, Italy, Switzerland, Australia, New Zealand, Singapore, South Korea, Netherlands, 	Ground Robot	Inspection	Research and development	Both	Industrial / Energy Infrastructure		Help keep workers safer and frees up their time for higher order tasks, making operations more effective.		https://bostondynamics.wd1.myworkdayjobs.com/Boston_Dynamics	Robotics and simulation.	https://www.youtube.com/watch?v=qgHeCfMa39E https://www.youtube.com/watch?v=tF4DML7FIWk	Videos shows the experiment with new behaviors which demonstrate their whole body athletics.	https://www.linkedin.com/company/boston-dynamics/																			
Burro AI	https://burro.ai/	Yes	Yes	2017	US	North America	US, Australia, New Zealand	Ground Robot	Agriculture	Ground Transport	Mitigation	Agriculture / Farmland		help farmers to work more efficiently by developing autonomous robots for labor problems.	Catalyst Investors, TransLink Capital, S2G Ventures, Toyota Ventures, F-Prime Capital, Cibus Capital, ff Venture Capital, Radicle Growth,	https://jobs.lever.co/Burro		https://www.youtube.com/watch?v=PwQZh8-HGyg https://www.youtube.com/watch?v=-KhG8jmviRU 	Videos show Burro's autonomous mobile platforms (like Burro, Verde, Grande) that assist in tasks like harvest and transport.	https://www.linkedin.com/company/augeanrobotics/	https://instagram.com/burro.ai/,																		
CleanRobotics	https://www.cleanrobotics.com/	Yes	Yes	2015	US	North America	US,Australia	Robotic Arm	Recycling/Waste Management		Mitigation	Waste & Recycling Management		The robotics solution, called TrashBot, uses AI and computer vision to automatically identify and sort waste into recycling or landfill bins at the point of disposal.	Melco International Development, HAX, RiverRoad, Undivided Ventures, Climate Capital	CleanRobotics Jobs + Careers - Built In	AI & Robotics.	https://www.youtube.com/watch?v=O7DZcaV6MaI https://www.youtube.com/watch?v=hVhHgxO1dqw	Videos shows the solution to our growing landfill Problem.	https://www.linkedin.com/company/cleanrobotics/	https://www.facebook.com/teamtrashbot																		
Coral Maker	https://coralmaker.org	Yes	No	2022	Austria	Oceania 	Austria,US	Robotic Arm	Biodiversity	Nature Conservation	Adaptation	Coastal / Marine Shallow		The robotics solution uses an AI-guided arm to automate the repetitive task of placing live coral fragments into manufactured stone skeletons, dramatically speeding up the restoration process.		none		https://www.youtube.com/watch?v=fYFAD6YKxlQ	Videos shows the how Coral Maker is saving the world’s coral reefs with Autodesk.		https://www.instagram.com/coralmaker__/																		
Ecoworks	https://ecoworks.tech/	Yes	Yes	2018	Germany	Europe	Germany.	Robotic Arm	Construction		Both	Urban / Built Environment		The company uses AI and industrial robots in partially automated factories to manufacture prefabricated facade and roof elements for rapid net-zero renovation.	World Fund, Haniel, KOMPAS VC, ISAI	none		https://www.youtube.com/watch?v=toFlQvu4Qrk   https://www.youtube.com/watch?v=uxYAE8lPBys	Videos shows the digitale Planung in der seriellen Sanierung | ecoworks.	https://www.linkedin.com/company/ecoworksnetzerobuildings/																			
Env. Robotics Lab WPI (Project)	https://wp.wpi.edu/merlab	Yes	No	N/A	US	North America	US	Robotic Arm	Recycling/Waste Management	Environmental Monitoring	Both	Waste & Recycling Management		The lab develops robotic systems and advanced manipulation techniques, including visual servoing and soft robot control, to solve complex environmental challenges like recycling and disassembling large structures.				https://www.youtube.com/watch?v=6dE7vwYk9O0  https://www.youtube.com/watch?v=1Ws3eOzOpRE	Videos shows the WPI Robotics - Manipulation and Environmental Robotics (MER) Lab.																				
Everest Labs	https://www.everestlabs.ai/	Yes	Yes	2018	US	North America	US,Australia and New Zealand 	Robotic Arm	Recycling/Waste Management	Data Collection	Mitigation	Waste & Recycling Management		to help material recovery facilities (MRFs) operate more efficiently and enabling CPG brands to exceed their recycled content, EPR and ESG goals	TransLink Capital, BioGeneration Ventures, Sierra Ventures.	https://www.everestlabs.ai/careers	AI  and Robotics.	https://www.youtube.com/watch?v=PAMAeTXctCY  https://www.youtube.com/watch?v=IxqCk-Z9A74	Videos shows the demo of Everestlabs, and Aluminum Can AI detection.	https://www.linkedin.com/company/everestlabsai/																			
Flier Systems	https://fliersystems.com/en/	Yes	Yes	1931	Netherland	Europe	US,China	Robotic Arm	Agriculture	Biodiversity	N/A	Controlled Agriculture / Greenhouse		Specialised in mechanisation and automation solutions in the process of developing a young plant for the improvement in efficiency, quality and profitability. automation / efficiency, helps in mitigation (efficiency) and adaptation (higher yield and more resistant to climate change)?		https://fliersystems.com/en/careers		https://www.youtube.com/watch?v=bIRQCr8WkHg https://www.youtube.com/watch?v=1CIcIXE8SXY 	These Relevant videos shows how the Flier System has helped the farmers to gain more efficiency, productivity and many more.	https://www.linkedin.com/company/flier-systems-bv/?originalSubdomain=nl																			
Glacier 	https://endwaste.io/	Yes	Yes	2019	US	North America	US	Robotic Arm	Recycling/Waste Management	Data Collection	Mitigation	Waste & Recycling Management		launching an AI-based sorting robot that is significantly cheaper and more portable than the competition, without sacrificing accuracy.	New Enterprise Associates (NEA), Ecosystem Integrity Fund (EIF), The Climate Pledge Fund.	https://wellfound.com/company/glacier-2/jobs	AI-powered robotics	Innovative Waste Recycling: AI and Robotics with Areeb Malik, Co-founder of Glacier	Video demonstrating the robot's high-speed, precise material picking in a recycling facility.	https://www.linkedin.com/company/endwaste/																			
GrayMatter Robotics 	https://graymatter-robotics.com/	yes	Yes	2019	US	North America	US,Canada,Maxico	Robotic Arm	Construction	Carbon Removal	Mitigation	Industrial/Manufacturing		GrayMatter Robotics provides AI-powered robotic cells (Physical AI) for surface treatment and finishing applications like sanding, grinding, and polishing in high-mix manufacturing environments.	Wellington Management (Series B lead), NGP Capital, Euclidean Capital, Advance Venture Partners, SQN Venture Partners, 3M Ventures, B Capital, Bow Capital, Calibrate Ventures, OCA Ventures, Swift Ventures, In-Q-Tel (IQT)	https://graymatter-robotics.com/careers/	industrial manufacturing automation company 	BetterWay Products' World's First Dual-Arm Autonomous Sanding Cell | GrayMatter Robotics	Video shows Meet Scan&Sand™, GrayMatter Robotics' automated system which empowers BetterWay Products Inc. to handle the marine industry’s challenges. This turnkey solution is a masterclass of innovation and the world’s first dual-armed autonomous robotic sanding cell– a result of combining GMR-AI, GrayMatter’s physics-informed AI, with the functionality of industrial robotics and sensing.	https://www.linkedin.com/company/graymatter-robotics/?viewAsMember=true	https://www.facebook.com/GrayMatterRobotics/																		
Livin Farms	https://www.livinfarms.com/	Yes	Yes	2015	Austria	Europe	Austria,Spain,Germany 	Robotic Arm	Recycling/Waste Management	Carbon Removal	Mitigation	Controlled Agriculture / Greenhouse		The robotic handling system automates the movement and management of Black Soldier Fly larvae trays within the modular Hive PRO factory to efficiently convert organic waste into protein.	HAX (SOSV), EIC Fund, Peter Luerssen, Elevation Investments, K-Startup Grand Challenge.	https://livinfarms.bamboohr.com/careers		https://www.youtube.com/watch?v=prEAhjl6dhU	N/A	https://www.linkedin.com/company/l-i-v-i-n-farms/?originalSubdomain=ca	https://www.instagram.com/livinfarms/																		
Plenty	https://www.plenty.ag/	Yes	Yes	2013	US	North America	US	Robotic Arm	Agriculture	Ground Transport	Mitigation	Controlled Agriculture / Greenhouse		The robotics system autonomously manages the entire plant life cycle, from planting to harvest, using proprietary vertical growing architecture and AI-guided sensors.	 SoftBank Vision Fund, Walmart, DCM.	https://www.plenty.ag/jobs/		https://www.youtube.com/watch?v=clDlTVwWZ1I  https://www.youtube.com/watch?v=fb4xcFw2VMg	Videos shows about the Plenty—Creating the Future of Farming in Compton and the Flavor Farmers: Behind the Scenes at a Plenty Vertical Farm.	https://www.linkedin.com/company/plenty-farms/ 																			
Posh Electric	https://www.poshelectric.com/	Yes	No	2022	US	North America	US	Robotic Arm	Recycling/Waste Management	Distributed Energy	Mitigation	Urban / Built Environment		The robotics system uses computer vision and automated arms to safely and efficiently disassemble end-of-life electric vehicle batteries for reuse and recycling.	Y Combinator, Global Founders Capital, Starling Ventures, UpHonest Capital.	none	Sustainable battery manufacturing.	POSH - Automated Electric Vehicle Battery Recycling #shorts	This start-up uses robotics and AI to create a circular economy for batteries.	https://www.linkedin.com/company/poshelectric/	https://www.instagram.com/poshelectric/																		
R-Zero	https://rzero.com/	Yes	Yes	2020	US	North America	US	Robotic Arm	Other	Biodiversity	N/A	Urban / Built Environment		The mobile disinfection solution uses UV-C light to autonomously neutralize over 99.99% of airborne and surface pathogens in indoor shared spaces.	DBL Partners, Upfront Ventures, World Innovation Lab, Mayo Clinic Ventures.	https://boards.greenhouse.io/rzero	Does not have direct climate application	Meet Arc - R-Zero's Smart, Whole-Room UV-C Disinfection Solution	Meet Arc - R-Zero's Smart, Whole-Room UV-C Disinfection Solution.	https://www.linkedin.com/company/rzerosystems/																			
Red Sea Reef Builders	https://www.redseareefbuilders.com	Yes	No	2023	UK	Asia	Saudi Arabia	Ocean Robot	Restoration	Biodiversity	Adaptation	Coastal / Marine Shallow		The robotic system is used to survey, monitor, and potentially perform precision placement of coral fragments or reef structures to enhance coral growth and survival.		none		Luis Rosa's Red Sea Reefer	A demonstration of an artificial reef environment (Luis Rosa's Red Sea Reefer).	https://www.linkedin.com/company/red-sea-reef-builders/?originalSubdomain=ae																			
Synovate	https://synthotech.com/products/leakvision/	Yes	Yes	2009	UK	Europe	UK	Ground Robot	Asset Inspection	Research and development	Mitigation	Gas Infrastructure		The robotics systems autonomously survey and perform repair/maintenance inside live utility pipelines (gas and water) to prevent leaks and eliminate the need for road excavations.		https://synthotech.com/about/careers/			Videos shows the Madame Web: First trailer for Spider-Man spin-off lands on the... web and  the echo director talks about that Maya Lopez Daredevil fight scene	https://www.linkedin.com/company/synthotech-limited/	https://www.facebook.com/Synthotech																		
The Plantoid (Project)	https://bsr.iit.it/plantoid	Yes	No	2012	Italy	Europe	Italy	Soft Robotics	Agricultural	Environmental Monitoring	Both	Soil / Underground Environment		The system is a plant root-inspired robot that can 'move by growing' to autonomously explore and monitor underground environments by sensing chemical and physical parameters.		IIT Careers Page (implied from Source 3.6)		https://www.youtube.com/watch?v=uXljUmGRLV4   https://www.youtube.com/watch?v=fWfGUOBv1qU	Videos shows the exoskeleton StreamEXO.	https://www.linkedin.com/company/istitutoitalianoditecnologia/	https://www.facebook.com/IITalk/																		
Toggle Robotics	https://toggle.is 
	Yes	Yes	2016	US	North America	US	Robotic Arm	Construction	Research and development	N/A	Industrial / Energy Infrastructure		Develops hardware, software and services for urban infrastructure and renewable projects.	Tribeca Venture Partners, Point72 Ventures, Blackhorn Ventures, Mark Cuban, Tokyu Construction, Alumni Ventures, Global Brain, New York Ventures	https://toggle.is/careers/		https://youtu.be/hswAfq21duk	Shows how the robots can help in building infrastructure.	https://www.linkedin.com/company/toggle-robotics/about/																			
Universe Energy	https://universeenergy.ai	Yes	No	2021	US	North America	US	Robotic Arm	Construction	Recycling/Waste Management	Mitigation	Urban / Built Environment		to make the next billion batteries out of used ones and reverse the need for mining.	Climate Capital, Fifty Years, NP-Hard Ventures, and Voyagers	https://boards.greenhouse.io/universeenergy	disassemble EV batteris with Robots.	N/A	N/A	https://www.linkedin.com/company/universe-energy/																			
Waste Robotics	https://wasterobotic.com/	Yes	Yes	2016	Canada	North America	US,France,UK	Robotic Arm	Recycling/Waste Management	Construction	Mitigation	Deployment Environment		Advanced waste handling processes, and state-of-the-art robotic technologies to more precise & more profitable waste recycling facilities.	Mirova, Fondaction, Sustainable Development Technology Canada, Creative Destruction Lab.	https://wasterobotic.com/careers/		https://www.youtube.com/watch?v=EipXHGNuRcI https://www.youtube.com/watch?v=ox71N078YWs	Videos shows the recycling robots using AI and robots Sorting Construction Demolition Waste with Incredible Skills.	https://www.linkedin.com/company/wasterobotics/?originalSubdomain=ca																			
ZenRobotics	https://zenrobotics.com/	Yes	Yes	2007	Finland	Europe	Finland,US, China, Australia, Italy, Sweden, Denmark, Lithuania,Germany, Japan, Netherlands, Norway, and UK	Robotic Arm	Recycling/Waste Management	Recycling/Waste Management	Mitigation	Waste & Recycling Management		leading supplier of intelligent sorting robots for the waste industry.	Invus, Evergreen Capital, EIC Fund, European Union,	https://terex.wd1.myworkdayjobs.com/terexcareers	Robotics and waste sorting.	https://www.youtube.com/watch?v=gjCpaUHHdMg https://www.youtube.com/watch?v=HxkklR3BNFc  https://www.youtube.com/watch?v=mWmk-9pB30Y	Videos shows the waste sorting with Zenrobotics recycler.	https://www.linkedin.com/company/zenrobotics/?viewAsMember=true	https://www.facebook.com/zenrobotics/ https://www.instagram.com/zenrobotics/ 																		
Zurich River Cleaning (Project)	https://riverclean.ethz.ch/ 	Yes	No	2019	Switzerland	Europe	Switzerland, South Africa	Ocean Robot	Recycling/Waste Management		Mitigation	Coastal / Water Infrastructure		Develop LIVIA for sorting out the waste .		none		https://youtu.be/n_n_B5I7vo0	Shows the LIVIA whle sorting our the waste at zurich river.	https://www.linkedin.com/company/autonomous-river-cleanup-project/	https://www.instagram.com/autonomousrivercleanup/																		
Terran Robotics	https://www.terranrobotics.ai/	Yes	No	2019	US	North America	US,Singapore	Ground Robot	Agriculture	Weeding	Mitigation	Agriculture / Farmland		" Terran uses automation, AI, and robotics to construct sustainable, low-cost homes
 from natural earth materials."	HAX 	none		https://www.youtube.com/watch?v=StjbHvP88NY		https://www.linkedin.com/company/terran-robotics/about/																			
Onsight	https://onsightops.com/	Yes	Yes	2021	US	North America	US	Ground Robot	Asset Inspection	Solar Power	Mitigation	Industrial / Energy Infrastructure		uses Ai visual learning to detect, report, and observe issues and anomalies on Utility Solar Farms. 		https://www.linkedin.com/jobs/search/?currentJobId=3829260889&f_C=77603635&geoId=92000000&origin=COMPANY_PAGE_JOBS_CLUSTER_EXPANSION&originToLandingJobPostings=3829260889		https://youtu.be/8VUl1FoEQaw	Use of Robot to inspect the use of solar sites in remote location.	https://www.linkedin.com/company/onsight-technology/																			
Trovador	https://www.trovador.eu	Yes	No	2023	Portugal	Europe 	Portugal	Ground Robot	Land Restoration	Environmental Monitoring	Mitigation	Forests / Silviculture		The Trovador robotics solution is an Autonomous mobile robot designed to plant saplings on steep, burned, and difficult terrain to revolutionize large-scale ecosystem restoration and reforestation.		None		https://www.youtube.com/watch?v=_9VLnem5zaI	Trovador is an autonomous, all-terrain reforestation robot designed to plant trees in steep and difficult landscapes where manual planting or heavy machinery cannot reach.	https://www.linkedin.com/company/trovador-eu																			
Reframe Systems	https://www.reframe.systems	Yes	Yes	2022	US	North America	US	Robotic Arm	Construction	Solar Power	Mitigation	Industrial / Energy Infrastructure		On a mission to build and retrofit net-zero homes for all, at scale. Modular manufacturing using microfactories built on software-driven workflows, robotics, AI, and augmentation.	VoLo Earth Ventures (Series A co-lead), Eclipse Venture Equity (Series A co-lead), MassMutual, Cubit Capital, Saga Ventures, Nor'easter Ventures, RA Capital Management subsidiary, Eclipse Ventures (seed), Foundamental Ventures (seed)	https://reframesystems.notion.site/reframesystems/Job-Board-b3ef954035834db6a5d52e11436f22a6	construction component manufacturing			https://www.linkedin.com/company/87226595/admin/feed/posts/	https://www.instagram.com/reframe.systems/																		
Windracers	https://www.windracers.com	Yes	Yes	2017	UK	Europe 	UK,Antartica	Aerial Robot	Aviation	Environmental Monitoring	Adaptation	Extreme / Arid Environments		An aerial robot that will help experts to forecast the impacts of climate change by surveying the melting of ice in Antartica.		None	Survelliance of ice melting in the cold regions to forecast the effects due to climste change.	https://youtu.be/pmMfsc26anc	Shows the test done by scientist  in snowdonia regarding the mapping of the regions to know how the climate change is altering Antartica.	https://www.linkedin.com/company/windracers																			
Robocean	https://www.robocean.io/	Yes	No	2020	Scotland	Europe	UK	Ocean Robot	Seaweed Farming	Biodiversity	Mitigation	Marine / Deep Ocean		A robot that helps restore the entire ocean ecosystem with just a touch on the robots to preserve and reforest seaweed in the ocean.		None		https://www.youtube.com/watch?v=5Iv8NONdQc4&feature=youtu.be	Shows the development of subsea robot and the objectives of developing robots.	https://www.linkedin.com/company/robocean/																			
PaintJet	https://paintjet.com/	Yes	Yes	2019	US	North America	USA	Robotic Arm	Construction	Recycling/Waste Management	Mitigation	Urban / Built Environment		address the systemic labor shortage by implementing advanced robotics to paint large scale industrial warehouses, marine ships and wind turbines. 	Dynamo, Pathbreaker Ventures, GRIDS Capital, MetaProp	https://paintjet.breezy.hr/	Industrial painting automation company	https://youtu.be/z6QB6d8E0FA	Shows the use of robots while painting a wall which is much faster than human doing it.	https://www.linkedin.com/company/paintjet/																			
Robotics 88	http://www.robotics88.com/	Yes	Unclear	2021	US	North America	Unclear 					Custom Solutions (including mobile robots, robotic arms)		An engineering design firm focused on developing custom robotics and automation systems for a diverse range of clients		https://www.linkedin.com/company/robotics-88/jobs/		https://www.youtube.com/watch?v=0VNA2almX1E	Videos shows Subcanopy Drone Footage of forest 	https://www.linkedin.com/company/robotics-88/																			
rStream Recycling 	https://www.rstreamrecycling.com/	Yes	No	2020	US	North America	US	Robotic Arm	Recycling/Waste Management	Data Collection	Mitigation	Urban / Built Environment		rStream develops and deploys AI-powered robotic systems to automate the sorting of recyclable materials in waste management facilities.	Massachusetts Technology Collaborative Cleantech Open	https://www.linkedin.com/company/rstream/jobs/		https://www.youtube.com/watch?v=fSPh-GMEsPg	Video related to rStream Recycling, demonstrating their technology.																				
Sunfish Inc	https://www.sunfish.ai	Yes	Yes	2019	US	North America	US,Namibia	Ocean Robot	Inspection	Ocean Data	Adaptation	Coastal / Water Infrastructure		Complex underwater exploration and infrastructure inspection	gener8tor,Creative Destruction Lab,Coho (institutional investor) 			https://www.youtube.com/@sunfishinc4395	Creation of maps for water resource management	https://www.linkedin.com/company/sunfishinc	https://www.instagram.com/sunfish_auv/																		
Rain	https://www.rain.aero 	Yes	No	2019	US	North America	US	Aerial Robot	Aviation	Multiple	Mitigation	Agriculture / Farmland		Rain develops and deploys autonomous aerial vehicles (drones) that rapidly deliver fire retardant to extinguish wildfires in their early stages.	Founders Fund, Good Friends, DBL Partners.	https://www.linkedin.com/company/rain-industries/jobs/		https://www.youtube.com/watch?v=RfeD5bUSnco&t=3s	Rain adapts military and civil autonomous aircraft with the intelligence to perceive, understand, and suppress wildfires. 	https://www.linkedin.com/company/rain-aero/	https://www.instagram.com/rain.aero/																		
Rock-Farm	www.rockfarm.io	Yes	No	2020	Germany	Europe	Germany 	Ground Robot	Construction	Carbon Removal	Both	Agriculture / Farmland		Uses autonomous rovers to precisely spread crushed rock on farmland, enabling scalable carbon removal via Enhanced Rock Weathering		https://www.linkedin.com/company/naska-robotics-gmbh/jobs/	Very unique application!																						
Syrenna	https://www.syrenna.com/	Yes	No	2022	Norway	Europe	Norway	Ocean Robot	Ocean Data	Wind Turbines	Both	Marine / Deep Ocean		Autonomous underwater "WaterDrone" that acts as a semi-stationary ocean monitoring station, vertically profiling from surface to 1,000m depth to collect oceanographic data (temperature, salinity, dissolved oxygen, pH, turbidity, microplastics, currents) for offshore wind, aquaculture, and carbon capture monitoring.	European Regional Development Fund, Investment Bank of State of Brandenburg, State of Brandenburg (Germany)																								
Suffolk	https://www.suffolk.com/	Yes	Yes	1982	US	North America	US	Ground Robot	Construction	Construction	N/A	Urban / Built Environment		Suffolk delivers complex construction projects nationwide using integrated digital platform (Suffolk System) with AI dashboards and advanced project management (no robotics).		https://www.suffolk.com/careers	Suffolk is a construction contractor that USES robotics technology (Boston Dynamics Spot, etc.) but does not manufacture or develop robots. They are a customer/user of robotics, not a robotics company.	https://www.youtube.com/watch?v=rAw2fp-k2Es	Video discussing Suffolk's adoption of AI and robotics to disrupt the construction industry and address labor shortages.	https://www.linkedin.com/company/suffolk/	https://www.facebook.com/SuffolkConstruction/																		
Insight Robotics	https://www.insightrobotics.com/en/	Yes	Yes	2009	Hong Kong	Asia	China,Canada	Multiple	Environment Monitoring 	Data Collection	Mitigation	Forests / Silviculture		Insight Robotics develops autonomous wildfire detection robots and aerial survey drones powered by AI and sensor technologies to enable early fire detection and risk management for forest and plantation owners.	AAIC Ventures, Beyond Ventures, Bright Success Capital,Venture Capital, Transition Level Investments.	https://www.insightrobotics.com/en/careers/		https://www.youtube.com/@insightroboticshk	Videos demonstrating the AI-assisted thermal Wildfire Detection Robot, its operation, and the benefits of early-stage threat detection.	https://www.linkedin.com/company/insight-robotics-ltd/ 	Insight Robotics | Hong Kong Hong Kong | Facebook																		
Menapia 	https://www.menapia.tech/	Yes	Yes	2020	UK	Europe	UK,Netherlands	Aerial Robot	Environmental Monitoring	Research and development	Both	Atmospheric / Aerial		Drones for atmospheric sensing. Automated routine vertical profiles as a service. Custom sensor integration. Research project subcontracting.		https://www.menapia.tech/careers		https://www.youtube.com/watch?v=PZwcnVvUFUE	Videos shows the Automated atmospheric profiling	https://www.linkedin.com/company/menapia-ltd																			
Clean Earth Rovers	https://www.cleanearthrovers.com/	Yes	Yes	2019	US	North America	US	Ocean Robot	Recycling/Waste Management	Ocean Data	Mitigation	Coastal / Marine Shallow		Uses autonomous surface vessels (Rover AVPro) and smart buoys (DataPod) to clean debris and monitor water quality in coastal and near-shore waterways.	Venture Lab (University of Cincinnati), Ocean Visions, various grants			https://www.youtube.com/watch?v=A61VCKd-Iao	Videos demonstrate the Rover AVPro USV autonomously collecting trash, debris, and algae in marinas and harbors in locations like Huntington Harbour. They often compare the robot to a "Roomba for the water.		https://www.instagram.com/cleanearthrovers/																		
Airseas	https://airseas.com/en/	Yes	Yes	2016	France	Europe	France	Ocean Robot	Ocean Power	Distributed Energy	Mitigation	Marine / Deep Ocean		Seawing automated kite system tows commercial ships using wind power, reducing fuel consumption by 20-40%.	Airbus , Kawasaki Kisen Kaisha  , European Union .	https://careers.werecruit.io/fr/airseas		https://www.youtube.com/watch?v=pPclp6fJ4BY	Videos shows "Seawing" automated kite system and its role in achieving the company's 2050 GHG net-zero emissions goal for the shipping industry.	https://www.linkedin.com/company/airseas/	https://www.instagram.com/airseas/																		
Ocean Aero	https://www.oceanaero.com/	Yes	Yes	2012	US	North America	US, Europe, South America, Asia, Africa 	Ocean Robot	Ocean Data	Inspection	Both	Marine / Deep Ocean		TRITON hybrid submarine/surface vehicle enables long-endurance autonomous ocean data collection and surveillance using renewable wind/solar propulsion.	Teledyne Technologies, Lockheed Martin	none		https://www.oceanaero.com	Video shows TRITON AUSV hybrid surface/submerged mission demonstrations.	https://www.linkedin.com/company/ocean-aero 	https://www.facebook.com/OceanAero.US/																		
Hullbot	hullbot.com	Yes	Yes	2017	Australia	Oceania	Australia , USA, Mexico, Singapore	Ocean Robot	Recycling/Waste Management	Asset Inspection	Mitigation	Marine / Deep Ocean		Autonomous robotic hull cleaning reducing fuel and emissions for all vessels.				https://www.youtube.com/watch?v=6b41PYaiYpI		https://www.linkedin.com/company/hullbot																			
Chance Maritime Technologies	chancemaritime.com	Yes	Yes	2022	US	North America	US	Ocean Robot	Ocean Data	Multiple	Adaptation	Marine / Deep Ocean		Long endurance USV platforms designed for modular payloads to collect ocean data, build offshore wind, monitor living marine resources, and more		https://www.linkedin.com/company/chance-maritime-technologies/				https://www.linkedin.com/company/chance-maritime-technologies/																			
Zordi	https://www.zordi.com/	Yes	Yes	2020	US	North America	US	Ground Robot	Agriculture	Carbon Removal	Mitigation	Controlled Environment Agriculture		Zordi builds and operates autonomous greenhouses that integrate mobile robots for precise scouting and harvesting with an AI platform to optimize crop care and yield for crops like strawberries.	Khosla Ventures, Yanmar Holdings (Yanmar Ventures), Shinhan Venture Investment, DSC Investment, Tech Council Ventures.	https://www.zordi.com/careers		https://www.youtube.com/watch?v=4BVDDh0y4f8	Video shows the demonstrations of the scouting robot collecting data and the harvesting robot picking fruit in the greenhouse.	https://www.linkedin.com/company/zordi																			
Reblade ApS	https://reblade.dk/	Yes	Yes	2020	Denmark	Europe 	Denmark,UK,China	Aerial Robot	Wind Turbines	Carbon Removal	Mitigation	Wind Energy Infrastructure		Reblade develops autonomous drone-based repair technology that attaches to wind turbine blades to clean, grind, and coat the leading edge, reducing downtime by 90%.	EIC Fund, European Union (Grants), Offshore Wind Innovation Hub, Greenbackers Investment Capital.	https://join.reblade.dk/		https://www.youtube.com/watch?v=K0LbzcVeCIU	Video shows the demonstration of drone-based robotic modules performing grinding, cleaning, and coating of the leading edge on a turbine blade.	https://www.linkedin.com/company/reblade	https://www.facebook.com/rebladeinnovations																		
Urban Machine	https://urbanmachine.build/	Yes	Yes	2021	US	North America	US,Canada	Robotic Arm	Construction	Carbon Removal	Mitigation	Construction / Infrastructure		The Machine is a robotic system that uses AI and patented end effectors to remove metal fasteners from C&D wood waste, reclaiming high-quality dimensional lumber for reuse in construction.	Lowercarbon Capital (seed round lead) ,GV (Google Ventures) 			https://www.youtube.com/watch?v=_u1Xs0tpmNg	Video shows the Documentary on the company's mission and the robotic process of removing metal fasteners from wood waste.	https://www.linkedin.com/company/urban-machine/																			
Molg AI	https://www.molg.ai/	Yes	Yes	2021	US	North America	US	Robotic Arm	Recycling/Waste Management	Recycling/Waste Management	Mitigation	Waste & Recycling Management		Molg builds AI-powered robotic microfactories that autonomously and non-destructively disassemble complex electronic waste like servers and laptops to recover high-value components for reuse and remanufacturing.	Closed Loop Partners' Ventures Group, Amazon Climate Pledge Fund, ABB Robotics & Automation Ventures, Overture Climate VC, Techstars.	https://www.google.com/search?q=https://www.molg.ai/careers		https://www.youtube.com/watch?v=s1AlWZGKS0M	Video shows how robotics arms assembles E-components	https://www.linkedin.com/company/molg																			
Windbotix	https://windbotix.com/	Yes	Yes	2022	Spain	Europe 	Spain, Portugal,US	Ground Robot	Asset Inspection	Wind Turbines	Mitigation	Industrial / Energy Infrastructure		Windbotix provides robotic systems, like the remotely controlled Nemo, that access the hard-to-reach interiors of wind turbine blades to perform detailed structural inspections, eliminating human risk.				https://www.youtube.com/watch?v=3dz0LLWjI7A	Video shows the demonstration of the NEMO inspection robot's software application for identifying and reporting defects within wind turbine blades.	https://www.linkedin.com/company/windbotix/																			
Borobotics AG	https://www.borobotics.ch/	Yes	No	2023	Switzerland	Europe 	Switzerland	Ground Robot	Construction	Carbon Removal	Mitigation	Urban / Built Environment		Borobotics' "Grabowski" is a compact, autonomous, tube-shaped robot that drills boreholes for geothermal heat pumps, operating efficiently inside the borehole to reduce space, cost, noise, and CO2 emissions.	Underground Ventures (UGV), Kickfund, Bospi AG (Strategic), WSG AG (Strategic), Chris Bach.	https://www.borobotics.ch/careers		https://www.youtube.com/watch?v=AKpdAaqfD1E	Video shows the overview of the company's mission and a visual explanation of how the autonomous "Grabowski" drilling robot works.	https://www.linkedin.com/company/borobotics																			
Tethys Robotics	https://www.tethys-robotics.ch/	Yes	No	2018	Switzerland	Europe 	Switzerland,Germany,Denmark,UAE	Ocean Robot	Inspection	Wind Turbines	Adaptation	Coastal / Water Infrastructure		Tethys Robotics develops the compact, hybrid Tethys ONE underwater drone that uses advanced sensor fusion and autonomy to perform safe, precise, and reproducible inspections and mapping in harsh, low-visibility aquatic environments, eliminating the need for human divers	MassChallenge, Kickfund, and Venture Kick	https://www.tethys-robotics.ch/company/jobs		https://vimeo.com/1071025804?fl=pl&fe=sh	Video discussing how the Tethys robot replaces human divers in hazardous, low-visibility underwater operations	https://www.linkedin.com/company/tethys-robotics/	https://www.instagram.com/TethysRobotics/																		
Cłapa	https://www.floormaster.eu//	Yes	Yes	1994	Poland	Europe 	Netherlands, UK, Ireland	Ground Robot	Construction	Other	N/A	Construction / Infrastructure		The Floor Master is a compact, laser-guided automatic screeding robot that levels and compacts semi-dry floor mixes with high precision, increasing floor quality and efficiency while reducing manual labor and occupational injury risk			Floor Master have indirectly climate effects 	https://www.youtube.com/watch?v=akP2dKBd2HE	Video showing the Floor Master 130 automatic screeding robot in operation on a large floor area, demonstrating efficiency and precision		https://www.facebook.com/clapafloormaster/																		
WildDrone (Project)	https://wilddrone.eu/	Yes	No	2023	Denmark	Europe 	Denmark ,Germany, Switzerland, Netherlands, Kenya,	Aerial Robot	Nature Conservation	Environment Monitoring 	Adaptation	Terrestrial / Agricultural		Correction: WildDrone is an interdisciplinary network training doctoral candidates to develop autonomous drone and computer vision systems that safely and effectively monitor wildlife populations, track animal behavior, and mitigate human-wildlife conflict		https://www.sdu.dk/en/forskning/sduuascenter/researchareas/interdisciplinary-research-in-drones-for-nature-conservation		https://www.youtube.com/watch?v=T2aal3u5F5k	Video shows the presentation on the use of thermal drones for the non-invasive monitoring and tracking of cetaceans (whales/dolphins)	https://www.linkedin.com/showcase/wilddrone/	https://www.instagram.com/wilddrone.eu/																		
AMSL Aero	https://www.amslaero.com/	Yes	No	2017	Australia	Oceania	Australia,New Zealand	Aerial Robot	Aviation	Carbon Removal	Mitigation	Atmospheric / Aerial		AMSL Aero develops Vertiia, a highly efficient, long-range hydrogen-electric eVTOL aircraft designed to take off and land vertically but fly fast like a plane, providing zero-emission air transport for aeromedical, passenger, and cargo services	IP Group Australia, St Baker Energy Innovation Fund (StBEIF), TelstraSuper, Hostplus	https://www.amslaero.com/careers		https://www.youtube.com/watch?v=n5oMT_XQegQ	Video highlighting the Vertiia's first free flight, zero emissions, and long range, positioning it as a leader in Urban Air Mobility	https://www.linkedin.com/company/amslaero/																			
Rosenxt 	https://www.rosenxt.com/	Yes	Yes	2023	Switzerland	Europe 	Switzerland,Germany,Netherlands,Canada,US,Vietnam	Multiple	Inspection	Asset Inspection	Adaptation	Marine / Deep Ocean		Vaarst provides AI-driven computer vision and autonomy software (like SubSLAM X2) that gives subsea robots spatial awareness and enables real-time 3D data collection for offshore asset management.	Legal & General, Future Planet Capital, SDF, Equinor Ventures, Foresight Group Holdings, In-Q-Tel			https://www.youtube.com/watch?v=XN1hihHL-DQ 	The video, titled "We are Rosenxt," briefly introduces Rosenxt as visionary architects with decades of engineering excellence.		https://www.instagram.com/rosen_nxt/ 																		
Solskin	https://www.solskin.swiss/en	Yes	Yes	2022	Switzerland	Europe 	Switzerland	Robotic Arm	Solar Power	Distributed Energy	Mitigation	Urban / Built Environment		Solskin provides AI-driven software and materials for adaptive solar coatings to optimize energy generation and efficiency on building facades.	Venture Kick	https://www.solskin.swiss/en/karriere		https://www.youtube.com/watch?v=SjuK7CKvo6Y&t=137s	Video show about the innovtive future ini solar energy panels by rotating it 	https://www.linkedin.com/company/zurich-soft-robotics	https://www.instagram.com/solskin.swiss/																		
Aquaai	https://www.aquaai.com/	Yes	Yes	2014	US	North America	Norway,US	Ocean Robot	Aquaculture	Recycling/Waste Management	Mitigation	Marine / Deep Ocean		Aquaai uses biomimicry and AI to deploy fish-like robotic platforms (AUVs) that collect real-time visual and environmental data for affordable water monitoring and risk management in marine and freshwater environments.	Boost VC, Backstage Capital, GrowthX, Kvarøy Fiskeoppdrett AS (Strategic Angel), Bart Ziegler	https://www.aquaai.com/careers		https://www.youtube.com/watch?v=UI3mxWF1Vz8	Video shows robotic fish Nammu has a new "skin" plus her data gathering skills are improving.	https://www.linkedin.com/company/aquaai-corp/	https://www.facebook.com/Aquaai/																		
Harvest CROO Robotics	 https://www.harvestcroorobotics.com/	Yes	Yes	2013	US	North America	US	Ground Robot	Agriculture	Data Collection	N/A	Agriculture / Farmland		Harvest CROO Robotics uses a large autonomous vehicle equipped with multiple AI-driven robotic arms and vision systems to fully automate the harvesting, inspection, and packing of ripe strawberries in the field.	Driscoll's, Naturipe Farms, Sonoco, Wishnatzki, National Science Foundation, America's Seed Fund	https://www.harvestcroorobotics.com/careers		https://www.youtube.com/watch?v=BuidOS_p3JI	Video shows that automate harvasting of strawberry 	https://www.linkedin.com/company/harvest-croo-robotics																			
Baubot	https://www.baubot.com/	Yes	Yes	2017	Austria	Europe 	Austria	Ground Robot	Construction	Other	N/A	Construction / Infrastructure		The Baubot is a mobile, multi-functional robotic system designed to autonomously perform high-precision tasks like drilling, fastening, and 3D printing on dynamic construction sites.	INiTS Universitäres Gründerservice ,fischer group (strategic partner/acquirer) 		Physical autonomous ground robots (construction automation)	https://www.youtube.com/watch?v=x_1vFcUxUaw	Video show the robot doing construction with accuracy in a tunnel	https://www.linkedin.com/company/baubot	https://www.instagram.com/baubot_gmbh/																		
Apis Cor	https://apis-cor.com/	Yes	Yes	2016	US	North America	USA, UAE 	Robotic Arm	Construction	Construction	N/A	Construction / Infrastructure		Apis Cor develops and leases a mobile, crane-like 3D printing robotic system (Frank) to autonomously extrude concrete walls for homes and commercial buildings directly on-site, rapidly and affordably.	Alchemist Accelerator, At One Ventures, D.R. Horton (Strategic Investment), JKS Ventures	https://www.apis-cor.com/team		https://www.youtube.com/watch?v=JqiMjw1GUL4	Videos showcase the Frank robot's on-site setup and autonomous 3D printing of durable, concrete-like walls.	https://www.linkedin.com/company/apis-cor	https://www.instagram.com/apiscor/																		
Monarch Tractor	https://www.monarchtractor.com/	Yes	Yes	2018	US	North America	US	Ground Robot	Agriculture	Carbon Removal	Mitigation	Agriculture / Farmland		Monarch Tractor produces the MK-V, a fully electric, driver-optional smart tractor that performs common farming operations while collecting data to improve efficiency and sustainability.	Astanor Ventures, CNH Industrial, Musashi Seimitsu Industry, At One Ventures, Trimble Ventures	https://www.monarchtractor.com/job-openings		https://www.youtube.com/watch?v=PsNixijMRX4	Video shows the misson and technology with CEO Pareveen Penmetsa	https://www.linkedin.com/company/monarch-tractor/	https://www.facebook.com/monarchtractor																		
Re-agRE.tech	https://www.agre.tech/	Yes	Yes	2019	Israel	Asia	Isreal	Ground Robot	Agriculture		Mitigation	Agriculture / Farmland		The agRE.tech A²PV system is a robotic operating system infrastructure that uses AI to autonomously perform crop maintenance tasks and solar panel upkeep in agrivoltaic (solar + agriculture) farms.	EDF Renewable Energy, Zemach Regional Enterprises, Environmental Sustainability Innovation Lab	https://www.agre.tech/		https://www.agre.tech/	Video showcasing the Autonomous-Agri-Photovoltaic (A²PV) Robotic Farm Operating System Infrastructure and its capabilities in crop maintenance and solar panel cleaning.	https://www.linkedin.com/company/agretech/?lipi=urn%3Ali%3Apage%3Ad_flagship3_search_srp_all%3BfaVt3MfEQK6axRrNBztB%2BQ%3D%3D																			
OSHEN 	https://www.oshendata.com/	Yes	Yes	2022	UK	Europe 	UK,US	Ocean Robot	Ocean Data	Inspection	Adaptation	Marine / Deep Ocean		Oshen develops and deploys constellations of low-cost, wind-propelled autonomous surface vehicles (C-Stars) to collect persistent, wide-area oceanographic and climate data for research and forecasting.		https://www.oshendata.com/careers		https://www.youtube.com/watch?v=DhFFAky2ylk	Interview discussing Oshen's low-cost, autonomous micro-vessels (C-Stars) for remote ocean sensing and monitoring of marine mammals and environmental data.	https://uk.linkedin.com/company/oshendata	https://x.com/oshensail 																		
Silana 	https://www.silana.com/	Yes	No	2022	Austria	Europe 	US,Austria	Robotic Arm	Other	Carbon Removal	Mitigation	Industrial/Manufacturing		Silana builds fully automated robotic sewing systems (micro-factories) that perform the entire garment production process to enable fast, ethical, and sustainable on-demand production closer to market.	SOSV, HAX, Material V, OÖ HightechFonds, Alexander Weber (Angel)	https://www.silana.com/team		https://www.youtube.com/watch?v=nt3E-GiGIeQ	Interview with Silana co-founder discussing the challenges of textile automation.	https://www.linkedin.com/company/silana/																			
Cosmic Robotics 	https://www.cosmicrobotics.com/	Yes	Yes	2023	US	North America	US	Multiple	Asset Inspection	Recycling/Waste Management	N/A	Extreme / Arid Environments		Cosmic Robotics' Cosmic-1A is an autonomous, all-electric mobile manipulation robot that autonomously picks up and installs large solar panels directly onto racking at utility-scale solar farms.	Giant Ventures (Lead), MaC Venture Capital, HCVC, Azeem Azhar (Angel), Aarthi Ramamurthy (Angel), Nate Williams (Angel)	https://www.cosmicrobotics.com/careers	NO direct climate focus  primary applications are nuclear and space, not climate	https://www.youtube.com/watch?v=RP49p73VHk0	Video interview with co-founders Lewis Jones and James Emerick discussing their vision for using AI-powered robotics to overcome labor shortages and accelerate the construction of solar infrastructure.	https://www.linkedin.com/company/cosmic-robotics																			
Twisted fields	https://www.twistedfields.com/	Yes	No	2019	US	North America	US	Ground Robot	Agriculture	Carbon Removal	Mitigation	Agriculture / Farmland		Twisted Fields develops the open-source, solar-powered Acorn Precision Farming Rover, an autonomous ground vehicle designed to perform light-duty cultivation, planting, and weeding tasks for small and medium-sized regenerative farms.		https://www.twistedfields.com/careers		https://www.youtube.com/watch?v=NsyEIgKVM5E	Videos showcase status updates, design, and field testing of the open-source Acorn Precision Farming Rover, alongside educational content on regenerative agriculture.	https://www.linkedin.com/company/twistedfields	https://www.facebook.com/twistedfields																		
Greenfield Robotics	https://www.greenfieldrobotics.com/	Yes	Yes	2017	US	North America	US	Ground Robot	Weeding	Carbon Removal	Mitigation	Agriculture / Farmland		Greenfield Robotics deploys fleets of autonomous, all-electric robots (BOTONY™) that use machine vision and AI to eliminate weeds by cutting them and performing nutrient microspraying, enabling chemical-free, regenerative farming.	Kauffman Seeds, NIKOLIMAX, Innovative Livestock Services, Outlaw Ventures	CAREERS - GREENFIELD ROBOTICS				https://www.linkedin.com/company/greenfieldrobotics	https://www.facebook.com/greenfieldrobotics																		
Zurich Soft Robotics (Solskin)	https://www.solskin.swiss/	Yes	Yes	2022	Switzerland	Europe 	Switzerland 	Robotic Arm	Solar Power	Distributed Energy	Mitigation	Urban / Built Environment		Solskin is an AI-optimized, soft-robotic building facade system that dynamically adjusts solar panels to maximize energy generation and regulate indoor climate.	Venture Kick, Stadtwerk Winterthur, Undisclosed Corporate Investor	https://www.solskin.swiss/en/karriere		https://www.youtube.com/watch?v=QeR3SNoKVG4	Demonstration of the Solskin adaptive solar facade system winning the Watt d'Or 2023 energy prize.	https://www.linkedin.com/company/zurich-soft-robotics	https://www.instagram.com/solskin.swiss/																		
Ripe Robotics	riperobotics.com	Yes	Yes	2019	Australia	Oceania	Australia	Ground Robot	Agriculture	Data Collection	N/A	Agriculture / Farmland		Ripe Robotics develops autonomous ground robots that use AI vision and vacuum grippers to harvest apples and stone fruit while collecting crop data.	Startmate, AfterWork Ventures, INCUBATE	https://www.riperobotics.com/#careers		https://www.youtube.com/watch?v=_fDO0qMNQKc	Field trials of the "Eve" apple harvesting robot demonstrating autonomous navigation and picking.	https://au.linkedin.com/company/riperobotics	https://www.facebook.com/riperobotics/																		
The Searial Cleaners	https://searial-cleaners.com/	Yes	Yes	2021	France	Europe 	France, United States	Multiple	Recycling/Waste Management	Data Collection	Mitigation	Coastal / Water Infrastructure		The Searial Cleaners provides a range of robotic, drone, and fixed technologies to collect plastic and other debris from beaches, lakes, rivers, harbors, and shorelines worldwide.				https://www.youtube.com/watch?v=s5fXW-Ga9rU	Demonstrations of the BeBot cleaning beaches and the PixieDrone collecting surface waste in marinas/harbors.	https://www.linkedin.com/company/the-searial-cleaners/	https://www.facebook.com/searialcleaners#																		
Squishy Robotics	https://www.hmpgloballearningnetwork.com/site/emsworld/feature-story/squishy-robotics-delivers-innovative-solutions-sky	Yes	Yes	2018	US	North America	US	Aerial Robot	Environmental Monitoring	Other	Adaptation	Urban / Industrial , Wildfire , Rough Terrain		Squishy Robotics develops air-deployable, impact-resistant tensegrity sensor robots that provide first responders and military and industrial users with real-time, ground-level situational awareness data from hazardous and inaccessible areas.		https://squishy-robotics.com/careers/		https://www.youtube.com/channel/UCeNICgWSXmyyZUYlL_dPltg	Demonstrations of the tensegrity robots being air-dropped from drones/helicopters and surviving the impact, providing real-time HazMat/gas data to first responders.	https://www.linkedin.com/company/squishy-robotics																			
Terradepth	https://www.terradepth.com/	Yes	No	2018	US	North America	US	Ocean Robot	Ocean Data	Environmental Monitoring	Adaptation	Marine / Deep Ocean		Terradepth builds and operates fleets of long-endurance, autonomous underwater vehicles (AUVs) to collect high-resolution ocean data and integrates this data into its cloud-native platform, Absolute Ocean, for commercial and defense decision-making.	Giant Ventures, IPO CLUB, Mantaray Investments, AWS Startups, Capital Innovators, Seagate Technology	https://www.terradepth.com/careers/		https://www.youtube.com/watch?v=cxAmMzE-ZzE	Andrew Lunstad, CTO, discusses Terradepth's mission to improve ocean decision-making, the use of AUVs, the Absolute Ocean platform, and applications in offshore energy and defense.	https://www.linkedin.com/company/terradepth	https://www.instagram.com/terradepth/																		
3Farmate Robotics	https://www.3farmate.com/	Yes	Yes	2021	Ghana	Afria	Ghana	Ground Robot	Agriculture	Solar Power	Mitigation	Agriculture / Farmland		3Farmate Robotics uses AI and autonomous robots to provide cost-effective, climate-friendly agri-automation solutions, including planting and fertilizing, to boost productivity for African farmers.				https://www.youtube.com/watch?v=HblPurjcKH8	Video shows First prototype demonstration of our agricultural robot (FAMA), for autonomous seed planting and fertilizer application.	https://www.linkedin.com/company/3farmate-robotics/																			
BurnBot	https://burnbot.com/	Yes	Yes	2020	US	North America	US	Ground Robot	Other	Carbon Removal	Mitigation	Wildland-Urban Interface , Managed Forest 		BurnBot develops and operates specialized ground-mobile masticators and aerial drone systems to perform safe, scalable, and ecologically precise fuel reduction and prescribed burning operations, dramatically accelerating wildfire prevention efforts.	ReGen Ventures, Toyota Ventures, American Family Ventures, Convective Capital, Blue Forest Asset Management, DCVC, Hawktail	https://burnbot.com/contact/		https://www.youtube.com/watch?v=q9rEOMN_P5o	Demonstrations of the BurnBot RX2 controlled-burn machine creating firebreaks and performing prescribed burns safely in a contained chamber; or the Masticator clearing heavy brush on steep terrain.	https://www.linkedin.com/company/burnbot-inc/	https://www.instagram.com/burnbot.rx/																		
Reclamation Factory	https://www.thereclamationfactory.com/	Yes	No	2023	US	North America	US	Ground Robot	Recycling/Waste Management	Recycling/Waste Management	Mitigation	Urban / Built Environment		The Reclamation Factory uses intelligent, modular robotic and automation systems paired with advanced acoustic and machine learning sensing to efficiently and accurately identify, sort, and prepare low-value plastic waste into high-value feedstock for a true circular economy.	Robotics Factory's Accelerate Program 			https://www.youtube.com/watch?v=NSPaJMmVSXQ	Video pitch explaining how the company uses robotics and automation to improve plastic recycling economics and create infrastructure for a cleaner, smarter supply chain.	https://www.linkedin.com/company/reclamation-factory																			
Lab of Sustainability Robotics 	https://www.epfl.ch/en/	Yes	No	2018	Switzerland	Europe 	Switzerland ,UK	Multiple	Environmental Monitoring	Construction	Both	Urban / Built Environment		Research lab developing sustainable robotic systems for environmental monitoring and infrastructure in support of climate and ecosystem resilience.				https://www.youtube.com/watch?v=sje50ezhfew	Videos showcase the development and testing of bio-inspired drones for aerial construction (Aerial Additive Manufacturing) and environmental monitoring.	EPFL | LinkedIn	https://www.instagram.com/epflcampus/																		
TeknTrash	https://www.tekntrash.com	Yes	Yes	2019	UK	Europe 	UK	Ground Robot	Recycling/Waste Management	Data Collection	Mitigation	Urban / Built Environment		Robots automate waste sorting and trash handling in recycling facilities while capturing detailed waste data for operational and sustainability insights.				https://www.youtube.com/watch?v=Wj7C6zTeyu0	Videos demonstrate humanoid and robotic systems sorting waste on conveyor belts and operating in live recycling and disposal plants.	https://www.linkedin.com/company/tekntrash/	https://www.facebook.com/people/TeknTrash-Robotics/61575183834204/																		
FarmRobo Technologies 	https://www.farmrobo.in	Yes	Yes	2020	India	Asia	India	Ground Robot	Agricultural	Farm Irigation	Adaptation	Controlled Agriculture / Greenhouse		FarmRobo’s autonomous field robots handle weeding, spraying, load carrying, and crop monitoring while streaming real‑time data to make farming more efficient and less labor‑intensive.		https://www.farmrobo.in/career		https://www.youtube.com/watch?v=LaaHmlBlcwk	Videos demonstrate FarmRobo’s agricultural robots performing tasks such as spraying, intercultivation, and load carrying in real farm conditions.	https://www.linkedin.com/company/farmrobo-technologies-pvt-ltd	FarmRobo | Facebook																		
Applied Carbon	https://www.appliedcarbon.com/	Yes	No	2020	US	North America 	US	Ground Robot	Agriculture	Carbon Removal	Mitigation	Agriculture / Farmland		Builds mobile pyrolysis units converting plant waste into biochar to sequester CO .
	TO VC,Congruent Ventures, Grantham Foundation, Anglo American	https://apply.workable.com/appliedcarbon/		https://www.youtube.com/watch?v=O5k2I0pSAJ4	Video shows Demonstrating the Applied Carbon Mobile Pyrolyzer on a freshly harvested corn field in North Texas.	https://www.linkedin.com/company/applied-carbon/																			
Flying Forests	https://flyingforests.co/	Yes	No	2021	UK	Europe 	Kenya, Peru, Brazil, Indonesia, Colombia, USA	Aerial Robot	Land Restoration	Data Collection	Both	Agriculture / Farmland		Aerial drones enable precision reforestation by planting seeds and collecting environmental data in restoration sites.						https://www.linkedin.com/company/flying-forests																			
Yarbo	https://www.yarbo.com/	Yes	Yes	2015	US	North America 	US	Ground Robot	Asset Inspection	Multiple	N/A	Agriculture / Farmland		Yarbo is a modular, autonomous yard robot that uses RTK-GPS and AI vision to perform multiple outdoor maintenance tasks, including snow removal, lawn mowing, and leaf blowing.			This is consumer lawn automation, not climate-specific	https://www.youtube.com/watch?v=Fzpwz-pfTlI	Video shows Step-by-step guide for setting up the Yarbo Lawn Mower module and defining the work area using the companion app.	https://www.linkedin.com/company/yarbo	https://www.facebook.com/Yarboinc/																		
AMP (Formerly AMP Robotics)	https://ampsortation.com/	Yes	Yes	2014	US	North America 	US, Canada, Japan, UK, Ireland, Spain	Robotic Arm	Recycling/Waste Management	Carbon Removal	Mitigation	Waste & Recycling Management		AMP Cortex AI robotic sorters use computer vision to identify and pick recyclable materials from waste streams at scale.	Microsoft Climate Innovation Fund, Wellington, Congruent Ventures	https://ampsortation.com/careers		https://www.youtube.com/watch?v=Jae9i5U7Eg4	Video shows AMP is applying AI-powered sortation at scale to modernize the world's recycling infrastructure and maximize the value in waste. 	https://www.linkedin.com/company/amprobotics	https://www.instagram.com/amprobotics/																		
Niqo Robotics	https://niqorobotics.com/	Yes	Yes	2015	India	Asia	India,US	Ground Robot	Agriculture	Other	Mitigation	Agriculture / Farmland		Niqo Sense AI camera converts regular sprayers to spot sprayers; RoboThinner automates precision lettuce thinning using computer vision.	Bidra Innovation Ventures , Fulcrum Global Capital, Omnivore, Blume Ventures, Beenext, and FMC Ventures	https://niqorobotics.com/careers/		https://www.youtube.com/watch?v=pc0uYWmdGLA	Videos shows CNBC TV18 news segment covering Niqo Robotics' $13 million Series B funding round and detailing their AI spot-spraying technology for agriculture.	https://www.linkedin.com/company/niqorobotics	https://www.instagram.com/niqorobotics/																		
Solix Ag Robotics	https://www.solinftec.com/	Yes	Yes	2023	Brazil	South America	Brazil, USA, Canada	Ground Robot	Agriculture	Weeding	Mitigation	Agriculture / Farmland		Solix Sprayer autonomously navigates crop rows using AI vision for targeted weed spraying, reducing herbicides by 95% while monitoring crop health.	AgFunder, The Lightsmith Group, Blue like an Orange Sustainable Capital, Arar Capital, YvY Capital Asset Management,	https://www.solinftec.com/en-us/careers/		https://www.youtube.com/watch?v=_DIpfEDr3S4	Video shows Solix is a fully autonomous, solar-powered scouting and spraying robot designed to operate 24/7,	https://www.linkedin.com/company/solinftec	https://www.instagram.com/solinftec/																		
Genrobotic Innovations 	https://genrobotics.com/	Yes	Yes	2017	India	Asia	India	Ground Robot	Recycling/Waste Management		N/A	Urban / Built Environment		Bandicoot is a sewer-cleaning robot that descends into manholes, removes blockages, and unclogs drains so workers no longer need to enter hazardous spaces.	Unicorn Venture Capital 	https://genrobotics.com/careers/		https://www.youtube.com/watch?v=MhSX-gdgJNc	Video showcases the Bandicoot robot, the world's first semi-robotic device designed for cleaning manholes and sewers, developed by Genrobotic Innovations.	https://www.linkedin.com/company/genrobotics	https://www.facebook.com/genrobotic																		
Pave Robotics 	https://pave-robotics.com/	Yes	Yes	2024	US	North America 	US	Ground Robot	Construction	Asset Inspection	Both	Urban / Built Environment		Pave Robotics develops the Tracer, a fully autonomous robot that uses sub-millimeter precision to detect, clean, and seal cracks in asphalt roads, drastically improving road longevity and reducing labor-intensive maintenance costs.	Y Combinator, Pioneer Fund, FundersClub, Contrarian Thinking Capital, Multimodal Ventures, Spacecadet Ventures.			https://www.youtube.com/watch?v=3S5MjsgtCyE	Video showcases the Tracer robot, a fully autonomous machine developed by Pave Robotics to revolutionize asphalt crack sealing and road maintenance.																				
Orpheus Ocean	https://orpheusocean.com/	Yes	No	2024	US	North America 	US	Ocean Robot	Ocean Data	Environmental Monitoring	Adaptation	Marine / Deep Ocean		Orpheus Ocean designs, builds, and operates small-footprint, autonomous underwater vehicles (AUVs) capable of reaching the full 11,000-meter ocean depth to collect scalable, high-resolution seafloor data for blue economy and scientific missions.	Propeller, Urban Future Lab, Climate Capital, Jetstream (San Francisco), Village Global.	https://orpheusocean.com/careers		https://www.youtube.com/watch?v=JVIRX0O3xSs	Video The video "Introducing the Orpheus AUV | Nautilus Live" features Jake Russell, co-founder and CEO of Orpheus Ocean, introducing the company's autonomous underwater vehicle (AUV)	https://www.linkedin.com/company/orpheus-ocean																			
Angsa Robotics 	angsa-robotics.com	Yes	Yes	2019	Germany 	Europe	Germany	Ground Robot	Recycling/Waste Management	Weeding	N/A	Agriculture / Farmland		Angsa Robotics develops an autonomous, AI-powered robot that identifies and vacuums small litter like cigarette butts from grass and gravel surfaces.	Husqvarna Ventures, ESA Business Incubation Centre (Bavaria), TUM Venture Labs, Xpreneurs, Clean Cities ClimAccelerator.	https://angsa-robotics.com/en/career/		https://www.youtube.com/watch?v=7zlVvUNFO90&t=19s	Video shows the Angsa Robotics autonomous cleaning machine in action on a grassy area . The robot is designed for green spaces and is shown being used by BSR	https://www.linkedin.com/company/angsa-robotics																			
GreenDigger	https://www.greendigger.org/	Yes	No	2024	Netherlands	Europe	Netherland,Kenya and Tanzania	Ground Robot	Land Restoration	Carbon Removal	Mitigation	Degraded / Fire-Scarred Landscapes		GreenDigger is an environmental initiative focused on large-scale land restoration and carbon reduction through technology-driven greening projects.				https://www.youtube.com/watch?v=cp6jOCrnpPU	Video emphasizes that by "reviving the earth," the project simultaneously reduces carbon through  high-tech model for large-scale environmental recovery.	https://www.linkedin.com/company/greendigger/	https://www.facebook.com/GreenDigger.org/																		
Sudoyantra India Pvt. Ltd. 	https://www.sudoyantra.com/	Yes	Yes	2022	India	Asia	India	Ground Robot	Solar Power	Multiple	Mitigation	Extreme / Arid Environments		Sudoyantra India develops automated waterless robotic cleaning systems and IoT monitoring tools to maximize the efficiency and ROI of solar energy plants.				https://www.youtube.com/watch?v=YGQaAW9IN3A	Video shows a SudoYantra autonomous solar panel cleaning robot in action. The robot moves across a large solar panel installation, cleaning the panels with its brushes	https://www.linkedin.com/posts/sudoyantra_sudo-yantra-activity-7220993541173391361-eUnm	https://www.instagram.com/sudoyantra/																		
Aerobotics	https://aerobotics.com/	Yes	Yes	2014	US	North America 	South Africa, USA, Australia, Spain, and Portugal	Aerial Robot	Agriculture	Environment Monitoring 	Mitigation	Agriculture / Farmland		Aerobotics is a precision agriculture company that uses drone and satellite imagery combined with AI to help fruit growers monitor tree health and forecast yields.	Naspers, Cathay Innovation, FMO, 4Di Capital, Savannah Fund, Nedbank CIB, and Paper Plane Ventures.	https://aerobotics.com/careers		https://www.youtube.com/watch?v=V9RMFJuCNDI	Video demonstrates an autonomous indoor drone system specifically designed for warehouse inventory management and stocktaking.	Aerobotics | LinkedIn	https://www.facebook.com/aeroboticsintl																		
Recycleye 	https://recycleye.com/	Yes	Yes	2019	UK	Europe 	UK, France, Italy, Ireland, Germany, Spain, and USA.	Ground Robot	Recycling/Waste Management	Multiple	Mitigation	Waste & Recycling Management		Recycleye develops AI-powered computer vision and robotic picking systems to automate and provide data analytics for the sorting of dry mixed recyclables.	DCVC, Promus Ventures, Playfair Capital, MMC Ventures, Seaya Andromeda, Creator Fund, and Atypical Ventures.	https://apply.workable.com/recycleye/		https://www.youtube.com/watch?v=patUAq1Yg58	Video shows these robots are integrated into existing waste management conveyor lines to autonomously identify and pick specific materials—such as plastics, paper, and metal cans—from a stream of mixed recycling [00:10].	https://www.linkedin.com/company/recycleye/	https://www.instagram.com/lifeatrecycleye/ 																		
Seaside Robotics 	https://www.1101001000.com/seaside-robotics	Yes	Yes	2023	Japan	Asia	Japan	Ground Robot	Recycling/Waste Management	Environment Monitoring 	Mitigation	Coastal / Marine		Seaside Robotics develops small, smart ground robots designed to autonomously remove marine debris and trash from shorelines without harming local wildlife or habitats.				https://www.1101001000.com/seaside-robotics	Video shows mini ground robots cleaning beach with automation	https://jp.linkedin.com/in/ryotayokoiwa																			
CLIIN Robotics	https://cliin.dk/	Yes	Yes	2016	Denmark	Europe 	Denmark, Singapore, Japan, Turkey, Greece	Ground Robot	Recycling/Waste Management	Multiple	Mitigation	Marine / Industrial		CLIIN Robotics develops versatile magnetic climbing robots that provide chemical-free cleaning for ship cargo holds, hulls, and storage tanks to improve safety and environmental sustainability.		https://cliin.dk/joining-cliin		https://www.youtube.com/watch?v=sE7arjm_CWQ	Video shows features a motorized system with two brush types—medium nylon and light stainless—to efficiently remove algae and biofouling	https://dk.linkedin.com/company/cliin	https://www.facebook.com/photo.php?fbid=122211670130178756&id=61555362703680&set=a.122158704584178756																		
Hyperion Robotics	https://www.hyperionrobotics.com/	Yes	Yes	2018	Finland	Europe 	Finland, UK	Robotic Arm	Construction	Distributed Energy	Both	Urban / Built Environment		Hyperion Robotics provides mobile 3D printing micro-factories that use industrial robots and low-carbon, recycled materials to build high-performance concrete infrastructure more sustainably.	Lifeline Ventures, Katapult, Übermorgen Ventures, Goldacre	https://www.kubota.com/search/?query=career+company		https://www.youtube.com/watch?v=KZfhZki9yjU	Video showcases Hyperion Robotics' 3D Printing Micro-factory, which can produce up to 20 concrete foundations in just three days	https://fi.linkedin.com/company/hyperionrobotics																			
Kubota Corporation	https://www.kubota.com/	Yes	Yes	1890	Japan	Asia	Japan, USA, France, Germany, China, and Thailand.	Ground Robot	Agriculture	Multiple	Mitigation	Terrestrial / Agricultural		Kubota Corporation develops autonomous ground robots and smart agricultural machinery designed to solve labor shortages and improve environmental sustainability in global food production.				https://www.youtube.com/watch?v=BQ-EUElg_MQ	Video showcases the ultimate tractor performance.It demonstrates powerful capabilities and durability in real-world farming and heavy-duty tasks.	https://www.linkedin.com/company/kubota/	https://www.facebook.com/KubotaGlobal/																		
Sea6 Energy 	https://www.sea6energy.com/	Yes	Yes	2010	India	Asia	India, Indonesia	Ocean Robot	Seaweed Farming	Multiple	Mitigation	Marine / Ocean		Sea6 Energy develops automated marine robotic platforms and biorefinery technologies to enable large-scale, sustainable seaweed farming for the production of carbon-neutral biofuels and bioproducts.	Tata Capital, BASF Venture Capital, Aqua-Spark, Silverstrand Capital			https://www.youtube.com/watch?v=faVzJfrCpUY	Video shows "Floating Ocean Tractor," this innovative vessel is the core of Sea6 Energy's mechanized farming system. It enables simultaneous seeding and harvesting of seaweed farms	https://www.linkedin.com/company/sea6-energy-private-limited	https://www.facebook.com/sea6energy/																		
Ascend Robotics	https://www.ascendrobotics.com/	Yes	Yes	2017	US	North America 	US	Robotic Arm	Construction	Construction	Both	Industrial / Urban / Artificial		Ascend Robotics provides AI-powered, vision-guided collaborative robots for high-precision industrial tasks, including painting, parts picking, and warehouse logistics.				https://www.youtube.com/watch?v=lqZ3X2xkC88	Videos shows its robotis arm doing paiting automatically with precision.																				
Solinas	https://solinas.in/	Yes	Yes	2018	India	Asia	India	Ground Robot	Recycling/Waste Management	Asset Inspection	Both	Urban / Built Environment		Solinas develops indigenous robotic solutions for pipeline inspection, sanitation, and underground asset management.	Social Alpha, Rainmatter, 8X Ventures, Neev Fund, Lister Ventures.	https://solinas.in/careers/		https://www.youtube.com/watch?v=A0DjB1hvTds	Video shows features the Endobot, an AI-powered robotic crawler series developed by Solinas Integrity for inspecting underground pipelines.	https://in.linkedin.com/company/solinasin	https://www.instagram.com/solinas_integrity/?hl=en																		
Farm Wise	https://farmwise.io/	Yes	Yes	2016	US	North America 	US	Ground Robot	Weeding	Agriculture	Mitigation	Terrestrial / Agricultural		FarmWise develops AI-driven agricultural robots that use computer vision to perform high-precision, chemical-free weeding for large-scale vegetable farms.	Playground Global, Felicis Ventures, GV, Fall Line Capital, Calibrate Ventures, Middleland Capital.	https://farmwise.io/careers		https://www.youtube.com/watch?v=wXm7HfBuiqM&t=17s	Video shows AI-driven weeding.	https://www.linkedin.com/company/farmwise	https://www.instagram.com/farmwiselabs/																		
EyeROV 	https://eyerov.com/	Yes	Yes	2016	India	Asia	India, UAE, Saudi Arabia	Ocean Robot	Ocean Data	Multiple	Mitigation	Marine / Ocean		EyeROV develops AI-enabled underwater remotely operated vehicles (ROVs) and surface vehicles for commercial and defense inspections of submerged infrastructure.	Unicorn India Ventures, GAIL, BPCL, Social Alpha, K Chittilappilly Foundation.	https://eyerov.com/company/careers/		https://www.youtube.com/watch?v=GiFHWnTyy_E	Video presents a company profile for EyeROV (IROV Technologies Pvt. Ltd), a pioneer in underwater robotics and marine technology	https://in.linkedin.com/company/eyerov	https://www.facebook.com/eyerov																		
Homura Heavy Industries	https://www.hmrc.co.jp/en/	Yes	Yes	2016	Japan	Asia	Japan	Ocean Robot	Ocean Data	Multiple	Both	Coastal / Water Infrastructure		Homura Heavy Industries develops autonomous marine surface vehicles and AI-driven control systems to automate tasks in aquaculture, fisheries, and underwater infrastructure monitoring.	Drone Fund, MIRAIDOOR, Agribusiness Investment & Development Co., Iwagin Jigyo Souzou Capital.			https://www.youtube.com/watch?v=ntLMu3-far4	Video documents the pitch presentation by Homura Heavy Industries  at the X-Tech Innovation 2021 Tohoku Regional Final.		https://www.facebook.com/hmrc.jp/																		
Shark Robotics	https://www.shark-robotics.com/	Yes	Yes	2016	France	Europe 	France, Ukraine, Singapore	Ground Robot	Other	Multiple	N/A	Forests & Terrestrial		Shark Robotics is a leader in terrestrial robotics for hostile environments, providing modular autonomous systems for firefighting, demining, and industrial safety.	Move Capital, Ouest Croissance, Ocean Participations.	https://www.shark-robotics.com/careers/		https://www.youtube.com/watch?v=9v7wm7wm3LQ	Video showcasing Colossus, a modular firefighting robot by Shark Robotics,	https://www.linkedin.com/company/sharkrobotics/	https://www.facebook.com/SharkRoboticsFrance/																		
Ishitva Robotic Systems	https://ishitva.in/	Yes	Yes	2018	India	Asia	India	Ground Robot	Recycling/Waste Management	Multiple	Both	Urban / Built Environment		Ishitva Robotic Systems provides AI-powered robotic and air-sorting solutions designed to automate waste segregation and promote a circular economy.	Inflection Point Ventures, FirstPort, Spectrum Impact			https://www.youtube.com/watch?v=Ll4ho-iZzkg 			https://www.facebook.com/ishitvarobotic/ 																		
WindBorne Systems	https://windbornesystems.com/	Yes	Yes	2017	US	North America 	US, Svalbard (Norway), and South Korea.	Aerial Robot	Other	Multiple	Both	Atmospheric & Waste Management		WindBorne Systems operates the world's largest constellation of autonomous weather balloons and an AI-based weather model to provide hyper-accurate global forecasts.	Khosla Ventures, Footwork VC, Pear VC, Ubiquity Ventures, Susa Ventures, Convective Capital.	https://windbornesystems.com/open-roles	Dont sure  about its technology although it is Autonomous but dont seem to be a robot	https://www.youtube.com/watch?v=0Lc2F_xwXjo	Video shows a behind-the-scenes look at how advanced weather balloons are built and tested at WindBorne Systems, exploring the manufacturing process from start to finish. 	https://www.linkedin.com/company/windborne/	https://www.instagram.com/windbornewx/?igsh=MzRlODBiNWFlZA%3D%3D#																		
PV Circonomy	https://www.pvcirconomy.com/	Yes	Yes	2023	US	North America 	US	Robotic Arm	Recycling/Waste Management	Solar Power	Mitigation	Atmospheric & Waste Management		PV Circonomy operates a fully automated, AI-driven recycling facility that achieves a 99.3% material recovery rate for end-of-life solar panels.				https://www.youtube.com/watch?v=88vNuONjAMA	Video shows robotics arm working on solar panels as Solar Panel Treatment - Full, PV Circonomy	https://www.linkedin.com/company/pv-circonomy	https://www.facebook.com/people/PV-Circonomy/61559655374593/																		
Recirculate (Project)	https://recirculate.eu/	Yes	No	2023	Finland	Europe 	Finland, Spain, Germany	Robotic Arm	Recycling/Waste Management	Multiple	Mitigation	Atmospheric & Waste Management		An EU-funded consortium developing AI-powered robotic systems and blockchain marketplaces to automate the dismantling, sorting, and second-life reuse of electric vehicle batteries.				https://www.youtube.com/watch?v=fzlzyrNovFU&embeds_referring_euri=https%3A%2F%2Fprobot.fi%2F&source_ve_path=Mjg2NjY	Video show demonstrates the Recirculate project's D2.4 deliverable, showcasing a robotized disassembly and sorting system for end-of-life electric vehicle (EV) batteries (0:04). The core of the demonstration focuses on the module-to-cell disassembly process conducted in an industrially relevant environment at Centria University of Applied Sciences 	https://www.linkedin.com/company/recirculate-eu	https://www.facebook.com/people/Recirculate/100093200620808/																		
Fraunhofer Society 	https://www.fraunhofer.de/	Yes	No	1949	Germany 	Europe 	Germany 	Robotic Arm	Recycling/Waste Management	Agriculture	Both	Atmospheric & Waste Management		A leading European research organization developing AI-driven robotic systems for the automated, non-destructive disassembly of complex products like electronics and batteries to enable high-value material recovery.	Fraunhofer Venture	https://www.fraunhofer.de/en/jobs-and-career.html		https://www.youtube.com/watch?v=d0V4OA69bpA	In this Fraunhofer FOKUS podcast, experts discuss the 2025 Germany Digitalization Index, noting that while Germany is technically more digital, user habits are evolving slowly.	https://www.linkedin.com/company/fraunhofer-gesellschaft/	https://www.linkedin.com/company/fraunhofer-gesellschaft/																		
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
																																							
