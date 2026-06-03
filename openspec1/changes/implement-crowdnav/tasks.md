## 1. Environment Setup

- [ ] 1.1 Install core dependencies: `torch`, `gym`, `numpy`, `matplotlib`.
- [ ] 1.2 Install `Python-RVO2` library for human simulation.
- [ ] 1.3 Set up the project structure with `crowd_sim/` and `crowd_nav/` directories.

## 2. Simulation Environment (crowd_sim)

- [ ] 2.1 Implement `CrowdSim` environment class with Gym interface.
- [ ] 2.2 Implement human agent simulation logic using RVO2.
- [ ] 2.3 Implement observation space (robot state + human states).
- [ ] 2.4 Implement reward function (collision penalty, goal reaching reward, etc.).

## 3. Policy Implementation (crowd_nav)

- [ ] 3.1 Implement the Socially Attentive Value Network (Self-Attention mechanism).
- [ ] 3.2 Implement the SARL policy class.
- [ ] 3.3 Implement the ORCA baseline policy using `Python-RVO2`.

## 4. Training and Evaluation

- [ ] 4.1 Implement `train.py` with training loop and logging.
- [ ] 4.2 Implement `test.py` for model evaluation and metrics.
- [ ] 4.3 Implement visualization script for trajectories.

## 5. Verification

- [ ] 5.1 Verify that the environment resets and steps correctly.
- [ ] 5.2 Train the SARL policy and verify improvement in success rate.
- [ ] 5.3 Compare SARL performance with ORCA baseline.
