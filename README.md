# Credit_Risk_Analysis

## Overview
In this project, we used multiple resampling methods and machine learning models to predict loan risk.

## Methods:

- Used logistic regression model to predict credit risk with two different resampling methods: Random Over Sampler, SMOTE Oversampling, Cluster Centroids undersampling
- Used the combination of over- and under- sampling method SMOTEENN algorithm to reduce sampling bias
- Compared two machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, in predicting credit risk

Balanced accuracy score, confusion matrix and imbalanced classification report were used to evaluate the performance of these methods and models.

**Data Source**: LoanStats_2019Q1.csv
Software: Python 3.8.8, jupyter Notebook 6.4.4 

## Results

###Logistic Regression

<center>

| Sampling Methods | Naive Random Oversampling |  SMOTE Oversampling |Cluster Centroids undersampling| SMOTEENN|
|:-----------|:------:|:------:|:------:|:------:|
| Accuracy Score: | 0.68 | 0.66 |0.66|0.53|
| Precision High Risk | 0.01 | 0.01  |0.01|0.01|
| Precision Low Risk | 1.00 | 1.00  |1.00|1.00|
| Recall High Risk | 0.75 | 0.66  |0.67|0.73|
| Recall Low Risk | 0.61 | 0.65 |0.39|0.58|
| Average Precision| 0.99 | 0.99 |0.99|0.99|
| Average Recall | 0.61 | 0.65 |0.39|0.58|

</center>

### Ensemble Models

<center>

| Models | Balanced Random Forest Classifier| Easy Ensemble AdaBoost Classifier |
|:-----------|:---------------:|:----------------:|
| Accuracy Score: | 0.67 | 0.69 |
| Precision High Risk | 0.02 | 0.02 |
| Precision Low Risk | 1.00 | 1.00 |
| Recall High Risk | 0.50 | 0.58 |
| Recall Low Risk | 0.84 | 0.80 |
| Average Precision| 0.99 | 0.99 |
| Average Recall | 0.84 | 0.80 |

</center>

## Summary

Using the different sampling approaches didn't significantly improve the losgistic models. Base on the results, we recommand using Balanced Random Forest Classifier or Easy Ensemble AdaBoost Classifier. Although the  since the average recall out perform all the logistic model with different sampling methods. To improve the model, we recommand to sort the features based on feature importance, and retrain the model using the most significant features.