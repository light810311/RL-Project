## ADDED Requirements

### Requirement: Gym-compatible Environment
The simulation environment must implement the OpenAI Gym interface, providing `reset()`, `step()`, and `render()` methods.

#### Scenario: Environment Reset
- **WHEN** the `reset()` method is called
- **THEN** the robot and humans are initialized to their starting positions, and the initial state of the environment is returned.

#### Scenario: Environment Step
- **WHEN** the `step(action)` method is called with a valid robot action
- **THEN** the simulator updates the positions of all agents (using ORCA for humans and the provided action for the robot), checks for collisions or goal reaching, and returns the next state, reward, done flag, and info dictionary.

### Requirement: RVO2 Simulation
The environment must use the `Python-RVO2` library to simulate human movement according to the Reciprocal Velocity Obstacles model.

#### Scenario: Human Collision Avoidance
- **WHEN** multiple humans are present in the simulation
- **THEN** they must move towards their respective goals while avoiding collisions with each other and the robot using the RVO2 algorithm.
