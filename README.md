# 🎲 QuantFlip - Stock Prediction Engine

> Probability-driven swing trade assistant for Indian NSE stocks

QuantFlip uses RSI + MACD technical indicators fed into an XGBoost classifier to estimate 3-day upside probability for any NSE stock.

## How It Works

- Fetches 2 years of historical data via yfinance  
- Engineers RSI, MACD, and return features  
- Trains an XGBoost classifier on historical patterns  
- Predicts upside probability for the latest trading day  

## Signals

| Probability | Signal | Meaning |
|-------------|--------|---------|
| ≥ 60% | 🟢 GREEN | Calculated Buy |
| 40–60% | 🟡 YELLOW | Neutral / Hold |
| ≤ 40% | 🔴 RED | High Risk / Avoid |

## Run on Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1VAfEG5VE9a8qBSgjQcigiM68ilB_dCNr#scrollTo=0BogJVJuOsFO)

1. Open the notebook in Colab  
2. Run all cells in order  
3. Enter any NSE symbol (RELIANCE, TCS, INFY...)  
4. See the prediction!

## Tech Stack

- **Data:** yfinance  
- **Indicators:** ta (RSI, MACD)  
- **Model:** XGBoost  
- **API:** FastAPI  
- **Notebook:** Google Colab  

## Disclaimer

Educational tool only. Not financial advice. Never risk more than 2% per trade.
