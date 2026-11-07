# FMCG Sales Analysis & Demand Forecasting

**A Python-based Business Analytics Project**

## 1. Project Overview

This project analyzes Fast-Moving Consumer Goods (FMCG) sales data from January 2022 to December 2024 to understand sales patterns, examine relationships between operational and promotional variables, and explore historical demand through time-series forecasting.

The project combines exploratory data analysis, correlation analysis, Ordinary Least Squares (OLS) regression, and exponential smoothing techniques to derive insights that can support business decision-making around sales monitoring, inventory planning, and demand forecasting.

## 2. Project Rationale

FMCG businesses operate in an environment where sales volumes vary across products, brands, regions, and sales channels. Variables such as pricing, promotional activity, stock availability, and replenishment can be relevant when examining these changes.

This project was undertaken to apply business analytics techniques to a practical business context and investigate how historical sales data can be translated into meaningful insights for business planning and decision-making.

## 3. Problem Statement

Understanding sales variation and demand patterns is important for FMCG businesses. This project investigates how operational and promotional variables are associated with units sold and how historical sales patterns can be used to evaluate different forecasting approaches.

## 4. Project Objectives

- Examine and prepare FMCG sales data for analysis.
- Understand sales distributions and regional record patterns.
- Identify relationships between sales and operational variables.
- Apply OLS regression to examine factors associated with units sold.
- Analyze historical daily sales trends using moving averages.
- Compare forecasting methods using MAE and RMSE.
- Generate a 90-day aggregate sales forecast.

## 5. Dataset Overview

| Attribute | Details |
|---|---|
| Original Records | 190,757 |
| Cleaned Records | 190,754 |
| Columns | 14 |
| Time Period | January 2022 – December 2024 |
| Regions | PL-North, PL-South, PL-Central |
| Target Variable | Units Sold |

**Key variables:** Unit Price, Promotion Flag, Delivery Days, Stock Available, Delivered Quantity, and Units Sold.

## 6. Tools & Technologies

- **Python:** Primary programming language
- **Pandas & NumPy:** Data manipulation and preparation
- **Matplotlib & Seaborn:** Data visualization
- **Statsmodels:** OLS regression and time-series modelling
- **Scikit-learn:** Forecast evaluation metrics

## 7. Methodology

The project follows five main analytical stages:

1. **Data Cleaning:** Handling missing essential values, date conversion, and removal of records with negative units sold.
2. **Exploratory Data Analysis:** Examining regional record distribution and the distribution of units sold.
3. **Correlation Analysis:** Measuring relationships between sales, promotional activity, inventory, pricing, and delivery variables.
4. **OLS Regression:** Examining the relationship between five selected predictors and units sold.
5. **Time-Series Forecasting:** Analyzing aggregate daily sales using a 30-day moving average, SES, DES, and a last-value baseline, followed by a 90-day forecast.

## 8. Key Findings

- **Sales Distribution:** Units sold followed a right-skewed distribution, with a mean of 19.92 and a median of 18 units.
- **Regional Distribution:** Records were almost equally distributed across the three regions, each contributing approximately 33% of observations.
- **Correlation Analysis:** Stock availability (0.58), promotion flag (0.50), and delivered quantity (0.39) showed positive associations with units sold.
- **Regression Analysis:** The OLS model achieved an R-squared of 0.592. Promotion flag, stock availability, and delivered quantity were statistically significant predictors at the 5% level.
- **Forecast Evaluation:** The last-value baseline outperformed DES and SES on the held-out test period, achieving an MAE of 144.97 and RMSE of 188.58.
- **Final Forecast:** The selected baseline generated a constant forecast of 3,509 aggregate units sold per day over the next 90 days.

## 9. Repository Structure

- `FMCG_Sales_Analysis.ipynb` — Python notebook containing the complete analytical workflow and outputs.
- `FMCG_Sales_Analysis_Report.pdf` — Detailed project report covering methodology, analysis, findings, recommendations, and limitations.
- `FMCG_2022_2024.csv` — Original dataset used for the analysis.
- `README.md` — Project overview and documentation.

## 10. Limitations

- The analysis is observational and does not establish causal relationships.
- Regression results depend on model assumptions and the selected predictors.
- Time-series forecasting is based on aggregate daily sales rather than individual SKU-level demand.
- Forecast evaluation uses a single held-out 90-observation period.
- The selected forecasting approach may perform differently under changing demand conditions.

---

**Project by:** Gaurang Gupta

**Area:** Business Analytics | Predictive Analytics | Sales & Demand Forecasting
