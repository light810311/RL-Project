## 1. Project Foundation

- [ ] 1.1 Create the modular directory structure: `src/agents/`, `src/policy/`, and `src/env/`.
- [ ] 1.2 Implement the `Agent` abstract base class with methods for `observe()`, `act()`, and `update_state()`.
- [ ] 1.3 Implement `Human` and `Robot` subclasses in `src/agents/agent.py` with specific kinematic constraints.

## 2. Attention Policy Implementation

- [ ] 2.1 Implement the `AttentionLayer` using PyTorch to calculate interaction weights between the robot and $N$ neighbors.
- [ ] 2.2 Implement the `MultiAgentPolicy` which combines self-state and the attentive pooling of neighbor states.
- [ ] 2.3 Verify that the output of the attention mechanism is permutation-invariant.

## 3. Simulation Environment

- [ ] 3.1 Implement `SocialNavEnv` (Gym interface) with continuous state space and discrete/continuous action space.
- [ ] 3.2 Implement collision detection and social distance violation logic.
- [ ] 3.3 Add support for initializing specific "failure scenarios" (e.g., Robot Frozen, Pass-Between).

## 4. Evaluation and Metrics

- [ ] 4.1 Implement `MetricsCollector` to track success rate, collision rate, and social discomfort scores.
- [ ] 4.2 Create a basic visualization script using Matplotlib to render agent trajectories.
