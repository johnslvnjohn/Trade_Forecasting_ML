# Week 5 Update: Feature Engineering and Initial Model Development

## What I Worked On

This week, I prepared the dataset for machine-learning modelling and developed the first set of baseline forecasting models.

I used the cleaned monthly trade dataset for the selected G20 economies and combined it with external oil, commodity-price and macroeconomic variables. The modelling period covers January 2014 to December 2024.

## Data Preparation Completed

* Created time variables including year, month and quarter.
* Used `log1p(primaryValue)` as the target variable to reduce the influence of very large trade values.
* Encoded country name and trade-flow direction for use in the models.
* Created a time-based train/test split:

  * Training data: January 2014 to December 2023
  * Test data: January 2024 to December 2024
* Tested lagged external variables to improve the realism of the forecasting design.

## Models Developed

The following baseline regression models were trained and evaluated:

* Linear Regression
* Random Forest Regression
* Support Vector Regression

## Initial Model Results

| Model                     | MAE (USD bn) | RMSE (USD bn) |    R² | MAPE (%) |
| ------------------------- | -----------: | ------------: | ----: | -------: |
| Linear Regression         |        10.25 |         19.56 | 0.922 |    13.73 |
| Random Forest             |         5.02 |          8.94 | 0.984 |     8.28 |
| Support Vector Regression |        13.32 |         18.05 | 0.934 |    33.72 |

## Key Finding

Random Forest produced the strongest result among the baseline models. It achieved the lowest MAE, RMSE and MAPE, while also producing a high R² score.

Based on these results, I selected Random Forest as the MVP benchmark model.

## Issues and Learning

I found that a random train/test split would not be suitable because this is a forecasting task. I therefore used a time-based split so that the model is trained on earlier data and tested on a later period.

I also tested lagged external variables because using current-month economic indicators may not be realistic when generating a forecast.

## Next Steps

* Finalise the MVP model comparison.
* Prepare predicted-versus-actual visualisations.
* Complete feature-importance analysis.
* Document the main business insights for the MVP submission.
