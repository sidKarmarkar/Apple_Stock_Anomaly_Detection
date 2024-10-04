## Overview

This project implements anomaly detection on historical stock data for Apple Inc. (AAPL) using machine learning techniques. Specifically, it uses the **Isolation Forest** algorithm to detect anomalies in stock prices, which could signify unusual market conditions or trading activities. The dataset spans from **12th December 1980 to 12th December 2022**, covering over 40 years of stock price movements. 

The primary objective of this project is to identify outliers in the data that may indicate market anomalies. By using machine learning models like Isolation Forest, we can automate the detection of such events.

## Dataset

The dataset used for this project is an Apple stock price dataset, which was sourced from **Kaggle**. It includes daily stock prices (Open, High, Low, Close) and trading volumes for Apple (AAPL) from **12th December 1980 to 12th December 2022**. You can find similar datasets on Kaggle at [Kaggle - Apple Stock Data](https://www.kaggle.com/datasets).

## Files

- `Market_Anomaly_Detection.ipynb`: The main Python script that loads the dataset, applies the Isolation Forest algorithm for anomaly detection, and visualizes the results.
- `README.md`: This file, providing project documentation and instructions.
- `AAPL.csv`: The dataset used for anomaly detection (not included in this repo, download separately from Kaggle or use your own dataset).

## Project Structure

1. **Data Loading**: The stock price dataset is loaded using Pandas, and the date column is formatted as a datetime object to ensure correct handling of time series data.
2. **Preprocessing**: The stock prices (specifically the 'Close' price) are scaled using a standard scaler to ensure uniformity in data values before applying the machine learning model.
3. **Anomaly Detection**: The **Isolation Forest** algorithm is used to detect anomalies in the stock price data. This unsupervised learning technique is ideal for finding outliers in financial time series data.
4. **Visualization**: The detected anomalies are plotted alongside the stock's closing prices. Anomalies are marked on the chart to visually indicate the points in time where abnormal stock movements occurred.

## Running the Code

To run the anomaly detection script, simply execute the following command after downloading the dataset and placing it in the same directory as the script:

```bash
python Market_Anomaly_Detection.ipynb.py
```

Make sure to update the `file_path` in the script to point to your local dataset file.

## How It Works

1. **Isolation Forest**: This algorithm isolates anomalies by constructing decision trees and partitioning data points into random subspaces. Points that are easier to isolate are classified as anomalies.
2. **Data Scaling**: We scale the input data before feeding it into the model, ensuring that the variance between features (e.g., price) doesn't impact the anomaly detection process.
3. **Result Interpretation**: Anomalies detected by the model are likely to correspond to unusual market conditions such as sharp price drops, spikes in volatility, or significant external events affecting stock prices.

## Example Output

When running the code, you will see a plot similar to the one below:

- The blue line represents the historical stock prices of Apple Inc.
- Red markers indicate the detected anomalies or outliers in the dataset.


## Conclusion

This project demonstrates how machine learning can be effectively applied to financial data to detect anomalies. By identifying outliers in stock price movements, we can potentially discover unusual market activities or external factors influencing the stock.

Feel free to fork this repository, contribute improvements, or reach out with any questions!

---

### License

This project is licensed under the MIT License. Feel free to use, modify, and share it for learning purposes.

---

### Acknowledgments

The dataset used in this project was sourced from Kaggle.
