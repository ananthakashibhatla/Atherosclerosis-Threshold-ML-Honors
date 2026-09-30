# Research Questions — Iteration 01

## Primary Question

Using simulated plaque trajectories generated from the threshold-logistic ODE, do progressively richer predictor sets improve future plaque prediction and threshold-regime classification?

## RQ1 — Continuous Prediction

How well does a one-predictor linear regression model predict final plaque burden?

## RQ2 — Added Predictors

Does adding trajectory information such as observed slope and distance from `T` improve linear-regression performance?

## RQ3 — Regime Classification

How well does a one-predictor logistic regression classifier identify the future regime relative to `T`?

## RQ4 — Multiple-Predictor Classification

Does adding slope, distance from `T`, and variability improve logistic-regression classification?

## RQ5 — Threshold Difficulty

Does prediction error change as the observed trajectory becomes closer to `T`?

## RQ6 — Measurement Noise

How does controlled measurement noise affect the two baseline model families?

## Iteration 01 Hypothesis Policy

No model is assumed to win in advance. Results will be reported from held-out trajectories using predefined evaluation metrics.
