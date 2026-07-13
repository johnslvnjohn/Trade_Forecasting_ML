## Current Status

The project has progressed beyond the initial MVP stage and is now in the
advanced evaluation and explainability phase.

Work completed by Week 8 includes:

- Collection and integration of monthly import and export data for 18 G20 economies.
- Integration of oil prices, commodity indices and macroeconomic indicators.
- Data cleaning, transformation and time-based feature engineering.
- Construction of seasonal trade features, including a 12-month trade lag.
- Training and evaluation of Linear Regression, Support Vector Regression,
  Random Forest, Histogram-Based Gradient Boosting, XGBoost and LSTM models.
- Comparison of history-only and history-plus-external-variable models.
- Country-level forecast error analysis.
- SHAP explainability analysis.
- Random Forest model-based prediction intervals.
- Feature ablation and economic scenario analysis.
- Repeatability testing of the final model.


## Current Best Model

The strongest model is the Seasonal Random Forest, using annual trade history,
monthly seasonality and lagged external indicators.

| Metric | Result |
|---|---:|
| MAE | USD 3.94 billion |
| RMSE | USD 6.95 billion |
| R² | 0.9902 |
| MAPE | 6.66% |

The model was trained using data before 2024 and evaluated on the held-out
January–December 2024 test period.

## Main Findings

- The 12-month historical trade lag was the strongest overall predictor.
- Base-metal prices were the strongest external predictor.
- The US dollar index and Federal Funds Rate added smaller predictive contributions.
- Crude-oil prices had limited marginal value in the pooled G20 model.
- External indicators reduced mean MAPE from approximately 7.01% to 6.66%.
- Random Forest tree-based prediction intervals achieved 94.44% overall
  empirical coverage.
- The LSTM underperformed the tree-based models, with a MAPE of 27.34%.

## Models Evaluated

- Linear Regression
- Support Vector Regression
- Random Forest Regression
- Seasonal Random Forest Regression
- Histogram-Based Gradient Boosting
- XGBoost
- Long Short-Term Memory neural network
