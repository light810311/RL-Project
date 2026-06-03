## Context

The project aims to implement the "Attention-Enhanced CADRL" framework for socially aware robot navigation. Current solutions lack the ability to scale to dense crowds or model complex human-human interactions. This design establishes a modular Python architecture to address these gaps.

## Goals / Non-Goals

**Goals:**
- **Agent Modularity**: Create abstract `Agent`, `Human`, and `Robot` classes.
- **Attention Policy**: Implement a PyTorch-based neural network that uses self-attention to pool state information from a variable number of neighbors.
- **Simulation**: Build a 2D continuous space environment with kinematic constraints.
- **Metrics**: Implement social compliance scoring (proximity, navigation time, collision rate).

**Non-Goals:**
- Training the models to convergence in this initial setup.
- Integration with ROS or real-world sensors.
- Graphical User Interface (GUI) beyond basic Matplotlib visualization.

## Decisions

- **State Representation**: The robot's state will include its own position, velocity, radius, and goal. Neighboring human states will be relative to the robot.
- **Attention Layer**: We will implement the `AttentionNetwork` using a Query-Key-Value-like mechanism or a simple MLP-based weight generator as described in the ICRA 2019 paper:
  - $e_i = \phi(s_r, s_h^i)$ (interaction encoding)
  - $\alpha_i = \text{softmax}(\psi(e_i))$ (attention weights)
- **Environment Interface**: Use the standard `gym.Env` pattern for compatibility with common RL libraries.
- **Directory Structure**:
  - `src/agents/`: Definitions for human and robot agents.
  - `src/policy/`: Neural network and attention logic.
  - `src/env/`: The navigation simulation logic.

## Risks / Trade-offs

- **Computational Complexity**: While attention scales better than fixed-input vectors, it is more computationally intensive than ORCA.
- **Sim-to-Real Gap**: The kinematic modeling in the simulation is a simplified version of real-world dynamics.
