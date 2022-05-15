# DS301_FinalProject_MaggieWang_VictorWong
This repo contains the final project code for DS301 in spring 2022 in NYU

## Project Title: 
Algorithm Comparison in Fraud Card Detection

## Project Team Member: 
Maggie Wang, Victor Wong

## Project Description:
Credit Card Fraud is a common problem happening in people’s daily life. If the bank is able to detect fraudulent transactions, people manage to minimize their losses. The algorithms we are going to use aim to determine if a certain transaction is fraudulent or not. At the same time, it can help progress the bank’s volume of transactions as correct predictions in the algorithm can boost people’s confidence in the current banking system.

Our goal is to apply several algorithms to detect fraud and find out the best algorithm: the one that detects 100% of the fraudulent transactions while minimizing the incorrect fraud classifications, especially the metrics of False Negative Rate(FNR) as business tends to prioritize minimizing the failure to identify the fraud. With the correct identification of the best model that minimizes the incorrect fraud classification, we are able to avoid unnecessary business expenses and therefore greatly improve the business performance. During the process of training and fitting one specific model, we also employed hyperparameter tuning to find out the best model configuration. This can help us finding a more accurate and high-performing model during the comparison. We will be majorly looking at the metrics of F1 score as in this case we want to take FN into consideration.



## Code Structure
In this project, we imported the data of creditcard.csv to inspect the data. After the initial inspection, we preprocessed, cleaned, and split the data. Then, we built six different models based on different approaches and trained and test them on the same dataset. These six models include Artificial Neural Network(ANN), RNN, XGBoost Classifier, Random Forest Classifier, CatBoost Classifier, and LightGBM Classifier. For each one of the models that can be tuned on its hyperparameters, we used grid search iterate the possible combinations of hyperparameters and reported the one with the best performance. Then, we calculated the evaluating metrics(accuracy and f1 score) and plotted the f1 score into histograms to make a visual comparison of the model performance, which gave us a collective insight into the best model that gives the best metrics performance.


