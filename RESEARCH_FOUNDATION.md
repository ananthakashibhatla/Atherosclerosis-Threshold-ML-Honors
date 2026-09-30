# Research Foundation

This document records the literature supporting the mathematical and machine-learning design of the project.

## Important Scientific Boundary

The exact threshold-augmented equation used in this repository is a **simplified research model for controlled computational experimentation**. It is not claimed to be a validated clinical law of atherosclerotic plaque progression.

The literature supports the ingredients used to construct the model: constrained logistic plaque growth, nonlinear plaque dynamics and threshold/bifurcation behavior, and data-driven prediction of plaque progression.

## 1. Logistic / Constrained Plaque Growth

**Formanowicz D, Krawczyk JB, Perek B, Formanowicz P. (2019). _A Control-Theoretic Model of Atherosclerosis._ International Journal of Molecular Sciences, 20(3), 785.**  
DOI: https://doi.org/10.3390/ijms20030785  
Open access: https://pmc.ncbi.nlm.nih.gov/articles/PMC6387061/

### Relevance
The authors model atherosclerotic plaque progression using nonlinear differential equations and explicitly use a logistic function to represent constrained plaque growth.

### Project Use
Supports beginning from the ordinary logistic form:

```text
dx/dt = a*x*(1 - x/c)
```

---

## 2. Nonlinear Dynamics, Stability, and Threshold Behavior

**Bulelzai MAK, Dubbeldam JLA, Meijer HGE. (2014). _Bifurcation analysis of a model for atherosclerotic plaque evolution._ Physica D: Nonlinear Phenomena, 278–279, 31–43.**  
DOI: https://doi.org/10.1016/j.physd.2014.04.005

### Relevance
The study performs bifurcation analysis of an atherosclerosis model and reports a threshold in a model parameter separating plaque-growth and plaque-stability behavior.

### Project Use
Supports investigating dynamical thresholds and stability behavior in a simplified Calculus II setting.

---

## 3. Prediction with Progressively Richer Predictor Sets

**Han D, et al. (2020). _Machine Learning Framework to Identify Individuals at Risk of Rapid Progression of Coronary Atherosclerosis: From the PARADIGM Registry._ Journal of the American Heart Association, 9(5), e013958.**  
DOI: https://doi.org/10.1161/JAHA.119.013958  
Open access: https://pmc.ncbi.nlm.nih.gov/articles/PMC7335586/

### Relevance
The study predicts rapid coronary plaque progression and evaluates models using progressively richer sets of clinical and plaque features. It also compares ML approaches with logistic regression.

### Project Use
Supports the Iteration 01 strategy of beginning with a simple predictor and then adding additional predictors to test whether predictive performance improves.

---

## 4. Continuous Plaque-Change Prediction and Progression/Regression Classification

**Bulant CA, Boroni GA, Bass R, et al. (2024). _Data-driven models for the prediction of coronary atherosclerotic plaque progression/regression._ Scientific Reports, 14, 1493.**  
DOI: https://doi.org/10.1038/s41598-024-51508-7  
Open access: https://pmc.ncbi.nlm.nih.gov/articles/PMC10794448/

### Relevance
The study predicts future change in percent atheroma volume from baseline information and evaluates plaque progression/regression. It emphasizes preprocessing, feature construction, leakage-aware validation, regression, and classification.

### Project Use
Supports treating plaque evolution as both:
1. a continuous prediction problem, and
2. a progression/regime classification problem.

---

## Research Logic Used in This Repository

```text
Published logistic plaque-growth modeling
        +
Published nonlinear / threshold behavior
        +
Published plaque-progression prediction studies
        ↓
Simplified threshold-logistic Calculus II model
        ↓
Controlled simulated plaque trajectories
        ↓
Interpretable regression baselines
        ↓
Later advanced ML / AWS iterations
```
