# Problem Statement

Atherosclerotic plaque progression is a dynamic process that has been studied with mathematical models and data-driven prediction methods.

For Iteration 01, the research problem is intentionally simplified:

1. Start from a research-informed logistic model of constrained plaque growth.
2. Add a simulated dynamical threshold `T` to create two mathematical progression regimes.
3. Generate controlled plaque trajectories from the resulting ODE.
4. Use only the observed portion of each trajectory to predict the withheld future.
5. Test whether simple linear and logistic regression models improve as additional interpretable predictors are added.

## Continuous Problem

**Question:** Can observed trajectory information predict future/final simulated plaque burden?

**Target:** continuous future plaque value, initially `x_final`.

## Classification Problem

**Question:** Can observed trajectory information identify the future mathematical regime relative to `T`?

**Target:** a binary future-regime label derived from the simulated system.

## Why This Problem Is Useful

Because the true generating equation is known, the project can directly study where simple statistical models approximate the nonlinear system well and where they fail, including near the unstable threshold and under measurement noise.
