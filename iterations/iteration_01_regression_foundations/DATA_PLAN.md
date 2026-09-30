# Data Plan — Iteration 01

## Data Source

Iteration 01 uses synthetic trajectories numerically generated from:

```text
dx/dt = a*x*(1 - x/c)*(x/T - 1)
```

No patient-level data are used.

## Parameters to Vary

The initial simulation design will vary:

- `x0` — initial plaque burden
- `a` — effective progression rate
- `c` — upper/asymptotic parameter
- `T` — simulated dynamical threshold
- observation duration
- measurement-noise level

Exact parameter ranges should be documented before generation rather than silently hard-coded.

## Two Different Splits

### Within-Trajectory Forecast Window

For each trajectory:

```text
First 70% = observed
Final 30% = withheld future
```

Features must be computed only from the observed portion.

### Across-Trajectory ML Split

Complete trajectories are assigned to training/validation/testing groups.

Rows from one trajectory may not cross groups.

## Raw Table

Expected long-format fields:

- `trajectory_id`
- `time`
- `x_true`
- `x_observed`
- `x0`
- `a`
- `c`
- `T`
- `noise_level`

## Model-Ready Feature Table

One row per trajectory, with candidate fields such as:

- `x_initial`
- `x_last_observed`
- `observed_change`
- `observed_slope`
- `observed_mean`
- `observed_variance`
- `distance_from_T`
- `noise_level`
- `x_final`
- `future_regime`

## Preprocessing Checks

- shape and column names
- data types
- missing values
- duplicate rows
- invalid parameter ranges
- impossible plaque values
- class balance
- leakage checks
- summary statistics

## Data Versioning

Each generated dataset should record:
- generation date
- random seed
- equation version
- parameter ranges
- noise design
- number of trajectories
