# Notebook Plan — Iteration 01

Notebooks will be added incrementally rather than all at once.

## Planned Order

1. `01_problem_and_data_generation.ipynb`
   - define the threshold-logistic ODE
   - select initial parameter ranges
   - generate first synthetic trajectories

2. `02_data_cleaning_preprocessing.ipynb`
   - inspect shape/types
   - missingness/duplicates/range checks
   - build observed vs future windows

3. `03_exploratory_data_analysis.ipynb`
   - distributions
   - trajectory plots
   - correlations
   - threshold-regime balance

4. `04_linear_regression_baselines.ipynb`
   - one predictor
   - progressively add predictors
   - compare R², MAE, RMSE

5. `05_logistic_regression_baselines.ipynb`
   - one predictor
   - progressively add predictors
   - compare accuracy, precision, recall, F1, ROC-AUC

6. `06_iteration_01_model_comparison.ipynb`
   - summarize model progression
   - analyze behavior near T
   - identify limitations and next questions

## Rule

Each notebook should answer one research stage clearly and should log conclusions in the iteration documentation.
