# Member Attrition Modeling

A historical portfolio project examining member attrition through behavioral feature engineering and supervised classification.

## Project contents

- `interpretable_attrition_model.ipynb` — logistic-regression workflow emphasizing interpretability, coefficient review, and classification performance.
- `attrition_model_development.ipynb` — broader model-development workflow with monthly transaction features, logistic regression, random forest, and XGBoost.

## What the project demonstrates

- Behavioral feature engineering from account and transaction history
- Time-based aggregation and tenure features
- Handling a highly imbalanced attrition outcome
- Stratified train/test splitting
- Logistic regression for interpretable modeling
- Random forest and XGBoost comparison
- Confusion matrices, classification reports, and feature importance

## Data and confidentiality

The original source data, database connections, SQL queries, member identifiers, and organization-specific infrastructure are not included. The notebooks use generic local-file placeholders:

- `member_attrition_features.csv`
- `member_transactions.csv`
- `member_status_history.csv`

Compatible anonymized extracts are required to rerun the notebooks.

## Historical context

This work was originally developed in 2020 and is included as a historical example of an iterative attrition-modeling workflow. The notebooks received limited portfolio cleanup rather than a full modernization so the original analytical process remains visible.

## Method note

The supplied `AttritionModelCanonV4(2)` notebook does **not** contain TensorFlow or Keras code. Its implemented models are logistic regression, random forest, and XGBoost. The README reflects the methods actually present in the source notebook.

## Limitations

- Source data is not distributed, so the notebooks are not self-contained.
- The notebooks predate current production ML practices and would benefit from modern pipelines, leakage checks, calibration, and time-based validation before operational use.
- Model outputs are cleared to prevent disclosure of historical internal results.
