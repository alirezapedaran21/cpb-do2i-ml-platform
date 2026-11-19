# Model Card — CPB DO₂i Forecaster

## Status

Draft. No model in this repository has yet passed the reproducibility and deployment checks.

## Intended use

Research and engineering demonstration of short-horizon DO₂i forecasting during CPB.

## Out-of-scope use

Not for diagnosis, treatment selection, perfusionist configuration recommendations, autonomous control, or direct patient care. Not clinically validated.

## Prediction task

- Inputs: time-series features available at the prediction timestamp.
- Target: DO₂i at +5 and +10 minutes.
- Sampling: nominally 10 seconds; verify actual data behavior.

## Candidate models

- Persistence baseline (future DO₂i equals current DO₂i).
- Existing tree-based baseline(s), including the prior delta-XGBoost experiment.
- Existing GRU checkpoint.

## Evaluation

Report MAE, RMSE, and R² for each horizon, plus per-case distributions and uncertainty intervals. Report performance by relevant subgroups only where sample sizes and data permissions support responsible analysis.

## Data and split

Document dataset provenance, case-level split manifest, preprocessing, and leakage checks in the Data Card and experiment record.

## Limitations and risks

Retrospective predictive accuracy does not demonstrate clinical utility, safety, or transportability. Forecast errors can be clinically consequential. Predictions must not be converted into treatment recommendations without prospective clinical validation and appropriate regulatory, institutional, and governance review.
