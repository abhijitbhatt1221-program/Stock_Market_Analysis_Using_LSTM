# Stock Price Prediction using LSTM and Geometric Brownian Motion

## Project Overview
This project demonstrates a stock price prediction model using a Long Short-Term Memory (LSTM) neural network, combined with a Geometric Brownian Motion (GBM) for trend-based projections. The model is trained on historical stock data fetched from Yahoo Finance.

## Dataset
The dataset used is the historical stock price data for TCS.NS (Tata Consultancy Services) fetched from Yahoo Finance, starting from 2010-01-01 to the current date.

## Key Features
- **Data Loading**: Fetches historical stock data using the `yfinance` library.
- **Data Preprocessing**: Handles data cleaning, including dropping unnecessary columns and scaling using `MinMaxScaler`.
- **Feature Engineering**: Calculates 100-day and 200-day moving averages.
- **Model Training**: Implements an LSTM model using TensorFlow/Keras for sequence prediction.
- **Model Evaluation**: Assesses the model's performance using Mean Absolute Error (MAE) and R2 Score.
- **Visualization**: Plots actual vs. predicted prices, moving averages, and trend-based projections.
- **Trend-Based Projection (Geometric Brownian Motion)**: Projects future stock prices based on historical drift and volatility.

## Installation
To run this notebook, you'll need the following Python libraries. You can install them using pip:

```bash
pip install pandas numpy matplotlib yfinance tensorflow scikit-learn
```

## Usage
1. Run all cells in the Colab notebook sequentially.
2. The notebook will:
    - Load historical stock data for 'TCS.NS'.
    - Visualize closing prices and moving averages.
    - Split data into training and testing sets.
    - Train an LSTM model.
    - Make predictions and visualize them against actual prices.
    - Perform a Geometric Brownian Motion projection for future prices.
    - Evaluate the model's performance with MAE and R2 score.

## Model Evaluation Metrics
- **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors in a set of forecasts, without considering their direction. A lower MAE indicates a better model.
- **R2 Score**: Represents the proportion of the variance in the dependent variable that is predictable from the independent variables. An R2 score closer to 1 indicates a better fit of the model to the data.

## Results
The model achieves an MAE of approximately 8.76% and an R2 score of 0.93, indicating a reasonably good fit and prediction accuracy for the given stock data.

## Geometric Brownian Motion Projection
This projection provides a probabilistic forecast for future stock prices, incorporating the historical drift and volatility of the stock. It's a useful tool for understanding potential future price movements under random market conditions.

## Future Enhancements
- Experiment with different LSTM architectures or other time series models (e.g., GRU, ARIMA).
- Incorporate more features like volume, open, high, low prices, or technical indicators.
- Optimize hyperparameters using techniques like GridSearchCV or RandomizedSearchCV.
- Implement sentiment analysis from news data to enhance predictions.
"""

