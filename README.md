## Aung Kaung Myat

Robotics Software Engineer. ROS 2, C++, navigation and LiDAR perception on real mobile robots in my current role.

The projects below are personal work: robot learning trained in simulation on a laptop CPU, measured against a hand-written baseline that had to be beaten, and exported to run on device.

Every number below has a script behind it. Where a table is not measured yet, the repo says so instead of guessing.

---

### Projects

**[microduck-rl](https://github.com/AungKaung1928/microduck-rl)** — `Python · MuJoCo · PyTorch · ONNX`<br>
Balance-and-recover policy for a 25 cm, 14-servo open-source biped, trained with PPO in CPU MuJoCo. The 48-dimensional observation contains only what the robot's own sensors report. The reward was rebuilt from measurement after three of four penalties turned out to be under 0.25% of the return. After 25M steps PPO scores 332.6 ± 5.1 of 500 against the PD controller's 175.8 ± 0.2 and keeps the trunk above the fall height for 74% of steps (PD 47%), 100 episodes × 5 seeds; no push knocked it over, so standing back up is still unmeasured. Domain randomisation, measured on two held-out physics models, made the policy worse: it learned to brace in a crouch (upright 28% of steps against 47%), shrugged off backlash and collapsed on rollers (147 against 374). One seed at half the schedule, reported as it came out.

**[mujoco-vecenv-cpp](https://github.com/AungKaung1928/mujoco-vecenv-cpp)** — `C++17 · MuJoCo · pybind11 · CMake`<br>
The same environment in C++17 on threads instead of forked processes, drop-in for the Python training script. 6,275 of 6,275 observations bit-identical to the Python reference over 25 episodes, which took matching numpy's pairwise summation and Python's libm `pow`. 1.9–2.0x the Python processes at 8 workers (12,327 vs 6,385 env-steps/s) and 27,011 bare physics steps/s at 8 threads. CI rebuilds the suite under ASan, UBSan and TSan.

**[so-arm100-rl](https://github.com/AungKaung1928/so-arm100-rl)** · **[so-arm100-il](https://github.com/AungKaung1928/so-arm100-il)** · **[so-arm100-vla](https://github.com/AungKaung1928/so-arm100-vla)** on the shared bench **[so-arm100-sim](https://github.com/AungKaung1928/so-arm100-sim)** — `Python · MuJoCo · PyTorch · LeRobot`<br>
One MuJoCo bench for the SO-ARM100 arm (four tasks, a scripted IK expert, domain randomisation, six held-out physics cells, 100 episodes × 5 seeds, a LeRobot dataset recorder) and three ways of learning the same tasks on it: curriculum PPO with and without randomisation, imitation from behaviour cloning through DAgger to an action-chunking transformer, and a language-conditioned policy scored on held-out paraphrases and unseen task–colour pairs, with SmolVLA-base zero-shot as a reference line. 122 tests green in CI. The expert scores 0.93 on lift and pick-and-place but 0.73 and 0.72 on the small cube. The policy tables are not yet measured.

**[mujoco-clutter-detect](https://github.com/AungKaung1928/mujoco-clutter-detect)** — `Python · PyTorch · MuJoCo · ONNX Runtime`<br>
Anchor-free tabletop clutter detection trained on synthetic MuJoCo scenes with labels read from the segmentation buffer. 0.911 mAP@[.5:.95] against a fitted classical baseline's 0.532, COCO AP implemented from scratch, 1.20 ms/image through ONNX Runtime on 8 threads. On one thread, static INT8 runs in 1.38 ms, 2.6x faster than fp32's 3.57 ms and under the classical pipeline's 2.13 ms, at mAP 0.9097 against 0.9107; structured pruning cost 0.065 mAP for 2.42 ms, so INT8 alone is what would ship. The augmentation ablation was a null result (+0.0007 mAP) and is published as one.

### Earlier work

- **[ppo-from-scratch](https://github.com/AungKaung1928/ppo-from-scratch)** — PPO from first principles against LQR on a hand-written cart-pole. 16 seeds, median 62,144 steps to threshold, permutation-tested ablations; LQR wins on sample cost and basin of attraction, and the repo says so. Its PPO loop trains the biped and the arm.
- **[mujoco-cube-pose-cnn](https://github.com/AungKaung1928/mujoco-cube-pose-cnn)** — cube pose from an overhead camera, 0.59 mm median error from a 27k-parameter soft-argmax head against a refitted classical baseline at 1.91 mm. Its keypoint head is the front end of the arm's image policies.
- **[moveit_pickplace_demo](https://github.com/AungKaung1928/moveit_pickplace_demo)** — a closed camera-to-grasp loop on a 7-DOF Franka Panda in simulation; no accuracy or success-rate figure is claimed because neither was measured.
- **[fleet_monitoring_ws](https://github.com/AungKaung1928/fleet_monitoring_ws)** — ROS 2 → Kafka → QuestDB telemetry for several TurtleBot3 in Gazebo, containerised.

Long-form walkthroughs for all of them: **[aungkaung1928.github.io/projects](https://aungkaung1928.github.io/projects/)**

---

### Stack

**Robot learning** &nbsp;PPO · imitation learning (BC, DAgger, ACT) · language-conditioned policies · reward design · domain randomisation · system identification · sim-to-real transfer<br>
**ML / CV** &nbsp;PyTorch · CNNs · object detection · INT8 quantisation and pruning · ONNX Runtime · OpenCV<br>
**Simulation** &nbsp;MuJoCo · a C++17 multithreaded MuJoCo backend · Gazebo · RViz · synthetic data generation<br>
**Robotics** &nbsp;ROS 2 (Nav2, MoveIt2, pluginlib, lifecycle nodes) · TF2 · PCL · SLAM (AMCL, Cartographer, FAST-LIO2) · sensor fusion<br>
**Systems** &nbsp;C++17 · Python · CMake · Linux · Docker · GitHub Actions · Git · Kafka

---

[Portfolio](https://aungkaung1928.github.io) · [LinkedIn](https://www.linkedin.com/in/aung-kaung-myat-30943a215/) · [Email](mailto:aungkaungmyattt1928@gmail.com)
