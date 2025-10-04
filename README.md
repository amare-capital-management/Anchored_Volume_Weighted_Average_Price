<img width="780" height="253" alt="ACM w color" src="https://github.com/user-attachments/assets/08833e10-7f24-4c08-9cca-3d60c99e439e" />

### The 6.Anchored_Volume_Weighted_Average_Price script is designed to perform Anchored Volume Weighted Average Price (VWAP) analysis for a list of stock tickers. Here's a detailed breakdown of its functionality:

*1. Imports and Setup:*

Utilizes libraries like pandas, matplotlib, and custom modules for data processing, visualization, and analysis.
Sets up directories for saving outputs such as VWAP charts, trade summaries, and other analysis results.

*2. Data Preparation:*
   
prepare_data:
Fetches OHLC (Open, High, Low, Close) data for a given ticker using Yahoo Finance.
Adds ATR (Average True Range) and identifies local minima and maxima in the data.
Stores prepared data for all tickers in a dictionary (ticker_data).

*3. Anchor Dates:*

get_anchor_dates:
Determines anchor dates for VWAP calculations, including:
The first day of the year.
The most recent local minima and maxima.
Any custom dates provided.
Generates anchor dates for all tickers.

*4. VWAP Analysis:*

analyze_ticker:
Calculates Anchored VWAPs for each anchor date.
Saves daily VWAP charts for each ticker.
Determines the trend (Bullish, Bearish, or Neutral) based on the relationship between the last close price and VWAP levels.
Generates trade signals (Long or Short) based on the trend, VWAP levels, and ATR.
Calculates trade parameters such as entry price, stop loss, take profit, and position size.

*5. Main Execution:*
   
Analyzes all tickers and saves the results:
CSV File: Saves the Anchored VWAP analysis results for all tickers in anchored_vwap.csv.
Trade Summaries: Saves trade summaries for each ticker in text files.
Generates additional plots:
5-Day SMA: Creates 5-day simple moving average charts.
Price and Volume Profile: Visualizes price and volume distribution.
Intraday VWAP: Optionally generates intraday VWAP charts.

*6. Logging and Outputs:*
Logs progress and errors during data preparation, analysis, and visualization.
Saves charts and summaries in their respective directories.

*Purpose:*

This script is a technical analysis tool designed to:

Calculate Anchored VWAPs for multiple stocks.
Identify trends and generate trade signals based on VWAP levels and ATR.
Visualize VWAPs, price/volume profiles, and moving averages for better decision-making.

### It is useful for traders and analysts looking to incorporate VWAP-based strategies into their trading workflows.
