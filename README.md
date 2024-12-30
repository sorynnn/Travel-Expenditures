# Travel Expenditures Analysis

## Project Overview

This project analyzes customer-level data on travel expenditures, focusing on understanding the factors that influence household tourism spending and participation. The dataset includes variables such as income, education, health, and weather conditions at the travel destination. The goal is to build regression models to predict expenditures and participation in tourism.

## Data Description

The dataset, `tour_data.RData`, contains the following variables:

- **income**: Household income.
- **education**: Education level of the household head.
- **health**: Health status index of household members.
- **tripweather**: Weather quality at the destination.
- **participation**: Dummy variable for tourism participation (1 if the household participated in tourism, 0 otherwise).
- **expenditure**: Total household tourism expenditure.

## Methodology

In this analysis, the following models were used to estimate tourism expenditures and participation:

1. **Regression Model**: Used OLS regression to model tourism expenditures (`expenditure`) as a function of **income**, **education**, and **weather** conditions at the destination.
   
2. **Probit Model**: Estimated the probability of tourism participation using **income**, **education**, and **health** as explanatory variables. The probit model is suitable for binary outcome variables.

3. **Sample Selection Model**: Addressed potential sample selection bias in the expenditure data. This model corrected for the possibility that only certain households (those that participated in tourism) are observed in the expenditure dataset.

4. **Inverse Mills Ratio**: Used the inverse Mills ratio from the probit model to correct for sample selection bias in the expenditure regression model.

All results are presented in a regression table for easy interpretation.

## Tools and Libraries Used

- **Programming Language**: R
- **Key Libraries**: `lm`, `AER`, `sampleSelection`, `ggplot2`, `dplyr`

## How to Run

1. Clone this repository to your local machine.
2. Load the `tour_data.RData` dataset into R.
3. Open the R script or R Markdown file to run the analysis.

## License

This project is open-source under the [MIT License](LICENSE).
