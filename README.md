# Predicting Disease Progression: A Complete, Reproducible Analysis

An end-to-end quantitative analysis in Python, built to demonstrate the full workflow behind defensible data work: data validation, baseline modeling, regularization with cross-validation, residual diagnostics, statistical inference with multiple-comparison correction, and A/B test design with power analysis.

## What's inside

**`portfolio_starter_analysis.ipynb`** — a single, fully executable Jupyter notebook covering:

| Section | Topic | Key result |
|---|---|---|
| 2 | Data validation | Missing-value checks, distribution review, correlation screening |
| 3 | Baseline linear regression | Test R² = 0.485, RMSE = 53.4 |
| 4 | Residual diagnostics | Heteroscedasticity identified and interpreted |
| 5 | Ridge regression via 5-fold CV | Honest result: regularization offers minimal gain here |
| 6 | OLS inference + Bonferroni correction | bmi, bp, s5, and sex remain significant after correction |
| 7 | A/B test simulation + power analysis | 3,835 users/group required for 80% power; simulation confirms 80.5% empirical detection vs. 12.3% at one-tenth the sample |
| 8 | Conclusions & limitations | Written in plain language, limitations stated explicitly |

## Skills demonstrated

- Predictive modeling: regression, regularization, cross-validation, model validation
- Statistical inference: OLS, confidence intervals, p-values, multiple-comparison correction
- Experiment design: power analysis, A/B testing, simulation-based verification
- Programming: Python (pandas, NumPy, scikit-learn, statsmodels, matplotlib), reproducible notebooks with fixed random seeds
- Communication: every section includes interpretation of the output and stated limitations

## How to run

```bash
pip install -r requirements.txt
jupyter notebook portfolio_starter_analysis.ipynb
```

Then run all cells top to bottom. No data download is required — the dataset (`sklearn.datasets.load_diabetes`, 442 patients, 10 baseline clinical measurements) ships with scikit-learn. A fixed random seed makes every result exactly reproducible.

## Dataset

The [diabetes dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#diabetes-dataset) from scikit-learn: ten baseline variables (age, sex, BMI, blood pressure, and six serum measurements) for 442 diabetes patients, with a quantitative measure of disease progression one year later as the target.

## Notes

This is a demonstration analysis on a small public dataset. Its purpose is to show method — validation discipline, honest reporting of null results, correct inference procedure, and clear written reasoning — rather than to produce novel clinical findings.
