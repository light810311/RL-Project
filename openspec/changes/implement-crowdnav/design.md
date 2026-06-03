## Context

The project implements the Crowd-Robot Interaction (CRI) model as described in the ICRA 2019 paper. The goal is to provide a simulation environment where a robot can learn to navigate through a crowd of humans using deep reinforcement learning, specifically the Socially Attentive Reinforcement Learning (SARL) policy.

## Goals / Non-Goals

**Goals:**
- Implement a robust simulation environment (`crowd_sim`) that models human-human and human-robot interactions.
- Implement the SARL policy using PyTorch, incorporating self-attention to model social interactions.
- Provide scripts for training navigation policies and evaluating them against baselines like ORCA.
- Enable visualization of robot navigation trajectories and human interactions.

**Non-Goals:**
- Deployment on physical robot hardware.
- Real-time performance optimization for embedded systems.
- Supporting environments other than the circular/linear crowd scenarios described in the paper.

## Decisions

- **Framework**: Use PyTorch for deep reinforcement learning due to its flexibility in implementing custom attention mechanisms.
- **Environment**: Use OpenAI Gym interface for `crowd_sim` to ensure compatibility with standard RL training loops.
- **Simulator**: Use `Python-RVO2` (Reciprocal Velocity Obstacles) to simulate human agents, as it provides a realistic baseline for collision avoidance.
- **Policy**: Implement SARL as the primary policy, with support for ORCA as a comparison baseline.

## Risks / Trade-offs

- **Dependency Risk**: `Python-RVO2` can be difficult to compile on certain systems (especially Windows). We may need to provide specific installation instructions or pre-built binaries.
- **Training Convergence**: DRL models for navigation can be sensitive to hyperparameters. We will use the hyperparameters recommended in the paper as a starting point.
- **Computational Cost**: Training with a large number of humans can be computationally expensive due to the O(N^2) complexity of the attention mechanism.
