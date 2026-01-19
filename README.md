# Superstore Sales Forecasting (Time Series)

## Overview
This project focuses on forecasting **monthly sales** using historical Superstore transaction data. 
Multiple time-series and machine learning models are built and compared to identify the most effective approach for business-oriented demand forecasting.

## Problem Statement
Accurate sales forecasting is critical for inventory planning, revenue estimation, and strategic decision-making. 
The objective of this analysis is to forecast monthly sales and compare classical time-series models, feature-based machine learning, and trend–seasonality based approaches.

## Dataset
- Superstore sales transaction data
- Aggregated from order-level records to **48 monthly observations**
- Time period: **January 2015 – December 2018**

> Note: The dataset may not be included in this repository due to licensing constraints.

## Methodology
1. **Data Preparation**
   - Cleaned and standardized date formats
   - Removed non-informative identifiers
   - Aggregated sales to monthly level to reduce noise and smooth extreme daily fluctuations

2. **Models Implemented**
   - Naïve Baseline (last observed value)
   - ARIMA (classical time series)
   - Random Forest with lag and rolling features
   - Prophet (trend + seasonality model)

3. **Evaluation Metrics**
   - RMSE (Root Mean Squared Error)
   - MAPE (Mean Absolute Percentage Error)

## Results

| Model | RMSE | MAPE |
|------|------|------|
| Baseline | 51,820 | 65.74% |
| ARIMA (1,0,1) | 34,073 | 32.30% |
| Random Forest | 24,779 | 18.89% |
| **Prophet** | **14,020** | **14.98%** |

## Key Insights
- Monthly sales exhibit strong trend and seasonality
- Feature-based ML significantly outperformed the naïve baseline
- Prophet achieved the best performance by explicitly modeling seasonal patterns

## Conclusion
Prophet was selected as the most suitable model for monthly sales forecasting due to its superior accuracy and interpretability, making it well-suited for business demand planning.

## Tools & Libraries
Python, Pandas, NumPy, scikit-learn, statsmodels, Prophet, Matplotlib
