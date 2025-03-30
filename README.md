# Credit Card Fraud Detection using Autoencoders in Keras

## Introduction

This repository contains code for detecting credit card fraud using an autoencoder neural network implemented in Keras. Autoencoders are particularly effective for anomaly detection, as they learn to reconstruct normal data patterns, making fraudulent transactions (anomalies) stand out with higher reconstruction errors.

The project utilizes the publicly available "Credit Card Fraud Detection" dataset from Kaggle, which is highly imbalanced.

## Methodology

* **Autoencoder Architecture:** A multi-layer autoencoder is employed. The encoder compresses the input data into a lower-dimensional representation, and the decoder reconstructs the original input from this compressed representation.
* **Anomaly Detection:** Fraudulent transactions are identified by calculating the reconstruction error (Mean Squared Error) between the original and reconstructed transactions. Transactions with a reconstruction error exceeding a predefined threshold are flagged as potential fraud.
* **Data Preprocessing:** The numerical features are scaled using `StandardScaler` to ensure consistent input ranges for the neural network.
* **Model Training:** The autoencoder is trained using the Adam optimizer and Mean Squared Error (MSE) loss function.

## Dataset

* **Source:** [Credit Card Fraud Detection dataset from Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* **Description:** The dataset contains transactions made by European cardholders in September 2013. It presents transactions that occurred in two days, with 492 frauds out of 284,807 transactions. The dataset is highly imbalanced, with fraudulent transactions representing approximately 0.17% of the total data.
* **Data Handling:** Due to the severe class imbalance, results can be heavily influenced by this.

## Requirements

* Python 3.x
* TensorFlow/Keras
* Pandas
* Scikit-learn
* NumPy

