# Beyond Obstacle Avoidance: Social Navigation for Autonomous Robots
**Integrating Human Intent and Cultural Norms into Robotic Path Planning**

## Project Overview (專案介紹)
This repository contains the presentation slides (PDF format) and video demonstration materials for a project focusing on true social navigation for autonomous robots.

Traditional navigation systems divide path planning into global routes and local dynamic obstacle avoidance—optimizing purely for the shortest time and distance, explicitly treating humans as moving obstacles (**The Geometric Paradigm**). This project advocates for **The Social Imperative**: true social navigation requires robots to respect human intent, cultural norms, and invisible social boundaries. Bypassing social rules in favor of mathematical efficiency leads to systemic failures in real-world human environments.

## The Diagnostic to Cure Framework

### 1. Introduction: The Symptoms
We identified four specific scenarios where traditional geometric optimization creates social friction in human environments:
- **Late Reaction (Late Sharp Angles):** The robot maintains a straight trajectory until dangerously close to a pedestrian, then executes a sudden, sharp-angle evasion, startling them.
- **Conversation Disruption (Pass-Between):** The robot navigates directly between two individuals engaged in active conversation, severing their interaction and violating unwritten rules of social space (O-space).
- **Cultural Misalignment (Pass-Left):** In environments with implicit "Keep Right" norms, the robot aggressively overtakes from the left to pursue the mathematically shortest route, forcing pedestrians into unexpected evasive actions.
- **Frozen Robot (Traffic Deadlock):** In dense, slow-moving crowds, multiple pedestrian constraints create a mathematically empty intersection (zero safe pathways). The system defaults to zero velocity, paralyzing the robot and causing a severe traffic deadlock.

### 2. Related Work: The Pathologies
We deconstructed the mathematical architectures of existing legacy systems to understand their systemic failures:
- **VO (Velocity Obstacle):** Based on pure geometry. It guarantees mathematical collision avoidance but suffers from infinite, jittery oscillations (Non-Reciprocity), local deadlocks, and sensor hypersensitivity.
- **ORCA (Optimal Reciprocal Collision Avoidance):** Based on linear programming. It fails due to the *Heterogeneity Problem* (falsely assuming humans follow identical 50/50 reciprocity math) and freezes entirely in dense crowds.
- **CADRL (Collision Avoidance via Deep Reinforcement Learning):** While DRL produces emergent social norms and anticipation, standard MLPs require fixed input dimensions, creating the *Scalability Crisis* (blindness to the N+1 pedestrian). It also neglects human-human interactions and suffers from reward overfitting.

### 3. Approach: The Cure
To bridge the gap between mathematical collision avoidance and true social fluidity, we propose a novel **Attention Mechanism** integrated into the CADRL framework:
- **Dynamic Scalability:** The attention mechanism replaces the fixed-vector constraint of native CADRL. The system can now process an arbitrary number of agents seamlessly.
- **Contextual Filtering:** Functions exactly like human perception—automatically filtering out background noise to focus computational power on the agents that actually impact the trajectory (Primary Collision Risk).
- **Decoding Social Bonds:** Attention allows the network to model not just Robot-Human interactions, but *Human-Human* interactions, preventing the disruption of social groups and conversation links.

## Contents (資料清單)
The repository includes the following core materials:

1. **`Socially_Aware_Robot_Navigation.pdf`** 
   - A comprehensive slide deck exploring the conceptual framework, diagnostic symptoms, comparative pathologies of legacy systems, and the proposed Attention-Enhanced CADRL solution.
2. **`Socially_Aware_Robot_Navigation.mp4`** 
   - A video demonstration showcasing the trained robot agent navigating dynamically and safely in human environments, illustrating the successful integration of social awareness.

---
**Repository Owner:** [light810311](https://github.com/light810311)
