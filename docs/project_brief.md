# Project Brief

## Project Title

**Forecasting International Trade Activity Using Oil Prices and Macroeconomic Indicators: A Machine Learning Analysis of G20 Economies**

## Project Aim

The aim of this project is to investigate whether oil-price movements can be used to predict international trade activity across G20 economies.

The project will develop machine-learning models capable of forecasting monthly import and export values using historical trade data, oil prices and selected macroeconomic indicators. The intended outcome is a predictive framework that provides insights into how energy-market fluctuations influence international trade performance and supports more informed business and economic decision-making.

This project is linked to my professional interest in trade finance, product development and digital transformation. The findings may provide relevant insights for trade-finance planning, liquidity management and risk assessment.

## Problem Statement

Global trade is influenced by fluctuations in oil prices because oil affects transportation costs, production expenses, supply-chain operations and wider economic activity. Changes in oil prices can influence the movement of goods across international markets and affect both import and export values.

However, the relationship between oil prices and trade activity is complex, dynamic and varies across countries. This project therefore examines whether machine-learning models can identify useful predictive relationships between historical trade activity, commodity-price movements and macroeconomic indicators.

## Proposed Solution

The proposed solution is a machine-learning forecasting framework that predicts monthly import and export values for selected G20 economies.

The framework will combine:

* Monthly trade data
* Oil-price indicators
* Commodity-price indicators
* Macroeconomic variables
* Time-based and trade-history features

Multiple machine-learning models will be developed and compared to identify the approach that produces the most accurate trade forecasts. The final system will generate forecasts, identify key predictive drivers and provide country-flow-level insights.

## Minimum Viable Product

The MVP will include:

* An integrated dataset containing monthly G20 trade data, oil prices and macroeconomic indicators.
* Automated data-preprocessing and feature-engineering workflows.
* Forecasting models capable of predicting monthly imports and exports.
* Performance evaluation using R², MAE, RMSE and MAPE.
* Interactive visualisations showing historical and predicted trade activity.
* Preliminary business insights into the relationship between oil prices, commodity indicators and trade activity.

## Technical Approach

The project follows a structured machine-learning lifecycle:

1. Data acquisition from public sources.
2. Data cleaning and integration.
3. Exploratory data analysis.
4. Feature engineering.
5. Model development.
6. Model evaluation.
7. Visualisation and interpretation of results.
8. Prototype deployment planning.

### Technologies

* Python
* Jupyter Notebooks
* Pandas and NumPy
* Scikit-learn
* Matplotlib
* Machine-learning regression models
* GitHub for version control and tracking of project progression

### Initial Model Scope

The project initially proposed comparison of:

* Multiple Linear Regression
* Random Forest Regression
* XGBoost
* Long Short-Term Memory models, subject to feasibility
* Other advanced time-series approaches, subject to feasibility

The final model selection will be based on out-of-sample forecasting performance and practical suitability.

## Data Sources

Potential and used data sources include:

* UN Comtrade Database: monthly import and export trade values for G20 economies.
* World Bank commodity-price data: oil, energy, metals, agriculture and related commodity indices.
* FRED and other public macroeconomic sources: selected macroeconomic variables where relevant.
* Publicly available freight or shipping indicators, subject to availability and suitability.

## Evaluation Criteria

Model performance will be assessed using:

* **R²:** proportion of variance explained by the model.
* **MAE:** average absolute forecast error.
* **RMSE:** forecast error measure that penalises larger errors more heavily.
* **MAPE:** average percentage forecast error, used as the primary comparison metric across country-flow combinations of different sizes.

The project will assess success based on:

* Forecasting accuracy.
* Improvement over baseline models.
* Robustness across countries and import/export flows.
* Identification of meaningful predictive drivers.
* Delivery of a working forecasting framework suitable for future development.
