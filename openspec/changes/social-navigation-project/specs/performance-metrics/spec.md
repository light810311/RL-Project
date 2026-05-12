## ADDED Requirements

### Requirement: Safety and Efficiency Scoring
The system SHALL track safety and efficiency metrics for each navigation episode.

#### Scenario: Collision Rate Calculation
- **WHEN** An episode concludes.
- **THEN** The system MUST report the total number of collisions and the percentage of successful goal reaches.

### Requirement: Social Compliance Metric
The system SHALL measure compliance with social norms.

#### Scenario: Personal Space Violation
- **WHEN** The robot enters a human's personal space radius.
- **THEN** The system MUST record a "Social Discomfort" event and apply a corresponding penalty to the DRL reward function.
