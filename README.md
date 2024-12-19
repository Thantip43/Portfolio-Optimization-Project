# Predicting Stock Prices and Optimizing Equity Investment Portfolio for Allianz Ayudhya

## Overview

This project aims to predict the stock prices of the top 20 stocks (ranked by market capitalization) from the SET and S&P 500 indices and optimize the equity investment portfolio for Allianz Ayudhya, an insurance company in Thailand. The goal is to use machine learning models and the PyPortfolioOpt library to develop an investment strategy that enhances returns while maintaining a low-risk profile.

## Problem Statement

Allianz Ayudhya's current investment portfolio is designed to be low-risk, comprising 60% government bonds and only 5% equities. Despite this conservative approach, the company faces persistent losses, mainly attributed to underperformance in its equity investments. This project addresses the following challenges:

- **Equity Losses**: Equity investments contribute disproportionately to overall portfolio losses.
- **Optimization Opportunity**: Identifying a data-driven strategy to rebalance the portfolio for improved profitability.

## Objectives

1. Predict stock prices for the top 20 stocks from SET and S&P 500 indices using multiple machine learning models.
2. Compare model performance to identify the most accurate approach based on RMSE (Root Mean Square Error).
3. Optimize the equity investment portfolio using PyPortfolioOpt to achieve higher returns.
4. Demonstrate the application of the optimized portfolio strategy to Allianz Ayudhya’s equity allocation and evaluate its impact on overall returns.

## Approach

### Stock Price Prediction

We used three machine learning models to predict stock prices:

1. **Linear Regression**
2. **LSTM (Long Short-Term Memory)**
3. **XGBoost**

Each model was trained on two configurations:

- **Univariate Model**: Using a single feature (e.g., past stock prices).
- **Multivariate Model**: Using multiple features (e.g., technical indicators, macroeconomic variables).

This resulted in six models:

- Univariate Linear Regression  
- Multivariate Linear Regression  
- Univariate LSTM  
- Multivariate LSTM  
- Univariate XGBoost  
- Multivariate XGBoost  

### Portfolio Optimization

The optimized portfolio was created using the PyPortfolioOpt library. The optimization process involved:

1. Calculating expected returns and risk for each stock.
2. Allocating weights to maximize returns while minimizing risk.
3. Adjusting the optimized portfolio to fit Allianz Ayudhya’s risk profile and constraints.

## Key Findings

### Prediction Results

The model performances were evaluated using RMSE. The multivariate Linear Regression model had the lowest RMSE, making it the best-performing model. The results highlight the importance of using multiple features for accurate predictions.

### Portfolio Optimization Results

Applying the optimized portfolio strategy led to significant improvements:

- **Return Improvement**: The adjusted portfolio achieved a return 4x higher than the actual portfolio’s return, calculated from the start of the last year’s last week until last week.
- **Risk Management**: The optimized portfolio maintained a low-risk profile, aligning with Allianz Ayudhya’s conservative investment strategy.

## Methodology

### Data Collection

- **Stock Data**: Historical price data for the top 20 stocks by market capitalization from the SET and S&P 500 indices.
- **Features**: Technical indicators (e.g., RSI, MACD), macroeconomic variables, and historical prices.

### Data Preprocessing

1. **Cleaning**: Removed missing and inconsistent data.
2. **Feature Engineering**: Generated additional features for multivariate models.
3. **Normalization**: Standardized data to ensure model efficiency.

### Model Training and Evaluation

1. Split data into training and testing sets.
2. Implemented each model with hyperparameter tuning.
3. Evaluated performance using RMSE.

### Portfolio Adjustment

1. Used PyPortfolioOpt to determine optimal weights.
2. Adjusted the equity allocation for Allianz Ayudhya’s portfolio.

## Tools and Technologies

- **Python**: Pandas, NumPy, Scikit-learn, TensorFlow, PyPortfolioOpt
- **Data Visualization**: Matplotlib, Seaborn

## Conclusion

This project demonstrates the power of machine learning and portfolio optimization in addressing Allianz Ayudhya’s equity investment challenges. By leveraging accurate stock price predictions and an optimized portfolio strategy:

- Losses due to equities were mitigated.
- Overall returns increased by 4x compared to the actual portfolio performance.

## Future Work

1. **Broader Stock Universe**: Expand predictions to include more stocks.
2. **Real-Time Implementation**: Develop a system for real-time portfolio adjustments.
3. **Risk Analysis**: Incorporate stress testing and scenario analysis.
