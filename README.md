# Forecasting International Trade Activity using Oil Prices and Macroeconomic Indicators

## A Machine Learning Analysis of G20 Economies

This project develops and evaluates a machine-learning pipeline for forecasting monthly import and export values across 18 G20 economies.

The main research question is whether oil prices, commodity indices and selected macroeconomic indicators improve forecasting accuracy beyond the information contained in historical seasonal trade patterns.

## Project Status

**Status: Completed – Final submission**

The final data pipeline, model development, evaluation, technical report and video demonstration have been completed.

The project includes:

- monthly import and export data for 18 G20 economies;
- data covering January 2014 to December 2024;
- an exact date-based 12-month historical trade lag;
- one-month-lagged commodity-price and macroeconomic indicators;
- a chronological split using data up to 2023 for training and 2024 for testing;
- comparison of six forecasting approaches;
- country-level error analysis;
- comparison of seasonal history alone against seasonal history with external indicators;
- SHAP model explainability;
- Random Forest tree-percentile uncertainty ranges;
- ablation analysis;
- scenario analysis; and
- reproducibility testing.

## Final Dataset

After cleaning, monthly alignment and creation of the exact 12-month trade lag, the final modelling dataset contained:

- **4,196 observations**
- **3,764 training observations**
- **432 test observations from 2024**
- **35 predictor variables**
- **18 G20 economies**
- separate import and export observations

## Models Evaluated

The following forecasting approaches were compared:

1. Linear Regression
2. Support Vector Regression
3. Random Forest
4. XGBoost
5. Histogram-Based Gradient Boosting
6. Seasonal Long Short-Term Memory

## Final Results

Random Forest produced the strongest overall forecasting performance on the unseen 2024 test dataset.

| Metric | Final Random Forest result |
|---|---:|
| Mean Absolute Percentage Error | 6.763% |
| Mean Absolute Error | USD 3.935 billion |
| Root Mean Squared Error | USD 6.850 billion |
| R-squared | 0.990 |

The exact 12-month historical trade lag was the most influential predictor. Among the external variables, the base-metals index made the clearest positive contribution.

Adding external indicators reduced Mean Absolute Percentage Error from **8.225% to 6.763%**. However, Root Mean Squared Error increased slightly and R-squared decreased slightly, showing that the contribution of the external indicators differed across evaluation measures.

## Main Findings

- Seasonal historical trade behaviour supplied most of the predictive value.
- Tree-based ensemble and boosting models outperformed the linear, kernel-based and recurrent approaches.
- External indicators provided smaller and uneven improvements.
- Model performance differed materially between countries.
- Strong overall accuracy did not mean that every country or month was forecast equally well.
- Random Forest provided the strongest balance of accuracy, interpretability and uncertainty analysis.

## Repository Contents

- [`notebooks/Tradeflow_Final.ipynb`](notebooks/Tradeflow_Final_Version.ipynb) – final structured forecasting notebook
- [`notebooks/archive/Tradeflow_Development_Notebook.ipynb`](notebooks/archive/Tradeflow_Development_Notebook.ipynb) – complete development and experimentation notebook
- [`docs/Trade_Flows_Final_Report.pdf`](docs/Trade_Flows_Final_Report.pdf) – final technical report
- `data/` – raw and processed project datasets
- `results/figures/` – final figures
- `results/tables/` – final result tables
- `weekly_update/` – project progress records

## Video Demonstration

The final project demonstration is available here:

https://youtu.be/ZCa0ufGfsS4

The video demonstrates the working forecasting pipeline, feature engineering, chronological evaluation, model comparison, real predictions, explainability, uncertainty and ablation analysis.

## Running the Final Notebook

Run the notebook from the repository root so that its relative data paths resolve correctly:

```text
notebooks/Tradeflow_Final.ipynb
