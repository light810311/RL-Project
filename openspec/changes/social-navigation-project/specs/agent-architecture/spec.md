## ADDED Requirements

### Requirement: Joint State Representation
The system SHALL represent the robot and human agents in a joint state space that includes both observable and internal states.

#### Scenario: Robot State Observation
- **WHEN** The robot agent is initialized.
- **THEN** Its state MUST include position ($p_x, p_y$), velocity ($v_x, v_y$), radius ($R$), and goal position ($g_x, g_y$).

### Requirement: Kinematic Constraints
Agent actions SHALL be governed by kinematic constraints to ensure realistic movement.

#### Scenario: Velocity Control
- **WHEN** A velocity action is applied to the agent.
- **THEN** The resultant movement MUST respect maximum speed ($v_{max}$) and rotation speed ($\omega_{max}$) limits.
