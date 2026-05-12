## Why

Implement the "Crowd-Robot Interaction: Crowd-aware Robot Navigation with Attention-based Deep Reinforcement Learning" project. This work goes beyond first-order Human-Robot interaction by explicitly modeling Crowd-Robot Interaction (CRI) using a self-attention mechanism and jointly modeling Human-Robot and Human-Human interactions. This allows robots to navigate in crowded spaces more effectively and in a socially-compliant manner.

## What Changes

The project involves implementing:
1.  A simulation environment (`crowd_sim`) based on `OpenAI Gym` and `Python-RVO2`.
2.  A reinforcement learning framework (`crowd_nav`) for training and testing navigation policies.
3.  The Socially Attentive Reinforcement Learning (SARL) policy which captures human-human interactions and learns the collective importance of neighboring humans.

## Capabilities

### New Capabilities
- `crowd-sim-env`: A simulation environment for crowd navigation that supports various human behaviors and robot policies.
- `sarl-policy`: A deep reinforcement learning policy that uses an attention mechanism to model interactions in a crowd.
- `crowd-nav-framework`: A framework for training, testing, and visualizing the performance of crowd-aware navigation policies.

### Modified Capabilities
- None

## Impact

- **New Files**: Implementation of `crowd_sim/` and `crowd_nav/` directories.
- **Dependencies**: Requires `Python-RVO2`, `pytorch`, `gym`, `matplotlib`, and `numpy`.
- **System**: The project will be contained within the `RL-Project` workspace.
