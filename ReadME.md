# Retail Demand Forecasting with XGBoost

This project predicts daily product demand using historical retail sales data.

## Objective
Build a demand forecasting model that can estimate future product quantities based on historical sales patterns, lag features, and product-level demand statistics.

## Dataset
The project uses the Online Retail II dataset, which contains transaction-level retail sales information.

## Methodology
- Filtered positive quantity sales
- Selected top-selling products
- Built daily stock-level demand data
- Added lag and rolling features
- Split data by date into train and test sets
- Trained an XGBoost regressor
- Evaluated using MAE and RMSE

## Key Features
- lag_1
- lag_7
- rolling_mean
- day_of_week
- month
- Product_avg_demand

## Model Performance
The current model was compared against a naive baseline using previous-day demand.

- Model MAE: 30.96
- Baseline MAE: 48.84
- Model RMSE: 131.58
- Baseline RMSE: 178.48

This shows the model outperforms the baseline and learns meaningful demand patterns.

## Files
- model.ipynb: notebook with preprocessing, feature engineering, and model training
- online_retail_II.csv: source dataset
- app.py: FastAPI prediction API


# RIDF

Retail Inventory Demand Forecasting

## Project Overview
RIDF is a retail demand forecasting project that predicts daily item demand using historical sales data and machine learning.

## FastAPI Backend
- GitHub Repository: https://github.com/jayeshkoli-1402/RIDF-API
- Live Deployment: https://ridf-api.onrender.com/

## Model
The forecasting model is trained in the notebook `model.ipynb` using XGBoost and sales-based lag features such as:
- lag_1
- lag_7
- rolling_mean
- day_of_week
- month

## Usage
The deployed API accepts a JSON payload and returns a demand prediction.

## Setup
```bash
python -m venv .venv
source .venv/bin/activate   # Linux/macOS
.venv\Scripts\activate      # Windows
pip install -r requirements.txt