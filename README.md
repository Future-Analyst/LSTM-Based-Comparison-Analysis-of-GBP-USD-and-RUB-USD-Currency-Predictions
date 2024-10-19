# LSTM-Based Comparison Analysis of GBP/USD and RUB/USD Currency Predictions

## Project Overview
This project focuses on building and comparing Long Short-Term Memory (LSTM) models to predict the closing prices of two currency pairs: **GBP/USD** and **RUB/USD**. By applying the same LSTM architecture, we evaluate the performance of both models based on various metrics and provide a comparative analysis of their predictions.

## Objective
**Primary Goal**: To compare the predictive performance of LSTM models on two currency pairs and analyze which model performs better in terms of accuracy and error distribution.

**Currency Pairs**:
1. **GBP/USD** – British Pound to US Dollar
2. **RUB/USD** – Russian Ruble to US Dollar

## Data Sources
- **GBP/USD Historical Data**: Historical stock data for GBP/USD, which includes daily closing prices.
- **RUB/USD Historical Data**: Historical stock data for RUB/USD, which includes daily closing prices.

Both datasets contain daily stock data, and they are preprocessed similarly for consistency in model training and comparison.

## Model Architecture
We utilized an LSTM model for both currency pairs. The architecture includes:
- Input layer with a specific number of timesteps (lookback window)
- LSTM layers with 50 units each
- Dense layer for final predictions
- Mean Squared Error (MSE) as the loss function and Adam optimizer

The same model architecture was used for both currency pairs to ensure a fair comparison.

## Data Preprocessing
- **Normalization**: The data was scaled between 0 and 1 using Min-Max normalization to facilitate LSTM training.
- **Windowing**: A lookback window of 60 days was applied to create sequences of historical prices to predict the next day's closing price.
- **Train/Test Split**: The data was split into training and testing sets, with 80% of the data for training and 20% for testing.

## Comparison Metrics
To evaluate and compare the performance of the LSTM models, the following metrics were used:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score

## Performance Analysis

### 1. Performance Metrics

**GBP/USD**:
- MAE: 0.0081
- MSE: 0.0001
- R² Score: 0.9176

**RUB/USD**:
- MAE: 0.0343
- MSE: 0.0018
- R² Score: 0.9176

### 2. Visualization

- **Predicted vs Actual Prices**: We plotted the predicted and actual closing prices for both GBP/USD and RUB/USD. These plots give a clear indication of how well each model tracked the actual trends of the respective currencies.
- **Percentage Error**: We calculated the percentage error for each time step to compare how close the predictions were to the actual values across both currency pairs. The percentage error was visualized on a graph for easy comparison.

### 3. Results Summary
Based on the performance metrics, we can observe that the LSTM model performed better on **[currency pair]**, as indicated by its lower MAE, MSE, and higher R² score. The visual comparison also shows that the predictions for **[currency pair]** tracked more closely with the actual prices, while the predictions for **[the other currency pair]** had a larger deviation. The percentage error comparison further highlights the differences in model performance, with **[currency pair]** generally exhibiting lower prediction errors.

## Insights and Conclusion
The LSTM model was able to capture the trends and make reasonably accurate predictions for both currency pairs. However, the model performed better for **[currency pair]**, as evidenced by its lower error metrics and more accurate predictions. The comparison analysis reveals that while LSTM is a powerful tool for time series prediction, the performance of the model can vary based on the specific characteristics of the data being used (e.g., volatility, trends, external economic factors).

## Future Work
- **Hyperparameter Tuning**: Future work could involve further tuning the model’s hyperparameters, such as the number of LSTM units, batch size, or lookback window, to improve the predictions for both currency pairs.
- **Feature Engineering**: Incorporating additional features, such as volume, open prices, or external economic indicators, may enhance the model’s predictive performance.
- **Alternative Models**: Exploring other deep learning architectures, such as GRUs (Gated Recurrent Units), or hybrid models combining LSTMs with other machine learning techniques could provide more insights into the predictability of currency pairs.
