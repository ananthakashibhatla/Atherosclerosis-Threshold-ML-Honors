# Mathematical Foundation — Iteration 01

## 1. Ordinary Logistic Foundation

The starting point is the constrained logistic form:

```text
dx/dt = a*x*(1 - x/c)
```

where:

- `x(t)` = normalized simulated plaque burden / IMT proxy
- `a > 0` = effective progression-rate parameter
- `c > 0` = upper/asymptotic plaque-burden parameter

Published atherosclerosis modeling has used logistic behavior to represent constrained plaque growth.

## 2. Threshold-Augmented Research Equation

Iteration 01 uses the simplified equation:

```text
dx/dt = a*x*(1 - x/c)*(x/T - 1)
```

Assume:

```text
a > 0
0 < T < c
```

where `T` is a **simulated dynamical threshold**.

## 3. Equilibria

Set the derivative equal to zero:

```text
a*x*(1 - x/c)*(x/T - 1) = 0
```

Therefore:

```text
x = 0
x = T
x = c
```

## 4. Sign Analysis

### Region A: 0 < x < T

- `x > 0`
- `1 - x/c > 0`
- `x/T - 1 < 0`

Therefore:

```text
dx/dt < 0
```

The trajectory moves downward toward the lower equilibrium.

### Region B: T < x < c

All three variable factors are positive, so:

```text
dx/dt > 0
```

The trajectory moves upward toward `c`.

### Region C: x > c

- `1 - x/c < 0`

Therefore:

```text
dx/dt < 0
```

The trajectory moves downward toward `c`.

## 5. Stability Interpretation

Under the stated assumptions:

- `x = 0` behaves as a stable equilibrium.
- `x = T` behaves as an unstable equilibrium.
- `x = c` behaves as a stable equilibrium.

Thus `T` separates two mathematical trajectory regimes.

## 6. Important Classification Consequence

In the ideal deterministic autonomous equation, a trajectory does not normally cross through the unstable equilibrium `T`; the side of `T` helps determine its direction of motion.

Therefore Iteration 01 will primarily classify **future regime relative to T**, rather than claim to predict a clinical threshold-crossing event.

Measurement noise can make the observed state uncertain even when the underlying simulated trajectory is known.

## 7. Scientific Boundary

This equation is a simplified research adaptation for a Calculus II computational experiment. `T` is not a clinical diagnostic threshold.
