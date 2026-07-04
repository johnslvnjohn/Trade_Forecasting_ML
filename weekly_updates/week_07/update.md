# Week 7 Progress Update

## Work completed

This week focused on improving and validating the Random Forest forecasting model.

A true 12-month seasonal lag feature was created using the matching month from the previous year. This was checked carefully to ensure that the lag represented the same calendar month in the prior year rather than simply the previous 12 available records.

A controlled comparison was then completed between:

- A matched external-only Random Forest model
- A Random Forest model including the true 12-month seasonal trade lag

Both models used the same training data, 2024 test period and Random Forest settings. The only difference was the inclusion of the seasonal lag feature.

## Controlled model comparison

| Model | MAE (USD bn) | RMSE (USD bn) | R² | MAPE |
|---|---:|---:|---:|---:|
| Matched external-only Random Forest | 4.95 | 8.79 | 0.984 | 8.21% |
| Random Forest with true 12-month seasonal lag | 3.94 | 6.95 | 0.990 | 6.66% |

The seasonal model reduced Mean Absolute Error by approximately USD 1.01 billion and reduced MAPE from 8.21% to 6.66%.

## Country-level findings

The seasonal lag improved MAPE in 14 of the 18 economies analysed.

The largest improvements were observed in:

- Mexico
- Saudi Arabia
- Canada
- Indonesia
- Italy

However, performance worsened for:

- Argentina
- Germany
- United Kingdom
- Republic of Korea

This indicates that same-month-prior-year trade activity is useful for many countries, but its value differs across economies. The final model development will therefore consider country-specific feature selection rather than applying one identical feature set to all countries.

## Evidence produced

- Controlled model comparison table
- Country-level MAPE comparison table
- Chart showing the controlled impact of the seasonal lag on forecasting accuracy

## Next steps

- Save the updated modelling notebook and final charts in the repository.
- Review feature importance in the seasonal model.
- Test an advanced model such as Histogram-Based Gradient Boosting or XGBoost.
- Start refining the final forecasting approach and report documentation.
