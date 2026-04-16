# RL-Project: Hospital Social Navigation via SARL
**會「察言觀色」的機器人 - 社交感知強化學習在醫院導航的應用**

## Project Overview (專案介紹)
This repository contains the presentation, report, and demonstration materials for the project **"Hospital Social Navigation via SARL"**. 

The project focuses on applying Deep Reinforcement Learning (DRL) techniques, specifically **Socially Aware Reinforcement Learning (SARL)**, to enable autonomous robots to navigate seamlessly through highly dynamic and crowded environments like hospitals. 

The primary goal is to develop a robot that can "Read the Room" (會「察言觀色」的機器人)—understanding human trajectories, personal spaces, and social norms to avoid collisions and navigate efficiently without causing discomfort to surrounding pedestrians.

## Contents (資料清單)
The repository includes the following core materials:

1. **`Hospital_Social_Navigation_via_SARL.pdf`** 
   - A detailed document/report exploring the methodologies, model architecture (SARL), simulation environment details, and performance evaluations of the reinforcement learning approach.
2. **`Hospital_Social_Navigation_via_SARL.pptx`** 
   - The presentation slides used for explaining the project. It covers the motivation, RL formulation (states, actions, reward functions), and visualizes the experimental findings.
3. **`會「察言觀色」的機器人.mp4`** 
   - A video demonstration showcasing the trained robot agent in action. It illustrates how the robot perceives moving pedestrians, adapts its trajectory dynamically, and reaches its goals in a socially compliant manner.

## Key Concepts (核心技術概念)
- **Reinforcement Learning (強化學習):** The robot acts as an agent learning to map sensory states (its own kinematics and observed pedestrians) to actions (steering and speed adjustments) to maximize cumulative rewards over time.
- **Socially Aware Navigation (社交感知導航):** Incorporates social constraints, such as maintaining a comfortable proxemic distance from pedestrians and anticipating human-human interactions to ensure safe passage.
- **SARL (Socially Aware Reinforcement Learning):** An advanced architecture that uses attention mechanisms or spatial pooling models to effectively capture collective human interactions and predict intent.

## Motivation & Application (動機與應用場景)
Hospitals present particularly challenging scenarios for autonomous platforms due to the presence of vulnerable patients, fast-moving medical staff, and narrow corridors. Navigating these spaces requires more than just obstacle avoidance—it requires social intelligence. This project demonstrates a robust solution enabling a robot to adhere to implicit human behavioral rules, making autonomous hospital delivery, patrol, or assistance tasks smoother and safer.

---
**Repository Owner:** [light810311](https://github.com/light810311)
