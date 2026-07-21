# Deep Learning Attribution Classification

A historical TensorFlow project modernized into a TensorFlow 2.x/Keras binary-classification workflow.

## Objective

Predict the binary `is_attributed` field from click-record identifiers and time-derived features.

## Source-supported context

The original notebook:

- loads `train.csv` from a local path containing `kaggle-talkingdata2/competition_files`;
- uses the fields `ip`, `app`, `device`, `os`, `channel`, `click_time`, and `is_attributed`;
- labels saved TensorFlow checkpoints with `ClickThroughRate`;
- implements the model with TensorFlow 1.x sessions and placeholders.

Those details suggest a historical Kaggle-style click-attribution or click-through modeling exercise. However, the notebook does not contain enough documentation to verify a specific competition, official dataset title, sponsor, or collection methodology. This portfolio version therefore does not make those claims.

## What the project demonstrates

- TensorFlow 2.x and Keras
- Feed-forward neural-network classification
- Feature engineering from timestamps
- Train, validation, and test separation
- Class-weighted training for an imbalanced outcome
- Early stopping and adaptive learning-rate reduction
- ROC-AUC and precision-recall evaluation
- Validation-based threshold selection
- Keras model export

## Repository contents

- `deep_learning_click_prediction.ipynb` — cleaned and modernized modeling workflow
- `README.md` — project overview, provenance note, and run instructions

## Data

The historical source dataset is not distributed. The notebook accepts a local `train.csv` containing:

- `ip`
- `app`
- `device`
- `os`
- `channel`
- `click_time`
- `is_attributed`

When the file is not present, the notebook generates synthetic data with the same field names and a binary target. The synthetic fallback supports reproducibility of the code only; it does not reproduce the original dataset, provenance, or results.

## Running the notebook

Use Python 3.10 or newer.

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow jupyter
jupyter notebook deep_learning_click_prediction.ipynb
```

Run all cells from top to bottom.

## Modernization notes

The source notebook used TensorFlow 1.x sessions, placeholders, manually defined weights and biases, fixed-epoch experiments, and checkpoint restoration. This portfolio version updates that workflow to TensorFlow 2.x/Keras and adds modern training and evaluation practices while retaining the observed inputs and `is_attributed` target.

## Limitations

- The exact external provenance of the source dataset is not verified from the notebook alone.
- Synthetic fallback results are illustrative and must not be presented as historical model performance.
- The compact example treats high-cardinality identifiers as numeric features.
- Production validation should use time-based splits and explicit operational cost assumptions.
- The model identifies predictive patterns, not causal effects.
