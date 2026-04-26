<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=35&duration=2500&pause=800&color=005F73&center=true&vCenter=true&width=600&height=70&lines=Aung+Kaung+Myat&animation=wave" alt="Typing SVG" />
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Robotics_Software_Engineer-008080?style=for-the-badge&logo=robot&logoColor=white" alt="Robotics Software Engineer" />
  <img src="https://img.shields.io/badge/ROS2_Navigation-008080?style=for-the-badge&logo=compass&logoColor=white" alt="ROS2 Navigation" />
  <img src="https://img.shields.io/badge/Computer_Vision-008080?style=for-the-badge&logo=opencv&logoColor=white" alt="Computer Vision" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=AungKaung1928&style=for-the-badge&color=008080&label=Profile+Views" alt="Profile Views" />
  <img src="https://img.shields.io/github/followers/AungKaung1928?style=for-the-badge&color=008080&label=Followers" alt="Followers" />
</p>

---

## About Me

**Robotics Software Engineer with a Mechanical Engineering background**

Developing autonomous mobile robots and manipulation systems with [ROS2](https://www.ros.org/), focused on navigation, localization, sensor integration, and real hardware deployment. Moving toward physical AI — sim-to-real transfer, legged robotics, and perception systems for autonomous robots in unstructured environments.

**Focus Areas:** Autonomous Mobile Robots • ROS2 Navigation & Localization • LiDAR Perception & PCL • Sensor Fusion • Robot Manipulation (MoveIt2) • Machine Learning for Robotics

---

## Tech Stack

<p align="center">
  <a href="https://www.ros.org/" target="_blank">
    <img src="https://img.shields.io/badge/ROS2-22314E?style=for-the-badge&logo=ros&logoColor=white" alt="ROS2" />
  </a>
  <a href="https://www.python.org/" target="_blank">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  </a>
  <a href="https://isocpp.org/" target="_blank">
    <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" />
  </a>
  <a href="https://www.linux.org/" target="_blank">
    <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  </a>
  <a href="https://git-scm.com/" target="_blank">
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  </a>
  <a href="https://pytorch.org/" target="_blank">
    <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  </a>
  <a href="https://opencv.org/" target="_blank">
    <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  </a>
  <a href="https://pointclouds.org/" target="_blank">
    <img src="https://img.shields.io/badge/PCL-008080?style=for-the-badge&logoColor=white" alt="PCL" />
  </a>
  <a href="https://www.docker.com/" target="_blank">
    <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  </a>
  <a href="https://kafka.apache.org/" target="_blank">
    <img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka" />
  </a>
  <a href="https://gazebosim.org/" target="_blank">
    <img src="https://img.shields.io/badge/Gazebo-FF6F00?style=for-the-badge&logoColor=white" alt="Gazebo" />
  </a>
</p>

---

## Projects

### Go2 Perception Pipeline — `C++ · ROS2 · PCL · Unitree Go2`
- Custom LiDAR perception pipeline for the Unitree Go2 quadruped robot in Gazebo
- Ground plane removal via PCL PassThrough filter — publishes clean obstacle point clouds
- RViz visualization of raw vs filtered clouds; teleop-ready with custom world

[View on GitHub →](https://github.com/AungKaung1928/go2-perception-pipeline)

---

### MoveIt2 Pick & Place Demo — `Python · MoveIt2 · ROS2 · Franka Panda`
- 7-DOF Franka Panda arm with OMPL motion planning and constraint-based execution
- ±1cm positioning accuracy; >95% success rate with multi-attempt fallback strategies
- Production-grade safety: action server verification, velocity scaling, graceful recovery

[View on GitHub →](https://github.com/AungKaung1928/moveit_pickplace_demo)

---

### TF Transform Explorer — `C++ · TF2 · Nav2 · pluginlib`
- TF2 frame transformation system with dynamic and static broadcasters
- Custom TFDiagnostics message type for transform health monitoring
- Nav2 costmap plugin via pluginlib for keepout zone implementation
- Autonomous patrol with random goal generation and recovery behavior

[View on GitHub →](https://github.com/AungKaung1928/TF-Transform-Explorer)

---

### Fleet Monitoring System — `Python · ROS2 · Kafka · Docker`
- Distributed multi-robot telemetry pipeline: ROS2 → Kafka → QuestDB time-series database
- Simulates production fleet infrastructure with multiple TurtleBot3 robots in Gazebo
- Containerized stack with Docker; real-time dashboard over PostgreSQL wire protocol

[View on GitHub →](https://github.com/AungKaung1928/fleet_monitoring_ws)

---

## GitHub Stats

<p align="center">
  <img height="180em" src="https://github-readme-stats-sigma-five.vercel.app/api?username=AungKaung1928&show_icons=true&theme=github_dark&hide_border=true&title_color=58a6ff&icon_color=58a6ff&count_private=true" />
  <img height="180em" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=AungKaung1928&layout=compact&theme=github_dark&hide_border=true&title_color=58a6ff" />
</p>

---

## Technical Expertise

**ROS2 Development** → Navigation with [Nav2](https://nav2.org/), action servers, lifecycle nodes, pluginlib  
**SLAM & Localization** → AMCL, GMapping, Cartographer, FAST-LIO2  
**Sensor Processing** → LiDAR, IMU, Camera — PCL filtering, sensor fusion  
**Manipulation** → MoveIt2, OMPL motion planning, trajectory execution  
**Control Systems** → PID controllers, state machines, path planning  
**Computer Vision** → Object detection with OpenCV and PyTorch (YOLO, CNN)  
**Infrastructure** → Docker, Kafka, ROS2–Kafka telemetry pipelines  

**Next:** Isaac Sim · TensorRT on Jetson · Sim-to-Real transfer · 3D detection (PointPillars)

---

## Let's Connect

<p align="center">
  <a href="https://www.linkedin.com/in/aung-kaung-myat-30943a215/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://aungkaung1928.github.io" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-005F73?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://github.com/AungKaung1928" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="mailto:aungkaungmyattt1928@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>
