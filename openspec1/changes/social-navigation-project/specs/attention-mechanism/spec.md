## ADDED Requirements

### Requirement: Dynamic Agent Weighting
The policy SHALL use an attention mechanism to dynamically weight the importance of surrounding human agents.

#### Scenario: Dense Crowd Scaling
- **WHEN** The robot is surrounded by $N$ humans.
- **THEN** The attention network MUST generate $N$ weights ($\alpha_1, \dots, \alpha_n$) that sum to 1, representing the relative importance of each human to the robot's navigation.

### Requirement: Attentive Pooling
The state representations of surrounding agents SHALL be aggregated using an attentive pooling operation.

#### Scenario: Aggregated State Computation
- **WHEN** All attention weights are calculated.
- **THEN** The system MUST compute a single fixed-size vector representing the pooled environment state to be passed to the Value Network.
