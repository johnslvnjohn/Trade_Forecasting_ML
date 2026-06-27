# Week 4 Update: Data Cleaning, Integration and Initial Exploration

## What I Worked On

This week, I focused on preparing the trade dataset for modelling. I combined the monthly trade data downloaded for the selected G20 economies and began integrating it with oil, commodity-price and macroeconomic variables.

## Data Preparation Completed

* Combined country-level monthly import and export trade files.
* Filtered the data to the project modelling period from January 2014 to December 2024.
* Converted the reporting period into a monthly date format.
* Created time-related variables including year, month and quarter.
* Standardised country names and trade-flow information.
* Checked the combined dataset for missing values and inconsistent records.
* Merged the trade data with external commodity and macroeconomic variables.

## Initial Data Exploration

I reviewed the overall data coverage and examined how trade values varied across countries and between imports and exports.

I also started exploring the relationship between trade values and external variables such as oil prices, metals indices, food indices and broader commodity indices.

## Key Outcome

The main outcome from this week was the creation of a combined dataset that could be used for feature engineering and machine-learning modelling.

The filtered modelling dataset contained:

* 18 selected G20 economies.
* Monthly import and export trade flows.
* Data covering January 2014 to December 2024.
* 4,668 country-flow monthly observations after filtering.

## Issues Identified

The data was not equally complete for every country and period. I therefore reviewed coverage carefully and retained only records that were suitable for the selected modelling period.

## Next Steps

* Create model features.
* Prepare a time-based train/test split.
* Build the first baseline machine-learning models.
