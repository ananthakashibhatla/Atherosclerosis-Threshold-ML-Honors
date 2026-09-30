# Research and Engineering Decisions

## Decision 001 — Use a Threshold-Augmented Logistic ODE

**Date:** 2026-09-30

**Decision:** Use the following simplified research equation as the mathematical generator for simulated plaque trajectories:

```text
dx/dt = a*x*(1 - x/c)*(x/T - 1)
```

**Reason:** Published work supports constrained logistic plaque growth and nonlinear/bifurcation behavior in atherosclerosis. The exact threshold-augmented equation used here is a simplified Calculus II research adaptation, not a validated clinical equation.

---

## Decision 002 — Treat T as a Simulated Dynamical Threshold

**Date:** 2026-09-30

**Decision:** `T` will be treated only as a simulated mathematical threshold.

**Reason:** The project must not imply that `T` is an established clinical cutoff.

---

## Decision 003 — Keep Iteration 01 Interpretable

**Date:** 2026-09-30

**Decision:** Limit Iteration 01 to linear regression and logistic regression, progressing from one predictor to multiple predictors.

**Reason:** Establish transparent baselines before introducing more complex ML.

---

## Decision 004 — Split by Trajectory

**Date:** 2026-09-30

**Decision:** Related rows from the same simulated trajectory must not be divided between training and testing groups.

**Reason:** Prevent data leakage and preserve honest evaluation.
