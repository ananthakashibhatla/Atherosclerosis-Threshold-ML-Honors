# Data Directory

Iteration 01 uses **synthetic plaque trajectories generated from the project's threshold-logistic differential equation**. No patient-level clinical data are used in this iteration.

## Planned Structure

```text
data/
├── raw/        # direct ODE simulation output
├── interim/    # cleaned / reshaped trajectories
└── processed/  # model-ready trajectory-level feature table
```

Git does not preserve empty folders, so these directories should be created when the first datasets are generated.

## Raw Trajectory Variables

Planned variables include:

- `trajectory_id`
- `time`
- `x` — simulated plaque burden
- `x0` — initial plaque burden
- `a` — effective progression rate
- `c` — asymptotic upper parameter
- `T` — simulated dynamical threshold
- `noise_level`

## Important Boundary

`T` is a simulated mathematical threshold and must not be described as a validated clinical cutoff.

## Leakage Rule

All rows from a single trajectory must remain in the same train/validation/test group.
