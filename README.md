# Stock Price Prediction using LSTM with Bayesian Optimization

This repository contains a Python script that predicts stock prices using a Long Short-Term Memory (LSTM) neural network. The script utilizes Bayesian Optimization to fine-tune the hyperparameters of the LSTM model for improved accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Hyperparameter Optimization](#hyperparameter-optimization)
- [Results](#results)
- [Model Saving](#model-saving)
- [Contributing](#contributing)

## Introduction

This project demonstrates how to build a stock price prediction model using LSTM and optimize its performance with Bayesian Optimization. LSTMs are a type of recurrent neural network well-suited for time series data like stock prices due to their ability to learn long-term dependencies.

## Dataset

The script uses a CSV file named "Quote-Equity-EICHERMOT-EQ-08-10-2023-to-08-10-2024.csv" for training and testing the model. This file should contain historical stock price data, including at least a 'Date' and 'Close' column. You can replace this with your own dataset.

## Dependencies

The following Python libraries are required to run the script:

- pandas
- numpy
- matplotlib
- scikit-learn
- tensorflow
- bayes_opt

## Usage

* **Prepare your data:** Ensure your CSV file containing the stock data is in the same directory as the script or provide the correct path. The CSV file should have a column named "Close" with the closing prices.
* **Adjust parameters:** You can modify the `look_back` variable in the script to change the number of previous days' data used for prediction.
* **Run the script:** Execute the Python script. The model will be trained, and the results will be displayed.

## Hyperparameter Optimization

The script uses Bayesian Optimization to find the optimal values for the following hyperparameters:

* `units1`: Number of units in the first LSTM layer.
* `units2`: Number of units in the second LSTM layer.
* `batch_size`: Batch size for training.

The `lstm_optimization` function defines the model architecture and training process, and the `BayesianOptimization` object handles the optimization process.

## Results

The script outputs the following:

* **Train RMSE:** Root Mean Squared Error on the training data.
* **Test RMSE:** Root Mean Squared Error on the testing data.
* A plot comparing the actual and predicted stock prices.

## Model Saving

The trained model is saved as "stock_prediction_model_RE.keras". You can load and reuse this model for future predictions.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for bug fixes, improvements, or new features.


