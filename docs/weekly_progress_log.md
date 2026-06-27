# Weekly Progress Log

This log records the progress of my project from Week 2 onwards. I started uploading my project work to GitHub during Week 5, so earlier activities are being added retrospectively based on the work, notebooks, datasets and outputs completed so far.

| Week   | Main Activity                                     | Work Completed                                                                                                                                                                                                                                                                                                                                                                            | Key Outcome                                                                                                                    |
| ------ | ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Week 2 | Project planning and data-source research         | I finalised the project topic, business problem and overall objective. I decided to investigate whether oil prices and macroeconomic indicators can help predict monthly international trade activity across selected G20 economies. I also identified possible data sources including UN Comtrade, World Bank commodity data and FRED macroeconomic data.                                | Project scope, objective and data-collection approach established.                                                             |
| Week 3 | Data collection and initial preparation           | I began downloading monthly import and export data for the selected G20 economies from UN Comtrade. I also collected commodity-price and macroeconomic data to use as potential external variables. I reviewed the country coverage and identified data gaps and availability issues.                                                                                                     | Initial trade and external-variable datasets collected.                                                                        |
| Week 4 | Data cleaning, integration and exploration        | I combined country-level trade files, cleaned and standardised the data, converted reporting periods into monthly dates and created year, month and quarter variables. I merged the trade data with commodity and macroeconomic indicators. I also checked missing values, coverage and initial relationships between variables.                                                          | Created a combined dataset for modelling, covering 18 selected G20 economies and monthly import/export data from 2014 onwards. |
| Week 5 | Feature engineering and initial model development | I created time-based features, encoded country and trade-flow variables and used a log-transformed trade-value target. I prepared a time-based split using 2014–2023 for training and 2024 for testing. I trained and compared Linear Regression, Random Forest and Support Vector Regression models. I also tested lagged external variables to make the forecast design more realistic. | Random Forest produced the strongest initial results and was selected as the MVP benchmark model.                              |
| Week 6 | MVP completion — planned                          | I will finalise the MVP model comparison, complete model evaluation using MAE, RMSE, R² and MAPE, prepare predicted-versus-actual charts and document the main findings. I will also complete the initial GitHub project evidence and prepare the MVP submission.                                                                                                                         | To be completed next week.                                                                                                     |

## Current Project Status

The project is currently in the final stage before MVP submission.

The dataset has been prepared, baseline models have been developed and initial model comparison has been completed. The next stage is to finalise the MVP model evaluation, supporting visualisations and business insights.

## Dataset Status

* The project includes 18 selected G20 economies.
* Both import and export trade flows are included.
* The modelling period covers January 2014 to December 2024.
* The initial combined dataset contained 5,066 records.
* After filtering, the dataset contained 4,668 monthly country-flow observations.
* The intended training period is January 2014 to December 2023.
* The intended test period is January 2024 to December 2024.
* Trade data has been merged with oil, commodity-price and selected macroeconomic variables.

## Initial Model Results

The initial models tested were Linear Regression, Random Forest Regression and Support Vector Regression.

| Model                     | MAE (USD bn) | RMSE (USD bn) |    R² | MAPE (%) |
| ------------------------- | -----------: | ------------: | ----: | -------: |
| Linear Regression         |        10.25 |         19.56 | 0.922 |    13.73 |
| Random Forest             |         5.02 |          8.94 | 0.984 |     8.28 |
| Support Vector Regression |        13.32 |         18.05 | 0.934 |    33.72 |

## Current Model Direction

At this stage, Random Forest is the strongest initial model and will be used as the MVP benchmark.

It achieved the lowest MAE, RMSE and MAPE among the models tested so far. The next step is to complete the MVP evaluation and decide whether further feature refinement or an advanced model is required after the MVP submission.

## Main Decisions Made So Far

* I used a time-based train/test split rather than a random split because this is a forecasting project.
* I used `log1p(primaryValue)` as the target variable to reduce the impact of very large trade values.
* I encoded country name and trade-flow direction for the machine-learning models.
* I tested lagged external variables so that the model would not depend on information that may not be available at the point of forecasting.
* I used MAE, RMSE, R² and MAPE to evaluate model performance.
* Random Forest is currently the strongest MVP benchmark model.
