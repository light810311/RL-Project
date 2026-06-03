## ADDED Requirements

### Requirement: Self-Attention Mechanism
The policy network must implement a self-attention mechanism to weigh the importance of different human agents in the crowd.

#### Scenario: Attention Weight Calculation
- **WHEN** the robot perceives a set of human states
- **THEN** the network must calculate attention weights for each human, reflecting their relative importance for the robot's navigation decision.

### Requirement: Joint Interaction Modeling
The policy must jointly model Human-Robot and Human-Human interactions.

#### Scenario: Value Function Evaluation
- **WHEN** evaluating a state-action pair
- **THEN** the value function must consider the anticipated future states of both the robot and all humans, accounting for their mutual interactions.
