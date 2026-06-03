## 1. Environment Setup

- [x] 1.1 Install core dependencies: `torch`, `gym`, `numpy`, `matplotlib`.
- [x] 1.2 Install `Python-RVO2` library for human simulation.
- [x] 1.3 Set up the project structure with `crowd_sim/` and `crowd_nav/` directories.

## 2. Simulation Environment (crowd_sim)

- [x] 2.1 Implement `CrowdSim` environment class with Gym interface.
- [x] 2.2 Implement human agent simulation logic using RVO2.
- [x] 2.3 Implement observation space (robot state + human states).
- [x] 2.4 Implement reward function (collision penalty, goal reaching reward, etc.).

## 3. Policy Implementation (crowd_nav)

- [x] 3.1 Implement the Socially Attentive Value Network (Self-Attention mechanism).
- [x] 3.2 Implement the SARL policy class.
- [x] 3.3 Implement the ORCA baseline policy using `Python-RVO2`.

## 4. Training and Evaluation

- [x] 4.1 Implement `train.py` with training loop and logging.
- [x] 4.2 Implement `test.py` for model evaluation and metrics.
- [x] 4.3 Implement visualization script for trajectories.

## 5. Verification

- [x] 5.1 Verify that the environment resets and steps correctly.
- [/] 5.2 Train the SARL policy and verify improvement in success rate.
- [ ] 5.3 Compare SARL performance with ORCA baseline.
