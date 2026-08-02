# Week 11 – Final Project Update

## Status

The project has now been completed and prepared for final submission.

This week, the final forecasting notebook was cleaned and reorganised into a structured end-to-end workflow covering data loading, preprocessing, feature engineering, model development, evaluation and interpretability.

The final controlled comparison used 3,764 training observations and 432 unseen test observations from 2024. Six forecasting approaches were evaluated using the same test period.

Random Forest produced the strongest overall performance, achieving:

- Mean Absolute Percentage Error of 6.763%;
- Mean Absolute Error of USD 3.935 billion;
- Root Mean Squared Error of USD 6.850 billion; and
- R-squared of 0.990.

The final evaluation also included:

- country-level performance analysis;
- comparison of seasonal history alone with seasonal history plus external indicators;
- SHAP feature analysis;
- Random Forest tree-percentile uncertainty ranges;
- ablation analysis;
- scenario analysis; and
- reproducibility testing.

The results showed that the exact 12-month historical trade lag provided the strongest forecasting signal. External indicators reduced overall percentage error, but their contribution was smaller and varied across indicators and evaluation metrics.

The final technical report was completed and updated to reflect the controlled model comparison and final evaluation results.

The final video demonstration was also completed and uploaded:

https://youtu.be/ZCa0ufGfsS4

## Final Deliverables Completed

- Final cleaned Jupyter notebook
- Development notebook retained as an audit trail
- Final technical report
- Final results and visualisations
- Updated GitHub README
- Final video demonstration

## Final Outcome

The project objectives were achieved. The work demonstrates that a pooled Random Forest model using exact seasonal trade history and selected lagged external indicators can produce accurate and interpretable monthly trade forecasts across multiple economies.

The final results also identify limitations in country-level consistency, evaluation using one holdout year and the use of uncalibrated uncertainty ranges. These have been documented as areas for future development.
