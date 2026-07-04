# Forecasting International Trade Activity Using Machine Learning

## Project Overview

This project investigates whether commodity prices, oil-price indicators and macroeconomic variables can be used to forecast monthly international trade activity across selected G20 economies.

The analysis predicts monthly import and export trade values using historical trade data from UN Comtrade combined with external economic indicators. The project is being developed as part of the Higher Diploma in Science in Computing programme, with a focus on Artificial Intelligence and Machine Learning.

## Project Aim

The aim is to develop and evaluate machine-learning models that forecast monthly import and export trade values for selected G20 economies.

A key part of the analysis is assessing whether external commodity and macroeconomic indicators, combined with historical trade seasonality, improve forecasting accuracy.

## Current Status

The project is currently in the post-MVP model refinement stage.

Completed work includes:

- Collection of monthly import and export trade data for 18 selected G20 economies.
- Integration of commodity-price and macroeconomic variables.
- Data cleaning, transformation and feature engineering.
- Time-based model training using 2014–2023 data.
- Out-of-sample testing using 2024 monthly trade observations.
- Initial comparison of Linear Regression, Random Forest and Support Vector Regression models.
- Development and validation of a true 12-month seasonal trade-lag feature.
- Controlled comparison of external-only and seasonal Random Forest models.
- Country-level performance analysis and visualisations.

## Current Best Validated Model

The current strongest validated model is a Random Forest model that includes a true 12-month seasonal lag feature.

The seasonal lag represents trade activity in the same month of the previous year. It was constructed using date matching rather than a simple row shift, ensuring that missing monthly observations do not create incorrectly aligned lags.

| Model | MAE (USD bn) | RMSE (USD bn) | R² | MAPE |
|---|---:|---:|---:|---:|
| Matched external-only Random Forest | 4.95 | 8.79 | 0.984 | 8.21% |
| Random Forest with true 12-month seasonal lag | **3.94** | **6.95** | **0.990** | **6.66%** |

Both models used the same training records, 2024 test period and Random Forest settings. The only difference was the inclusion of the 12-month seasonal lag.

## Key Findings

Adding the true 12-month seasonal lag improved overall forecasting accuracy:

- MAE reduced by approximately USD 1.01 billion.
- MAPE reduced from 8.21% to 6.66%.
- R² increased from 0.984 to 0.990.
- Country-level MAPE improved in 14 of the 18 economies examined.

The largest improvements were observed in:

- Mexico
- Saudi Arabia
- Canada
- Indonesia
- Italy

The seasonal feature reduced accuracy for Argentina, Germany, the United Kingdom and the Republic of Korea. This indicates that annual trade persistence is valuable for many economies, but not uniformly useful across all countries.

## Data Sources

The project uses publicly available data sources, including:

- UN Comtrade monthly trade data.
- World Bank commodity-price indicators.
- FRED macroeconomic indicators.
- Other relevant public economic datasets where suitable.

## Models Tested

The following models have been tested during the project:

- Linear Regression
- Random Forest Regression
- Support Vector Regression

Further final-stage evaluation will consider advanced approaches such as Histogram-Based Gradient Boosting and XGBoost.

## Evaluation Metrics

Models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Mean Absolute Percentage Error (MAPE)

MAPE is particularly useful because trade values differ substantially across countries and between import and export flows.

## Repository Structure

```text
docs/               Project brief, requirements, progress documentation and data dictionary
notebooks/          Jupyter notebooks for data preparation, modelling and evaluation
results/            Visualisations, model outputs and summary tables
data/sample/        Sample datasets used for demonstration
weekly_updates/     Weekly evidence of project development
