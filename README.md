## Aung Kaung Myat

Robotics Software Engineer. ROS 2, C++, navigation and LiDAR perception on real mobile robots in my current role.

The projects below are personal work: learned perception and control, trained in simulation, measured against a classical baseline that had to be beaten, and exported to run on device.

Every number below has a script behind it. Where the learned method loses to the classical one, the repo says so.

---

### Projects

**[mujoco-clutter-detect](https://github.com/AungKaung1928/mujoco-clutter-detect)** — `Python · PyTorch · MuJoCo · ONNX Runtime`<br>
CenterNet-style tabletop clutter detection trained on synthetic MuJoCo scenes. 0.911 mAP@[.5:.95] against a fitted classical CV baseline's 0.532, COCO AP implemented from scratch, 1.20 ms/image through ONNX Runtime on 8 CPU threads. The augmentation ablation was a null result (+0.0007 mAP) and is published as one.

**[ppo-from-scratch](https://github.com/AungKaung1928/ppo-from-scratch)** — `Python · PyTorch · RL`<br>
PPO written from scratch and measured honestly against LQR on a hand-written cart-pole. 16 seeds, median 62,144 steps to threshold, IQR [60,442, 63,448]; ablations judged by two-sided permutation tests; hyperparameters searched on seeds disjoint from the reported ones. Conclusion goes against the learned method — LQR solves it at zero sample cost with roughly twice the basin of attraction.

**[microduck-rl-cpu](https://github.com/AungKaung1928/microduck-rl-cpu)** — `Python · MuJoCo · PyTorch`<br>
Balance-and-recover policy for a 25 cm, 14-servo open-source biped, trained in CPU MuJoCo with no GPU anywhere in the stack. Feasibility gated before any training was committed: 13,300 sustained env-steps/s across 8 processes, after three earlier figures turned out to be short bursts. 48-dimensional observation contract fixed, PD hold-pose baseline at 108.7 ± 2.9 of 500 for the policy to beat. Training is the next step.

**[mujoco-cube-pose-cnn](https://github.com/AungKaung1928/mujoco-cube-pose-cnn)** — `Python · PyTorch · MuJoCo · ONNX`<br>
Cube pose (x, y, yaw) from an overhead camera. 0.59 mm median error from a 27k-parameter soft-argmax head, beating a 130k-parameter flatten head at 0.75 mm. The classical baseline was refitted after a +2.98 mm radial bias was found in it — that correction closed 53% of the gap before the CNN was credited with anything. 0.23 ms single-threaded through ONNX Runtime.

**[moveit_pickplace_demo](https://github.com/AungKaung1928/moveit_pickplace_demo)** — `Python · C++ · ROS 2 · MoveIt2`<br>
Closed camera-to-grasp loop on a 7-DOF Franka Panda in simulation: HSV detection back-projected onto the table plane through an exact pinhole model, a C++ reachability validator ahead of planning, Cartesian-first execution with an OMPL RRTConnect fallback, and a homing recovery state. No positioning-accuracy or success-rate figure is claimed, because neither was measured.

**[fleet_monitoring_ws](https://github.com/AungKaung1928/fleet_monitoring_ws)** — `Python · ROS 2 · Kafka · Docker`<br>
Multi-robot telemetry pipeline: ROS 2 → Kafka → QuestDB, containerized, several TurtleBot3 in Gazebo. The infrastructure slot rather than the main line of work.

Long-form walkthroughs for the first five: **[aungkaung1928.github.io/projects](https://aungkaung1928.github.io/projects/)**

---

### Stack

**Robot learning** &nbsp;PPO · reward design · domain randomisation · system identification · sim-to-real transfer<br>
**ML / CV** &nbsp;PyTorch · CNNs · object detection · pose regression · ONNX Runtime · OpenCV<br>
**Simulation** &nbsp;MuJoCo · Gazebo · RViz · synthetic data generation<br>
**Robotics** &nbsp;ROS 2 (Nav2, MoveIt2, pluginlib, lifecycle nodes) · TF2 · PCL · SLAM (AMCL, Cartographer, FAST-LIO2) · sensor fusion<br>
**Systems** &nbsp;C++ · Python · Linux · Docker · Git · Kafka

---

[Portfolio](https://aungkaung1928.github.io) · [LinkedIn](https://www.linkedin.com/in/aung-kaung-myat-30943a215/) · [Email](mailto:aungkaungmyattt1928@gmail.com)
