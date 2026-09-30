# Data Dictionary

This file will be updated when the first synthetic dataset is generated.

## Raw / Simulation Variables

| Variable | Type | Meaning | Source |
|---|---|---|---|
| trajectory_id | identifier | Unique simulated trajectory | generated |
| time | numeric | Simulation time | ODE solver |
| x_true | numeric | Noise-free simulated plaque state | threshold-logistic ODE |
| x_observed | numeric | Observed plaque state after measurement noise | generated |
| x0 | numeric | Initial plaque state | simulation parameter |
| a | numeric | Effective progression-rate parameter | simulation parameter |
| c | numeric | Upper/asymptotic plaque parameter | simulation parameter |
| T | numeric | Simulated dynamical threshold | simulation parameter |
| noise_level | numeric | Controlled measurement-noise condition | experiment design |

## Planned Engineered Features

| Variable | Type | Meaning | Computed From |
|---|---|---|---|
| x_initial | numeric | First observed plaque value | observed 70% |
| x_last_observed | numeric | Last plaque value available to model | observed 70% |
| observed_change | numeric | Change across observed window | observed 70% |
| observed_slope | numeric | Estimated observed trajectory slope | observed 70% |
| observed_mean | numeric | Mean plaque state | observed 70% |
| observed_variance | numeric | Variance in observed plaque values | observed 70% |
| distance_from_T | numeric | Observed state relative to threshold | x_last_observed - T |
| x_final | numeric target | Final true plaque state | withheld future |
| future_regime | binary target | Final true state below/above T | withheld future |

## Important Rule

No predictor may use information from the withheld final 30% of a trajectory.
