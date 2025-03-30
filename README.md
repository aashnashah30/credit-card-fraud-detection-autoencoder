# Credit Card Fraud Detection and Classification Accuracy Verification using Autoencoders in Keras

## Introduction

This repository contains code for detecting credit card fraud using an autoencoder neural network implemented in Keras. Additionally, it incorporates a mechanism to verify the accuracy of the classification, determining whether the identified fraud is genuinely fraudulent or a false positive. This dual functionality enhances the reliability of the fraud detection system.

The project utilizes the publicly available "Credit Card Fraud Detection" dataset from Kaggle, which is highly imbalanced.

## Methodology

* **Autoencoder for Anomaly Detection:** A multi-layer autoencoder is employed to learn the normal patterns of credit card transactions. Fraudulent transactions, being anomalies, exhibit higher reconstruction errors.
* **Classification Accuracy Verification:** After the autoencoder identifies potential fraud, a separate component analyzes the transactions flagged as fraudulent. This component aims to verify if the classified fraud is indeed a true positive. This may involve further analysis of the reconstruction error patterns, or additional classification or rule based methods.
* **Data Preprocessing:** Numerical features are scaled using `StandardScaler` to ensure consistent input ranges for the neural network.
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
