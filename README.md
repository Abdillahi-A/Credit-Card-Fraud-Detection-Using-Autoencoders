# Credit-Card-Fruad-Detection-Using-Autoencoders

## Introduction

Anomaly detection is concerned with identifying data points that do not quite fit the norm. One common application of anomaly detection is in finance, where banks attempt to discern between fraudulent transactions vs genuine ones.

## Data  

This project uses data from the Credit Card Fraud Detection dataset on Kaggle. The datasets contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. Due to file size restrictions on Github I could not upload the csv file onto the repository. However, you can access a zip file of the dataset from this link:
 https://www.kaggle.com/mlg-ulb/creditcardfraud


## Goal

Develop a deep learning model (autoencoder) to identify fraudulent transactions.  

## Result

Setting a very sensitive threshold of 0.09, leads to a very strong model in terms of recall where our model is able to correctly identify 111 fraudulent transactions out of 113. However, such a sensitive threshold comes with an opportunity cost of a reduced precision i.e. there are more than 23700 false positives.

Increasing the threshold value to 0.8 reduces recall (although since our data is heavily imbalanced it hardly shows). Now our model only correctly identifies 89 fraudulent transactions out of 113 (the number of false negatives increases from only 2 to 24). However, the number of false positives drastically reduces from above 23700 to 1403.

