## Objective:
The project aims to predict the closing stock price of major technology companies, including Apple Inc. (AAPL), Google LLC (GOOG), Microsoft Corporation (MSFT), and Amazon.com Inc. (AMZN), using Long Short-Term Memory (LSTM) neural networks. LSTM is chosen for its efficacy in capturing temporal dependencies in time-series data, making it suitable for financial market predictions where past stock prices can influence future prices.

## Methodology:

1. Data Collection: Historical stock price data for AAPL, GOOG, MSFT, and AMZN are fetched for the past year using the Yahoo Finance API via the yfinance and pandas_datareader libraries. The dataset includes Open, High, Low, Close, Adjusted Close prices, and Volume for each trading day.
2. Data Preparation: The dataset is cleaned and preprocessed. This involves setting the datetime as the index, handling missing values (weekends and public holidays when the stock market is closed), and scaling the data using Min-Max Scaling to normalize the values between 0 and 1, which is a crucial step for neural network training.
3. Model Building: An LSTM model is constructed using the Keras library with TensorFlow backend. The model architecture includes LSTM layers followed by Dense layers, designed to capture both the short-term and long-term dependencies in the stock price movements.
Training: The model is trained on the closing prices of the stocks, using historical data up to 95% of the dataset for training, and the remainder for testing. The data is further divided into sequences (or batches) to train the model to predict the next day's closing price based on the previous 60 days' data.
4. Evaluation: The model's performance is evaluated using the Root Mean Squared Error (RMSE) metric, which measures the model's accuracy by calculating the square root of the average squared differences between the predicted and actual closing prices.

## Outcomes:

The LSTM model successfully predicts the closing stock prices of the selected technology companies. The predictions are visually represented through plots comparing the actual and predicted prices, allowing for an easy assessment of the model's performance.
The RMSE value provides a quantitative measure of the model's prediction accuracy. A lower RMSE indicates a higher accuracy, and for this project, the RMSE achieved suggests that the model has a reasonable level of precision in forecasting stock prices.
The project demonstrates the potential of LSTM neural networks in financial market predictions, particularly for stock price forecasting. It highlights the importance of data preprocessing, model architecture design, and the choice of evaluation metrics in building effective predictive models.


## Metrics:

RMSE (Root Mean Squared Error): A key metric used to quantify the difference between the values predicted by the model and the actual values. For this project, the RMSE value indicates how closely the model's predictions match the real stock prices, with a lower RMSE value representing higher accuracy.


## Conclusion
This project showcases the application of LSTM neural networks in predicting the closing prices of stocks, offering valuable insights into the potential of machine learning in financial analysis. The methodology employed, from data collection to model evaluation, outlines a comprehensive approach to stock price forecasting, providing a foundation for further exploration and refinement in the field of financial market predictions.