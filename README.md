# Hybrid Energy Demand Forecasting (XGBoost + LSTM)

> A time series machine learning project combining the power of tree-based models and deep learning to accurately forecast electricity demand.

---

## 📌 Overview

It is a hybrid energy forecasting project that leverages both **XGBoost** and **LSTM** models to predict electricity demand using historical consumption data and time-based engineered features.

The idea is to ensemble both approaches to improve robustness, accuracy, and temporal learning — ideal for smart grid applications and energy demand management.

---

## 🚀 Models Used

| Model       | Description |
|-------------|-------------|
| **XGBoost** | Uses lag features, rolling statistics, calendar-based features for tabular modeling. |
| **LSTM**    | Captures long-term temporal dependencies and sequential patterns in consumption. |
| **Ensemble**| Combines XGBoost + LSTM predictions to reduce variance and improve accuracy. (WIP)|

---

## 📈 Dataset

- Source: [Kaggle - PJM Hourly Energy Consumption](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption)  
- Coverage: Hourly energy usage by regional zones
- Period: 2002 - 2018
- Size: ~2.5M records
- Features: `PJME`, time features (`hour`, `month`, `dayofweek`, etc.), lags, rolling averages



---

## 🧠 Features Engineered

- Lag Features: `lag_1`, `lag_24`, `lag_168`
- Rolling Statistics: `rolling_mean_3`, `rolling_mean_7`, `rolling_std_7`, etc.
- Time Features: `hour`, `dayofweek`, `month`, `quarter`, `dayofyear`
- Holiday / Weekend Flags

---

## 🧪 Evaluation Metrics

- **RMSE** (Root Mean Squared Error)
- **MAE** (Mean Absolute Error)
- **Ensemble RMSE Improvement**: TBD

---

## 📊 Results

| Model       | RMSE      | MAE     |
|-------------|-----------|---------|
| XGBoost     | ~560    |  ~316  |
| LSTM        | ~530  | ~267 |
| **Ensemble**| TBD |

---


