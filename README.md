# Trade_Forecasting_ML
Tracking my Trade forecasting using Machine Learning Project
# Forecasting International Trade Activity Using Machine Learning

## Project Overview

In this project, I am investigating whether oil prices, commodity indicators and macroeconomic variables can be used to forecast monthly international trade activity across selected G20 economies.

The project focuses on predicting monthly import and export values using historical trade data from UN Comtrade combined with external economic indicators.

The project is being developed as part of the Higher Diploma in Science in Computing programme, with a focus on Artificial Intelligence and Machine Learning.

## Project Aim

The aim of the project is to develop and evaluate machine-learning models that can forecast monthly import and export trade values for selected G20 economies.

The project will assess whether oil prices and other external economic indicators can improve trade forecasting accuracy and provide useful business insights.

## Current Status

The project is currently at the MVP development stage.

Work completed so far includes:

* Collection of monthly import and export trade data for 18 selected G20 economies.
* Integration of commodity-price and macroeconomic variables.
* Data cleaning, transformation and feature engineering.
* Time-based model training and testing.
* Initial comparison of Linear Regression, Random Forest and Support Vector Regression models.
* Initial model visualisations and performance analysis.

The MVP submission is planned for Week 6.

## Current Best MVP Model

The current strongest model is Random Forest Regression.

| Metric |           Result |
| ------ | ---------------: |
| MAE    | USD 5.02 billion |
| RMSE   | USD 8.94 billion |
| R²     |            0.984 |
| MAPE   |            8.28% |

These results are based on a time-based test period covering monthly trade observations from 2024.

## Data Sources

The project uses publicly available data sources, including:

* UN Comtrade monthly trade data.
* World Bank commodity-price indicators.
* FRED macroeconomic indicators.
* Other relevant public economic datasets where suitable.

## Models Tested

The following models have been tested during the MVP stage:

* Linear Regression
* Random Forest Regression
* Support Vector Regression

Further model development after the MVP will consider advanced approaches such as Histogram-Based Gradient Boosting and XGBoost.

## Evaluation Metrics

The models are evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score
* Mean Absolute Percentage Error (MAPE)

MAPE is particularly useful in this project because trade values vary substantially between countries and between import and export flows.

## Repository Structure

```text
docs/              Project brief, progress log and data dictionary
notebooks/         Jupyter notebooks used for data preparation and modelling
weekly_update/     Weekly evidence of project development
results/           Visualisations, model outputs and summary tables
data/sample/       Sample datasets used for demonstration
```

## Project Documentation

* [Project Brief](docs/project_brief.md)
* [Weekly Progress Log](docs/weekly_progress_log.md)
* [Data Dictionary](docs/data_dictionary.md)

## Key Limitation

This project uses monthly trade data, which may be published with a delay depending on the reporting country. The model is therefore designed as a monthly forecasting framework rather than a real-time trade forecasting system.

## Author

John Selvin Raja John
Student Number: 25120051
Module / Cohort: HDAIML_SEP25OL
