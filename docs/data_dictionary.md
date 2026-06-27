# Data Dictionary

I am using this dictionary to describe the main variables used in the trade forecasting dataset.

## Trade Data Variables

| Variable        | Description                                                                                               |
| --------------- | --------------------------------------------------------------------------------------------------------- |
| `country_name`  | Name of the reporting G20 country.                                                                        |
| `flowCode`      | Direction of trade: `M` represents imports and `X` represents exports.                                    |
| `flowDesc`      | Description of the trade flow, such as Import or Export.                                                  |
| `period`        | Monthly reporting period in `YYYYMM` format.                                                              |
| `date`          | Date version of the reporting period used for time-series analysis.                                       |
| `year`          | Year extracted from the reporting period.                                                                 |
| `month`         | Month number extracted from the reporting period.                                                         |
| `quarter`       | Quarter of the year derived from the month.                                                               |
| `primaryValue`  | Total monthly trade value reported in US dollars. This is the main target variable before transformation. |
| `trade_balance` | Difference between export and import trade value, where applicable.                                       |

## Target Variable

| Variable           | Description                                                                                                                                                          |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `log_primaryValue` | Log-transformed version of `primaryValue`, created using `log1p(primaryValue)`. This is used as the model target to reduce the influence of very large trade values. |

## Commodity and Oil Variables

| Variable                | Description                                                             |
| ----------------------- | ----------------------------------------------------------------------- |
| `crude_oil_avg_usd`     | Average crude oil price in US dollars.                                  |
| `brent_crude_usd`       | Brent crude oil price in US dollars, where available.                   |
| `wti_crude_usd`         | West Texas Intermediate crude oil price in US dollars, where available. |
| `commodity_total_index` | Overall commodity-price index.                                          |
| `energy_index`          | Energy commodity-price index.                                           |
| `non_energy_index`      | Non-energy commodity-price index.                                       |
| `agriculture_index`     | Agriculture commodity-price index.                                      |
| `food_index`            | Food commodity-price index.                                             |
| `fertilizers_index`     | Fertilizer commodity-price index.                                       |
| `metals_minerals_index` | Metals and minerals commodity-price index.                              |
| `base_metals_index`     | Base metals commodity-price index.                                      |
| `precious_metals_index` | Precious metals commodity-price index.                                  |

## Macroeconomic Variables

| Variable                    | Description                                                        |
| --------------------------- | ------------------------------------------------------------------ |
| `usd_broad_index`           | Broad US dollar index, used as an indicator of US dollar strength. |
| `us_industrial_production`  | US industrial production indicator.                                |
| `us_cpi`                    | US Consumer Price Index.                                           |
| `fed_funds_rate`            | US Federal Funds Rate.                                             |
| `us_10y_treasury`           | US 10-year Treasury yield.                                         |
| `global_policy_uncertainty` | Global Policy Uncertainty Index.                                   |

## Model Input Features

The model uses a combination of:

* Country and trade-flow categories.
* Time variables such as year, month and quarter.
* Oil, commodity and macroeconomic indicators.
* Lagged versions of selected external variables.
* Historical trade values and derived trade-history features in later model versions.
