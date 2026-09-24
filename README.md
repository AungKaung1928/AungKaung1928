## Aung Kaung Myat

Robotics Software Engineer. ROS 2, C++, navigation and LiDAR perception on real mobile robots in my current role.

The projects below are personal work: robot learning trained in simulation on a laptop CPU, measured against a hand-written baseline, exported to run on device.

Every number has a script behind it; unmeasured tables are marked as such.

---

### Projects

**[microduck-rl](https://github.com/AungKaung1928/microduck-rl)** — `Python · MuJoCo · PyTorch · ONNX`<br>
Balance policy for a 25 cm, 14-servo open-source biped, trained with PPO in CPU MuJoCo on a 48-dim sensors-only observation. Reward rebuilt after three of four penalties measured under 0.25% of the return. After 25M steps PPO scores 332.6 ± 5.1 of 500 against PD's 175.8 ± 0.2, trunk upright 74% of steps vs 47%, 100 episodes × 5 seeds; push recovery is still unmeasured. Domain randomisation, tested on two held-out physics models, made it worse: it learned to brace in a crouch (upright 28% vs 47%), shrugged off backlash and collapsed on rollers (147 vs 374). One seed, half the schedule, reported as it came out.

**[mujoco-vecenv-cpp](https://github.com/AungKaung1928/mujoco-vecenv-cpp)** — `C++17 · MuJoCo · pybind11 · CMake`<br>
The same environment in C++17 on threads, drop-in for the Python training script. 6,275 of 6,275 observations bit-identical to Python over 25 episodes (matching numpy's pairwise sum and libm `pow`). 1.9–2.0x the Python processes at 8 workers (12,327 vs 6,385 env-steps/s), 27,011 bare physics steps/s. CI under ASan, UBSan and TSan.

**[so-arm100-rl](https://github.com/AungKaung1928/so-arm100-rl)** · **[so-arm100-il](https://github.com/AungKaung1928/so-arm100-il)** · **[so-arm100-vla](https://github.com/AungKaung1928/so-arm100-vla)** on the shared bench **[so-arm100-sim](https://github.com/AungKaung1928/so-arm100-sim)** — `Python · MuJoCo · PyTorch · LeRobot`<br>
One MuJoCo bench for the SO-ARM100 arm (four tasks, scripted IK expert, domain randomisation, six held-out physics cells, LeRobot recorder) and three ways to learn on it: curriculum PPO, imitation (BC, DAgger, ACT), and a language-conditioned policy tested on held-out paraphrases and unseen task–colour pairs against SmolVLA-base zero-shot. 127 tests green. The expert scores 0.93 on lift and pick-and-place, 0.73 and 0.72 on the small cube. RL, one training seed: a domain-randomised fine-tune halves the held-out success drop (0.120 → 0.056), almost all of it on 3-step action latency (0.46 → 0.76); language, one seed, weak: 0.11 on seen instructions, 0.03 on unseen task–colour pairs, encoder ablation inside its noise, SmolVLA-base 0/40 zero-shot at 3.2 s per action chunk on CPU; imitation tables not yet measured.

**[mujoco-clutter-detect](https://github.com/AungKaung1928/mujoco-clutter-detect)** — `Python · PyTorch · MuJoCo · ONNX Runtime`<br>
Anchor-free clutter detection on synthetic MuJoCo scenes, labels from the segmentation buffer. 0.911 mAP@[.5:.95] vs a classical baseline's 0.532, COCO AP from scratch, 1.20 ms/image on 8 threads. Static INT8 on one thread: 1.38 ms, 2.6x fp32's 3.57 ms and under classical 2.13 ms, mAP 0.9097 vs 0.9107; pruning cost 0.065 mAP, so INT8 alone ships. The augmentation ablation was a null result (+0.0007 mAP), published as one.

### Earlier work

- **[ppo-from-scratch](https://github.com/AungKaung1928/ppo-from-scratch)** — PPO from first principles vs LQR on a hand-written cart-pole, 16 seeds, median 62,144 steps to threshold; LQR wins on sample cost and basin of attraction, and the repo says so. Its PPO loop trains the biped and the arm.
- **[mujoco-cube-pose-cnn](https://github.com/AungKaung1928/mujoco-cube-pose-cnn)** — cube pose from an overhead camera, 0.59 mm median error (27k-param soft-argmax CNN) vs classical 1.91 mm. Its keypoint head is the front end of the arm's image policies.
- **[moveit_pickplace_demo](https://github.com/AungKaung1928/moveit_pickplace_demo)** — camera-to-grasp loop on a simulated Franka Panda; no success rate claimed, none measured.
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
