# Stock Drawdown Risk Prediction

A machine learning project focused on predicting short-term stock drawdown risk using historical price data and technical features.

## Project Overview

This project aims to identify whether a stock is likely to experience a significant future decline within the next 20 trading days. Instead of using the broad term "crash", the project uses a more precise risk definition based on **maximum drawdown**.

### Target Definition

A stock is labeled as high-risk (`1`) if its future 20-day maximum drawdown exceeds **10%**:

Crash=1\ if\ Future\ MDD_{20}<-10%

Otherwise, it is labeled as normal (`0`).

## Dataset

This project uses daily adjusted closing prices from 10 major U.S. large-cap stocks:

* AAPL
* AMZN
* GOOGL
* JNJ
* JPM
* META
* MSFT
* NVDA
* PG
* XOM

## Features Engineered

Current features include:

### Momentum

* 5-day return
* 20-day return
* 60-day return

### Volatility

* 10-day volatility
* 20-day volatility

### Trend / Moving Average

* 5-day moving average gap
* 20-day moving average gap

### Risk Signals

* 20-day drawdown
* RSI(14)
* Z-score(20)

## Model Roadmap

Planned models:

* LightGBM
* Random Forest
* Logistic Regression

Evaluation metrics:

* ROC-AUC
* Precision / Recall
* F1 Score

## Current Progress

* ✅ Day1 Literature Review
* ✅ Day2 Data Preparation
* ✅ Day3 Label Construction (Future Drawdown)
* ✅ Day4 Feature Engineering
* 🔄 Day5 Model Training

## Repository Structure

```text
notebooks/   Jupyter notebooks
src/         Python scripts
data/        datasets
outputs/     charts and results
docs/        notes / reports
```

## Objective

Build an interpretable and practical stock downside-risk prediction pipeline that can be extended to larger equity universes in the future.

## Author

Jemary072
