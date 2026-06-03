## Why

To implement a functional social navigation framework based on the "Attention-Enhanced CADRL" research. Traditional geometric navigation (VO, ORCA) fails in dense crowds, and legacy DRL (CADRL) has scalability issues. This project aims to provide a scalable, attention-based solution as described in the ICRA 2019 foundational paper.

## What Changes

- Initialize a Python-based Reinforcement Learning project structure.
- Define modular classes for Agents (Human, Robot) and их state representations.
- Implement the core logic for the Attention-Enhanced policy, including Self-Attention and Attentive Pooling mechanisms.
- Setup a modular simulation environment to test the four failure scenarios (Late Reaction, Conversation Disruption, Cultural Misalignment, Frozen Robot).

## Capabilities

### New Capabilities
- `agent-architecture`: Defines the state and action spaces for humans and robots, following the ICRA 2019 joint modeling approach.
- `attention-mechanism`: Implements the Self-Attention layer to dynamically weight the importance of surrounding agents in dense crowds.
- `social-navigation-env`: A simulation environment capable of modeling Human-Robot and Human-Human interactions.
- `performance-metrics`: Tools to measure social compliance, safety, and efficiency.

### Modified Capabilities
- None (Initial project generation).

## Impact

- **Project Root**: Introduces a new directory structure for source code (`src/`), configuration (`configs/`), and experiments (`experiments/`).
- **Dependencies**: Requires Python 3.x, PyTorch (for the attention mechanism), and potentially OpenAI Gym/Gymnasium for the environment interface.
