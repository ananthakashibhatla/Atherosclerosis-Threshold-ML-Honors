# Iteration 01 Research Foundation

This file maps specific Iteration 01 design choices to the literature. The project-level bibliography is in `/RESEARCH_FOUNDATION.md`.

## Design Choice 1 — Logistic Plaque Growth

**Source:** Formanowicz et al. (2019), _A Control-Theoretic Model of Atherosclerosis_.  
https://doi.org/10.3390/ijms20030785

**Supports:** Using logistic behavior to model constrained plaque growth.

## Design Choice 2 — Threshold / Stability Analysis

**Source:** Bulelzai, Dubbeldam & Meijer (2014), _Bifurcation analysis of a model for atherosclerotic plaque evolution_.  
https://doi.org/10.1016/j.physd.2014.04.005

**Supports:** Studying nonlinear dynamics, plaque stability, bifurcation behavior, and model thresholds.

**Important:** This does not establish this repository's exact threshold ODE as a validated plaque equation.

## Design Choice 3 — Add Predictors Progressively

**Source:** Han et al. (2020), PARADIGM Registry.  
https://doi.org/10.1161/JAHA.119.013958

**Supports:** Comparing models built from progressively richer groups of predictors and using logistic-regression-style statistical baselines for plaque progression.

## Design Choice 4 — Predict Continuous Plaque Change and Classify Progression

**Source:** Bulant et al. (2024), _Data-driven models for the prediction of coronary atherosclerotic plaque progression/regression_.  
https://doi.org/10.1038/s41598-024-51508-7

**Supports:** A workflow involving data preprocessing, feature construction, continuous plaque-change prediction, progression/regression classification, and leakage-aware evaluation.

## Iteration 01 Research Position

The project combines these published ideas into a controlled teaching/research experiment:

```text
Logistic growth
+ nonlinear threshold behavior
+ plaque-progression prediction
+ progressively richer predictor sets
= Iteration 01 experimental design
```
