# DS301 FinalProject by Maggie Wang and Victor Wong
This repo contains the final project code for DS301 in spring 2022 in NYU

## Project Title: 
Algorithm Comparison in Fraud Card Detection

## Project Team Member: 
Maggie Wang, Victor Wong

## Project Description:
Credit Card Fraud is a common problem happening in people’s daily life. If the bank is able to detect fraudulent transactions, people manage to minimize their losses. The algorithms we are going to use aim to determine if a certain transaction is fraudulent or not. At the same time, it can help progress the bank’s volume of transactions as correct predictions in the algorithm can boost people’s confidence in the current banking system.

Our goal is to apply several algorithms to detect fraud and find out the best algorithm: the one that detects 100% of the fraudulent transactions while minimizing the incorrect fraud classifications, especially the metrics of F1 score as business tends to prioritize minimizing the failure to identify the fraud. With the correct identification of the best model that minimizes the incorrect fraud classification, we are able to avoid unnecessary business expenses and therefore greatly improve the business performance. During the process of training and fitting one specific model, we also employed hyperparameter tuning to find out the best model configuration. This can help us finding a more accurate and high-performing model during the comparison. We will be majorly looking at the metrics of F1 score as in this case we want to take FN into consideration.



## Repository and Code Structure
For this repository, we had a .ipynb file "DS301_GroupProject_MaggieWang_VictorWong.ipynb" for the whole coding and graph sections. We implemented the graph within the .ipynb file.

In this project, we imported the data of creditcard.csv to inspect the data. After the initial inspection, we preprocessed, cleaned, and split the data. Then, we built six different models based on different approaches and trained and test them on the same dataset. These six models include Artificial Neural Network(ANN), RNN, XGBoost Classifier, Random Forest Classifier, CatBoost Classifier, and LightGBM Classifier. For each one of the models that can be tuned on its hyperparameters, we used grid search iterate the possible combinations of hyperparameters and reported the one with the best performance. Then, we calculated the evaluating metrics(accuracy and f1 score) and plotted the f1 score into histograms to make a visual comparison of the model performance, which gave us a collective insight into the best model that gives the best metrics performance.

## Example commands to execute the code    
Our python code is initiated in Google Colab(cloud based). In order to execute the code, it's suggested to download the file and .csv file and import them to the Google Colab in order to import the data without much effort. As long as .ipynb file and the .csv file are in the same folder, it's believed to function normally.

## Results

Based on the model evaluation, here are our result:
For ANNs, we did a grid search on the hyperparameter. The best parameters are:
{'batch_size': 64, 'lr': 0.034646016306089024, 'dropout_proba': 0.08979839550989333}
For test accuracy, we get: 0.9993153330290369
for test f1 score, we get: 0.812533

<img width="715" alt="image" src="https://user-images.githubusercontent.com/67981521/168461304-6d58a7f3-b79f-4359-8e73-f884a2b6679e.png">


For XGBoostClassifier, we did a grid search on the hyperparameter. The best parameter is:
n_estimators=150
For test accuracy, we get:0.999403110845827
for test f1 score, we get:0.821053

For RandomForestClassifier, we did a grid search on the hyperparameter. The best parameter is:
eta=0.1
For test accuracy, we get:0.9993504441557529
for test f1 score, we get:0.806283

For CatBoostClassifier, we fit the model and evaluate the metrics:
For test accuracy, we get:0.9993328885923949
for test f1 score, we get:0.802083

For LightGBMClassifier, we fit the model and evaluate the metrics:
For test accuracy, we get:0.9988237772550121
for test f1 score, we get:0.556291

Here, we can see that since test accuracy across the models all give a consistently high value around 0.99, it's of more importance to compare by the f1 score. The graph we generated on F1 score is attached below:
<img width="894" alt="image" src="https://user-images.githubusercontent.com/67981521/168461401-3021650b-c734-4615-b4cf-c9075ab582db.png">


The values of f1 score:
<img width="507" alt="image" src="https://user-images.githubusercontent.com/67981521/168461517-addbeb2e-2967-4499-a07d-ed9b7898b7ae.png">

Here, by comparing the f1 scores, with consideration on the test accuracy, we can come to an conclusion that for this dataset,XGBoost Classifier has the best performance in f1 score, as our special attention is regarding the False Negative cases. 



