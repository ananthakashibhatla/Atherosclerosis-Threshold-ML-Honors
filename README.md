# Atherosclerosis Threshold ML Honors Research

## Iterative Calculus II + Machine Learning Research Project

**Student Researcher:** Ananth Kashibhatla  
**Course:** Calculus II Honors  
**Term:** Fall 2026  
**Status:** Iteration 01 in development

## Project Vision

This repository documents an iterative computational research project studying simulated atherosclerotic plaque progression with a research-informed threshold-augmented logistic differential equation and progressively more capable machine-learning models.

The repository is intended to tell the full research story: mathematical assumptions, literature support, data generation, preprocessing, exploratory analysis, model development, results, faculty feedback, revisions, and iteration sign-off.

This project is a computational modeling study. It is **not a clinical diagnostic system**, and the simulated threshold used in this work is **not a validated clinical cutoff**.

## Mathematical Foundation

The standard constrained logistic model is

```text
dx/dt = a*x*(1 - x/c)
```

The simplified threshold-augmented research model used in this project is

```text
dx/dt = a*x*(1 - x/c)*(x/T - 1)
```

where:

- `x(t)` = normalized simulated plaque burden / IMT proxy
- `a` = effective progression rate
- `c` = upper/asymptotic plaque-burden parameter
- `T` = simulated dynamical threshold

The threshold equation is a simplified Calculus II research adaptation informed by published logistic plaque-growth modeling and nonlinear/bifurcation analyses of atherosclerosis. See `RESEARCH_FOUNDATION.md`.

## Current Iteration — Iteration 01: Regression Foundations

> **Central Research Question:** Using simulated plaque trajectories generated from the threshold-logistic differential equation, can simple linear and logistic regression models predict future plaque burden and future progression regime, and does adding additional trajectory-derived predictors improve performance?

### Problem A — Continuous Plaque Prediction

Compare:

- Simple Linear Regression
- Multiple Linear Regression

**Target:** future/final simulated plaque burden

### Problem B — Threshold-Regime Classification

Compare:

- Simple Logistic Regression
- Multiple Logistic Regression

**Target:** below-threshold / higher-progression regime classification derived from the simulated mathematical system.

## Iteration 01 Workflow

Published Atherosclerosis Research  
→ Mathematical Model Definition  
→ Threshold-Logistic ODE  
→ Synthetic Trajectory Generation  
→ Data Organization  
→ Data Cleaning  
→ Preprocessing  
→ Exploratory Data Analysis  
→ Feature Engineering  
→ Simple Linear Regression  
→ Multiple Linear Regression  
→ Simple Logistic Regression  
→ Multiple Logistic Regression  
→ Model Comparison  
→ Interpretation  
→ Faculty Feedback  
→ Revisions  
→ Iteration Sign-Off

## Repository Philosophy

Advanced modeling is intentionally outside the scope of Iteration 01.

Random forests, gradient boosting, SageMaker Canvas, advanced nonlinear parameter fitting, deep learning, and production deployment belong to later iterations. The first iteration establishes a transparent, reproducible baseline using methods already understood and interpretable within the Calculus II research context.

## Repository Structure

- `data/` — data-generation and dataset documentation
- `notebooks/` — Jupyter notebooks for each research stage
- `reports/` — figures, tables, summaries, and later presentation material
- `iterations/` — self-contained documentation for each research iteration
- `CHANGELOG.md` — project-level changes over time
- `DECISIONS.md` — research and engineering decisions
- `FACULTY_FEEDBACK.md` — faculty comments and responses
- `RESEARCH_FOUNDATION.md` — literature supporting the mathematical and modeling choices
