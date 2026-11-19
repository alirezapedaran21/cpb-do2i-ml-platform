# Data Card — CPB DO₂i Forecasting

## Status

Draft. Complete this document before publishing model results.

## Source and access

- Dataset/source name:
- Dataset version/release:
- Source URL:
- Date accessed:
- Data-use agreement/license:
- Attribution text required by source:
- Is redistribution permitted? (Do not assume yes.)

## Population and unit of analysis

- Unit of analysis: CPB case / patient encounter.
- Number of cases:
- Number of time-series rows:
- Inclusion/exclusion criteria:
- Missingness and data-quality rules:

## Data fields

For every input and target, document the definition, unit, source channel, timestamp semantics, expected range, and when the value becomes available to the prediction system.

Particular attention is required for laboratory measurements: distinguish sample collection time, result time, and the time at which the result would actually be available to a perfusionist.

## Temporal construction

- Nominal sampling interval: 10 seconds (verify per source).
- Prediction horizons: +5 and +10 minutes.
- Target alignment/tolerance:
- Handling of irregular intervals:
- Handling of stale laboratory measurements:
- Handling of gaps and missing values:

## Leakage controls

- Split by case ID, never by individual time-series rows.
- Fit scalers/imputers only on training cases.
- Ensure all inputs are available at prediction time.
- Ensure windows do not cross case boundaries.
- Keep the test set untouched during model selection.

## Privacy and redistribution

Do not commit raw patient-level data, identifiers, or row-level derived datasets. Confirm source terms before publishing derived artifacts or model weights.

## Known limitations

- Retrospective dataset may not represent prospective deployment conditions.
- Sampling and measurement practices may differ between institutions.
- Model performance does not establish clinical benefit or safety.
