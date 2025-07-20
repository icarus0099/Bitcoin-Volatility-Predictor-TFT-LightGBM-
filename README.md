# Bitcoin-Volatility-Predictor-TFT-LightGBM-


A hybrid forecasting notebook combining a deep‐learning Temporal Fusion Transformer (TFT) and a LightGBM regressor to predict Bitcoin's 5‑day realized volatility using daily features.

## Dataset

* **Source:** imranbukhari/comprehensive-btcusd-1h-data on Kaggle
* **File:** `BTCUSD_1h_Binance.csv`
* **Features:** Hourly OHLCV resampled to daily; computed realized volatility (5-day RV), volume, rolling RV MA, RSI, ATR.

## Results

| Model    | RMSE   | R²    |
| -------- | ------ | ----- |
| ARIMA    | 0.0795 | 0.061 |
| LightGBM | 0.0658 | 0.358 |
| TFT      | 0.0688 | 0.298 |
| Ensemble | 0.0604 | 0.458 |

*Ensemble = 0.56·LightGBM + 0.44·TFT*
