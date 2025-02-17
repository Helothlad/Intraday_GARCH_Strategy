This project implements an intraday trading strategy that combines daily volatility predictions using a GARCH (Generalized Autoregressive Conditional Heteroskedasticity) model with intraday technical indicators to generate trading signals. The strategy aims to capitalize on short-term price movements by leveraging volatility forecasts and intraday price patterns.

How It Works:
Data Preparation:

The project uses two datasets: daily and 5-minute intraday simulated price data.

Daily data is used to calculate log returns and rolling variance.

Intraday data is used to calculate technical indicators like RSI (Relative Strength Index) and Bollinger Bands.

Volatility Prediction:

A GARCH(1,3) model is applied to the daily log returns to predict future volatility.

The predicted volatility is compared to the historical rolling variance to calculate a "prediction premium."

Daily Signal Generation:

A daily trading signal is generated based on the prediction premium. If the premium exceeds a rolling standard deviation threshold, a signal is triggered (long or short).

Intraday Signal Generation:

Intraday signals are generated using RSI and Bollinger Bands. Overbought/oversold conditions are identified to complement the daily signal.

Strategy Execution:

The strategy combines daily and intraday signals to determine entry points.

Positions are held until the end of the trading day, and returns are calculated based on the strategy's performance.

Performance Visualization:

The cumulative returns of the strategy are plotted to evaluate its performance over time.

Key Features:
GARCH Model: Used for volatility forecasting.

Technical Indicators: RSI and Bollinger Bands for intraday signal generation.

Daily and Intraday Integration: Combines daily volatility predictions with intraday price action.

Simulated Data: Demonstrates the strategy's potential using simulated price data.

Dependencies:
matplotlib: For plotting results.

arch: For GARCH modeling.

pandas_ta: For technical indicator calculations.

pandas and numpy: For data manipulation and calculations.

Usage:
Ensure the required libraries are installed.

Place the simulated daily and intraday data files in the specified folder.

Run the script to generate trading signals, execute the strategy, and visualize the cumulative returns.

This project is a demonstration of how volatility modeling and technical analysis can be combined to create a systematic intraday trading strategy. It is intended for educational purposes and can be extended or adapted for real-world applications.

