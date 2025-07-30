📈 SmartStockSignals
A machine learning-driven trading strategy that predicts stock market signals using technical indicators like SMA, RSI, MACD, and more. The project includes real-time data fetching from Yahoo Finance (yfinance), signal generation, feature scaling, and backtesting against a buy-and-hold benchmark.

🚀 Features

✅ Fetches historical stock data using yfinance

✅ Computes technical indicators: SMA, RSI, MACD

✅ Builds predictive signals using machine learning (placeholder for model)

✅ Scales features using StandardScaler

✅ Backtests strategy returns vs buy-and-hold

✅ Visualizes cumulative returns over time

🧠 Technical Indicators Used

SMA (Simple Moving Averages): 10-day, 50-day

RSI (Relative Strength Index)

MACD and MACD Signal Line

Return: Daily log returns

Future_Close: Next day's closing price (for supervised ML training)


📊 Model & Signal Logic

This version uses a placeholder logic for signals (e.g., SMA crossover or ML-based classification). You can train a model like:

Logistic Regression

Random Forest

XGBoost

LSTM (for sequential modeling)

Example:

Signal generation logic (can be replaced with ML model)

df['Signal'] = 0

df.loc[df['SMA_10'] > df['SMA_50'], 'Signal'] = 1

df.loc[df['SMA_10'] < df['SMA_50'], 'Signal'] = -1

📈 Backtest Visualization
The strategy is backtested by comparing predicted signals vs market returns.

python

strategy_returns = returns[1:] * y_pred_final[:-1]

cumulative_strategy = (1 + strategy_returns).cumprod()

cumulative_market = (1 + returns[1:]).cumprod()


