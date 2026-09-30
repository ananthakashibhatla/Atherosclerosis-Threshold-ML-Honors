# Model Plan — Iteration 01

Iteration 01 intentionally uses simple, interpretable models.

# Part A — Linear Regression

## Target

Initial target:

```text
x_final
```

## Model LR-1 — One Predictor

```text
x_last_observed -> x_final
```

Purpose: establish the simplest useful baseline.

## Model LR-2 — Add Observed Trend

```text
x_last_observed + observed_slope -> x_final
```

## Model LR-3 — Add Threshold Information

```text
x_last_observed + observed_slope + distance_from_T -> x_final
```

## Model LR-4 — Add Variability / Noise Context

Candidate predictors:

```text
x_last_observed
observed_slope
distance_from_T
observed_variance
noise_level
```

## Regression Metrics

- R²
- MAE
- RMSE
- actual vs predicted plot
- residual analysis

---

# Part B — Logistic Regression

## Target

Initial binary target:

```text
future_regime
0 = final true state below T
1 = final true state above T
```

This represents a mathematical regime, not a clinical outcome.

## Model LOG-1 — One Predictor

```text
x_last_observed -> future_regime
```

## Model LOG-2 — Add Trend

```text
x_last_observed + observed_slope -> future_regime
```

## Model LOG-3 — Add Threshold Information

```text
x_last_observed + observed_slope + distance_from_T -> future_regime
```

## Model LOG-4 — Add Variability / Noise Context

Candidate predictors:

```text
x_last_observed
observed_slope
distance_from_T
observed_variance
noise_level
```

## Classification Metrics

- accuracy
- precision
- recall
- F1
- ROC-AUC
- confusion matrix

---

# Comparison Question

For both model families:

> Does adding additional trajectory-derived information materially improve held-out performance compared with the simplest baseline?

## Special Analysis

Report model performance by:
- distance from `T`
- measurement-noise level

This will help identify where linear/logistic baselines break down relative to the nonlinear generating system.
