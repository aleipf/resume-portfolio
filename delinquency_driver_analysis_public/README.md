# Year-over-Year Delinquency Driver Analysis

A self-contained portfolio project demonstrating how to analyze a change in delinquency between two origination cohorts using synthetic consumer-credit data.

## Repository contents

| File | Description |
|---|---|
| `delinquency_driver_analysis.ipynb` | Complete, reproducible analysis with synthetic data generated inside the notebook. |
| `README.md` | Project overview and run instructions. |

## What the notebook demonstrates

- synthetic cohort generation
- feature engineering
- regularized logistic regression
- stratified cross-validation
- holdout ROC and precision-recall evaluation
- threshold tradeoff analysis
- coefficient interpretation
- holdout permutation importance
- cohort and segment analysis
- composition versus within-segment rate decomposition

## Key definition

**Delinquency:** `dlq_code` in `{2, 3, 4, 5}` is classified as delinquent. Other codes are classified as current.

## Methodological framing

This is an **observational driver analysis**, not a causal study.

The logistic model estimates adjusted associations between the included features and delinquency. The two-part decomposition separates the observed year-over-year rate change into:

1. a **composition effect** from changing segment proportions, and
2. a **within-segment effect** from changing delinquency rates inside those segments.

Each feature is decomposed separately, so percentages from different decompositions should not be summed.

## Data

All records are generated inside the notebook. The repository contains no employer data, customer records, personally identifiable information, or proprietary business results.

The synthetic schema uses generic analytical fields such as `site_id`, `rating_code_calc`, `trans_union_score`, `app_type`, `app_stat`, purchase amounts, loan amounts, and `dlq_code`.

## Running the notebook

Use Python 3.10 or newer.

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
jupyter notebook delinquency_driver_analysis.ipynb
```

Run all cells from top to bottom.

## Limitations

- The dataset is synthetic and does not represent any real portfolio.
- Logistic regression and decomposition identify associations, not causal effects.
- Results depend on the generated sample, selected features, and segmentation.
- Operational threshold selection requires explicit cost assumptions.
