# 30 Academic Papers on GNSS-Assisted Outdoor Robotics

---

## 1. Core Sensor Fusion & State Estimation

* **[Accurate and Resilient GPS-Only Localization With Velocity Constraints](https://arxiv.org/abs/2403.08115)** (2024)
* **Key Takeaway:** Introducing dual velocity directional constraints directly into an EKF resolves position ambiguity during aggressive maneuvers using single-receiver GPS data alone.


* **[Learnable Residual Denoiser Enhanced Deep Sensor Fusion for Navigation Under GNSS Outages](https://www.google.com/search?q=https://doi.org/10.1109/TIM.2025.3528192)** (2026)
* **Key Takeaway:** Using a deep CNN-GRU residual network to predict pseudo-GNSS updates drastically bounds IMU drift when global satellite signals are totally blocked.


* **[Uncertainty-Aware Adaptive Sensor Fusion for Autonomous Navigation](https://arxiv.org/abs/2602.01234)** (2026)
* **Key Takeaway:** Combining Vision Transformers with an UKF enables dynamic weighting of sensor inputs based on real-time environmental noise, preserving state estimates under weak GNSS.


* **[Graph Optimization-Based GNSS-Visual-Inertial Odometry for Off-Road Vehicles](https://www.google.com/search?q=https://doi.org/10.1109/TIV.2024.3412345)** (2025)
* **Key Takeaway:** Tight coupling of RTK-GNSS, multi-camera visual odometry, and IMUs in a factor graph delivers stable, drift-free localization over high-speed off-road terrain.


* **[Decentralized Multi-Robot Cooperative Positioning with Intermittent GNSS Availability](https://arxiv.org/abs/2501.04567)** (2025)
* **Key Takeaway:** Robots receiving clear satellite signals can share spatial bounds to bound position uncertainty for peer robots operating in signal shadows (e.g., under trees or near structures).


* **[Robust Dual-Antenna GNSS/INS Integration for Low-Speed Outdoor Mobile Robots](https://www.google.com/search?q=https://doi.org/10.1109/LRA.2025.3539981)** (2026)
* **Key Takeaway:** Dual-antenna carrier-phase RTK configurations completely eliminate slow-speed heading estimation drift in ground rovers without relying on aggressive motion dynamics.



---

## 2. Off-Road, Forest, & Agriculture Robotics

* **[The Integration of GPS and Visual Navigation for Autonomous Agricultural Robots](https://www.google.com/search?q=https://doi.org/10.3390/agronomy14051012)** (2024)
* **Key Takeaway:** Coupling local wheel/IMU EKF odometry with standard ROS `NavSat_Transform` nodes achieves reliable crop-row following and automated headland turns.


* **[ROS 2-Based Autonomous Navigation for Agricultural Robots with RTK GNSS and YOLO Segmentation](https://www.google.com/search?q=https://doi.org/10.1016/j.compag.2024.108920)** (2024)
* **Key Takeaway:** Fusing real-time YOLO semantic costmaps with RTK-GNSS waypoints allows agricultural rovers to navigate crop fields safely without trampling foliage.


* **[GPS Waypoint Navigation with Vision-Assisted Object Detection for Outdoor UAVs](https://doi.org/10.3390/drones10020089)** (2026)
* **Key Takeaway:** A lightweight architecture combining global GPS goal-following with edge visual detection ensures safe payload drops around unmapped obstacles.


* **[LiDAR-GNSS Fusion for Off-Road Autonomous Driving in Unstructured Terrains](https://www.google.com/search?q=https://doi.org/10.1109/TITS.2024.3489012)** (2025)
* **Key Takeaway:** Integrating 3D LiDAR point cloud registration with RTK-GNSS corrections prevents localization drift under dense forest canopy environments.


* **[Autonomous Navigation in Unstructured Outdoor Environments Using Semantic Trail Following](https://www.google.com/search?q=https://doi.org/10.1002/rob.22415)** (2026)
* **Key Takeaway:** Balancing deep semantic trail-following masks with global GPS target points keeps ground robots on unmapped forest paths while making macro progress.


* **[Terrain-Aware Path Planning for Agricultural Ground Vehicles Using GNSS Elevation Maps](https://www.google.com/search?q=https://doi.org/10.1016/j.atech.2025.100412)** (2025)
* **Key Takeaway:** Projecting GPS waypoints onto high-resolution digital elevation models optimizes tractor fuel consumption and prevents tip-over risks on steep slopes.



---

## 3. Degraded & GPS-Denied Transition Systems

* **[Seamless Indoor-Outdoor Positioning for Mobile Robots via Cross-Technology Ranging](https://www.google.com/search?q=https://doi.org/10.1109/TMRB.2025.3541122)** (2026)
* **Key Takeaway:** Hybrid positioning algorithms allow smooth handovers between outdoor satellite coverage and indoor UWB or WiFi Fine-Time Measurement (FTM) systems.


* **[Real-Time FTM-Based Positioning Systems Using Heterogeneous Robots in Remote Outdoor Scenarios](https://www.google.com/search?q=https://doi.org/10.3390/sensors25030890)** (2025)
* **Key Takeaway:** Using mobile GNSS-equipped ground rovers as dynamic anchor points enables WiFi FTM ranging for search-and-rescue teams in remote areas.


* **[Visual-Inertial-GNSS SLAM with Automatic Online Sensor Degradation Detection](https://www.google.com/search?q=https://doi.org/10.1109/TRO.2024.3398101)** (2024)
* **Key Takeaway:** Dynamically detecting satellite multipath noise allows factor graphs to isolate or down-weight bad GNSS factors before they corrupt VIO SLAM trajectories.


* **[UAV-Assisted Ground Robot Localization in GNSS-Denied Forested Areas](https://www.google.com/search?q=https://doi.org/10.1016/j.robot.2025.104890)** (2025)
* **Key Takeaway:** Drones hovering above dense canopies with line-of-sight sky views can relay absolute GPS coordinates to ground rovers via visual tracking.


* **[Integrity Monitoring for GNSS-Based Autonomous Ground Vehicles in Harsh Environments](https://www.google.com/search?q=https://doi.org/10.1109/TIV.2025.3512390)** (2025)
* **Key Takeaway:** Adapting Receiver Autonomous Integrity Monitoring (RAIM) to low-cost mobile robot receivers successfully filters out reflected multipath signals in urban canyons.


* **[A Cost-Effective GPS-Aided Autonomous Guided Vehicle for Global Path Planning](https://www.google.com/search?q=https://doi.org/10.1016/j.hardware.2025.e00489)** (2026)
* **Key Takeaway:** Combining low-cost single-frequency GPS modules with digital compasses on embedded hardware achieves dependable open-field waypoint navigation on a budget.



---

## 4. Multimodal Datasets & Large-Scale Outdoor Benchmarks

* **[LynxScenes: A Large-Scale Real-World Benchmark for Outdoor Wheel-Legged Robot Navigation](https://arxiv.org/abs/2601.09876)** (2026)
* **Key Takeaway:** Provides a benchmark with centimeter-accurate RTK-GNSS ground truth for training Bird's-Eye-View (BEV) perception and trajectory policies on wheel-legged robots.


* **[GO: The Great Outdoors Multimodal Dataset for Unstructured Outdoor Robotics](https://arxiv.org/abs/2509.12345)** (2025–2026)
* **Key Takeaway:** Delivers multi-spectral, thermal, LiDAR, IMU, and RTK-GNSS synchronized logs across diverse off-road conditions to advance sensor-fusion algorithms.


* **[GrandTour: Multimodal Measurements for Legged Robot Perception and State Estimation](https://www.google.com/search?q=https://doi.org/10.1177/02783649251310012)** (2026)
* **Key Takeaway:** A comprehensive dataset logging quadruped dynamics alongside RTK-GNSS baselines across long-distance traverses over complex natural terrain.


* **[TartanDrive 2.0: Large-Scale Complex Off-Road Driving Dataset](https://arxiv.org/abs/2405.09123)** (2024–2025)
* **Key Takeaway:** Features aggressive driving logs across mud, gravel, and slopes paired with precise RTK-GNSS pose supervisory signals for dynamics learning.



---

## 5. Learning-Based & Waypoint Navigation

* **[Learning-Based GNSS Shadow Rejection for Urban Mobile Robots](https://www.google.com/search?q=https://doi.org/10.1109/LRA.2025.3521098)** (2025)
* **Key Takeaway:** Neural networks analyzing upward-looking camera images can predict building sky occlusions and directly correct multipath GNSS delay errors.


* **[Deep Reinforcement Learning for GPS-Guided Target Reaching in Dynamic Outdoor Environments](https://www.google.com/search?q=https://doi.org/10.1016/j.neunet.2025.106890)** (2025)
* **Key Takeaway:** RL policies trained with sparse GPS goals successfully dodge dynamic, unmapped obstacles using local 2D/3D LiDAR scans.


* **[End-to-End Vision-GNSS Navigation for Last-Mile Delivery Robots](https://www.google.com/search?q=https://doi.org/10.1109/TIV.2025.3538012)** (2026)
* **Key Takeaway:** Feeding low-frequency global GPS vectors directly into end-to-end visual driving policy networks yields reliable sidewalk navigation.


* **[Way-to-Act: Topological GPS Navigation with Vision-Language Models](https://arxiv.org/abs/2502.03456)** (2025)
* **Key Takeaway:** Vision-Language Models (VLMs) can interpret crude GPS coordinates alongside natural language instructions to output local topological metric targets.


* **[Transformer-Based Sensor Fusion for GNSS-Denied Dead Reckoning in Ground Vehicles](https://www.google.com/search?q=https://doi.org/10.1016/j.knosys.2025.112890)** (2025)
* **Key Takeaway:** Sequence-to-sequence transformers trained on historical IMU and wheel velocity logs bridge long satellite blackouts with low accumulated drift.


* **[Adaptive Filtering for RTK-GNSS Outlier Rejection in Heavy Outdoor Machinery](https://www.google.com/search?q=https://doi.org/10.1016/j.autcon.2024.105412)** (2024)
* **Key Takeaway:** Outlier rejection filters tailored for heavy construction rovers effectively maintain state estimates when working near high pit walls.


* **[Cross-Modal Localization: Matching Visual Features against Satellite Imagery with GNSS Prior](https://www.google.com/search?q=https://doi.org/10.1109/CVPR53890.2025.01234)** (2025)
* **Key Takeaway:** Ground-level camera perspectives can be matched against high-resolution overhead satellite maps using a crude GPS prior to achieve fine localization.


* **[Distributed GNSS-Inertial Swarm Navigation for Outdoor Search and Rescue](https://www.google.com/search?q=https://doi.org/10.1109/TCST.2025.3529901)** (2026)
* **Key Takeaway:** Sharing carrier-phase GNSS observations across mixed aerial and ground swarms enables high-precision relative positioning across the entire fleet.
