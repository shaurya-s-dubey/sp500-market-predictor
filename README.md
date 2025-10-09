# S&P 500 Market Direction Predictor

A machine learning model for predicting daily S&P 500 index movements using Random Forest classification with engineered technical indicators and rolling statistics.

## Overview

This project implements a Random Forest classifier to predict whether the S&P 500 index will close higher or lower the following trading day. The model uses historical price data and engineered features including moving average ratios and trend indicators across multiple time horizons.

## Features

- **Historical Data Analysis**: Utilizes S&P 500 data from 1990-present via Yahoo Finance API
- **Feature Engineering**: Implements rolling statistics and technical indicators across 5 time horizons (2, 5, 60, 250, 1000 days)
- **Walk-Forward Backtesting**: Employs expanding window validation to simulate real trading conditions
- **Conservative Prediction Threshold**: Uses 60% probability threshold to reduce false positives

## Model Performance

- **Precision**: 57.47% (vs. 54.66% baseline)
- **Strategy**: Conservative approach with high-confidence signals only
- **Validation**: Out-of-sample backtesting from 2500+ trading days

## Technical Stack

- Python 3.x
- pandas & NumPy for data manipulation
- scikit-learn for machine learning
- yfinance for market data
- matplotlib for visualization

### Prerequisites

Install the required Python libraries:
```bash
pip install -r requirements.txt
```
## References & Acknowledgments

This project is based on the S&P 500 prediction tutorial by [Vik Paruchuri](https://github.com/VikParuchuri). The original implementation and methodology provided the foundation for this machine learning model.

### Original Tutorial
- **Author**: Vik Paruchuri
- **GitHub**: [https://github.com/VikParuchuri](https://github.com/VikParuchuri)
- **Tutorial**: S&P 500 Stock Market Prediction with Machine Learning

### Modifications
This implementation includes:
- Updated data through 2025
- Enhanced documentation and code comments
- Additional performance metrics and analysis
