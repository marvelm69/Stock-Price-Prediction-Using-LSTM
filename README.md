# Stock Price Prediction using LSTM

## Overview

This project is focused on predicting stock prices using a **Long Short-Term Memory (LSTM)** neural network. The theoretical goal of this project is to demonstrate how deep learning techniques can be used for time series forecasting, particularly in the financial domain. The project compares stock prices of two companies, **Apple Inc. (AAPL)** and **Advanced Micro Devices, Inc. (AMD)**, to showcase how the model performs on different datasets.

## Goals

The primary goal of this project is to explore the theoretical underpinnings of **time series analysis** and how they can be applied using **deep learning** models such as LSTM. This includes:

- **Time Series Analysis**: Investigating how sequential data (like stock prices) can be effectively modeled.
- **LSTM for Financial Predictions**: Applying LSTM, a type of recurrent neural network, for predicting stock prices, emphasizing the benefits of LSTM's ability to capture long-term dependencies.
- **Comparative Analysis**: Evaluating the performance of the model on different stock datasets (AAPL and AMD) and analyzing the results.
- **Feature Engineering**: Discussing the impact of various preprocessing techniques such as data normalization and windowing for model performance.

## Data

This project uses publicly available historical stock data from Apple (AAPL) and AMD (AMD), spanning from the 1980s to 2020. The data contains the following columns:
- Date
- Open
- High
- Low
- Close
- Adjusted Close
- Volume

## Methodology

The project follows a systematic process to build and train an LSTM model:

1. **Data Preprocessing**: 
   - **Exploration**: Initial analysis of both AAPL and AMD datasets to understand trends, missing values, and data distribution.
   - **Normalization**: Normalizing the 'Close' price for input into the LSTM model.
   - **Windowing**: Creating sliding windows of data to capture the sequential nature of stock prices.

2. **Model Architecture**:
   - Using an **LSTM** model with 50 units and a **Dense layer** to predict future stock prices based on the previous time steps.
   - The model is compiled using the **Adam optimizer** and trained using **mean squared error (MSE)** as the loss function.

3. **Evaluation**:
   - The model is evaluated on **validation** and **test datasets** for both AAPL and AMD stocks.
   - Performance metrics such as **Root Mean Squared Error (RMSE)**, **Mean Absolute Error (MAE)**, and **Mean Absolute Percentage Error (MAPE)** are calculated to assess model accuracy.

## Results

The performance of the LSTM model on the AAPL and AMD datasets is summarized below:

| Stock Symbol | Dataset   | RMSE   | MAE    | MAPE (%) |
|--------------|-----------|--------|--------|----------|
| AAPL         | Test Set  | 4.2134 | 2.5857 | 1.4054   |
| AMD          | Test Set  | 0.9860 | 0.5956 | 2.9280   |

As seen in the results, the LSTM model performed well on both datasets, with lower RMSE, MAE, and MAPE values for AMD.

## Future Work

This project lays the foundation for more complex financial forecasting models. Future work can include:
- Incorporating additional features like **trading volume**, **technical indicators**, and **macroeconomic data**.
- Implementing more advanced architectures such as **Transformer** models for improved accuracy.
- Expanding the project to predict **multiple time steps ahead** rather than just one-step forecasting.

## Conclusion

This project demonstrates the practical application of LSTM models for stock price prediction. By leveraging the sequential nature of stock data, LSTM models can effectively capture patterns and trends, providing valuable insights for financial forecasting.
