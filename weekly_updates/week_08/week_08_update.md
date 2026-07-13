# Week 8 Project Update

## Work Completed

During Week 8, the project moved from model development into advanced
evaluation, explainability and uncertainty analysis.

The following work was completed:

- Finalised the Seasonal Random Forest model using month, trade flow,
  12-month trade lag and lagged external indicators.
- Confirmed the final model performance on the 2024 held-out test period:
  - MAE: USD 3.94 billion
  - RMSE: USD 6.95 billion
  - R²: 0.9902
  - MAPE: 6.66%
- Completed LSTM model evaluation. The LSTM achieved a MAPE of 27.34%
  and underperformed the tree-based models.
- Used SHAP to explain both overall and external-variable contributions.
- Identified the 12-month trade lag as the dominant feature.
- Identified base metals as the strongest external variable.
- Generated country-level SHAP outputs for China, Australia and Saudi Arabia.
- Produced Random Forest model-based prediction intervals with overall
  empirical coverage of 94.44%.
- Completed feature-ablation analysis.
- Completed scenario analysis for oil prices, base metals and interest rates.
- Tested model repeatability using identical data, parameters and random seed.
- Produced a final China export forecast dashboard showing actual values,
  predictions and uncertainty ranges.

## Key Findings

The Seasonal Random Forest remained the strongest model. Historical annual
trade patterns explained most of the predictive performance, while external
variables produced smaller incremental improvements.

Removing the base-metals index increased MAPE by 0.200 percentage points,
while removing the US dollar index increased MAPE by 0.151 percentage points.
Removing crude oil increased MAPE by only 0.008 percentage points.

A 20% increase in oil prices increased predicted Saudi Arabian trade by only
0.40%. A 15% decrease in base-metal prices reduced predicted Australian trade
by 1.99%.

## Challenges and Limitations

- The pooled model may conceal differences between individual economies.
- Random Forest predictions are smoother than actual trade and can miss
  sudden turning points.
- Country-level prediction-interval coverage varied.
- Highly correlated commodity variables can divide feature importance.
- Scenario results represent model responses and should not be interpreted
  as causal economic estimates.

## Next Stage

The next stage is to consolidate the final model results, update the
requirements specification and complete the technical report.
