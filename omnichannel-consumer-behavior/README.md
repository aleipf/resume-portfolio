# Omnichannel Consumer Behavior Analysis

A historical analytics project examining how anonymized physical retail visits align with app, web, and shopping activity.

## What the project demonstrates

- Multi-source behavioral data preparation
- Timestamp and UTC-offset normalization
- Panelist-level joins across physical and digital events
- Exact and fuzzy text classification
- Event-window analysis around store visits
- Exploratory consumer journey analysis

## Repository contents

- `omnichannel_consumer_behavior.ipynb` — cleaned portfolio version of the analysis

## Data

The original cleaned source data is not distributed. The notebook retains generic placeholder paths for visits, app activity, web activity, and shopping activity files.

Expected source directory:

```text
consumer_behavior_sample/
├── visits.txt
├── app.txt
├── web.txt
└── shopper.txt
```

## Notes

This analysis is observational. Event timing and behavioral associations should not be interpreted as causal effects. The notebook has been preserved primarily to demonstrate data integration and analytical methodology.
