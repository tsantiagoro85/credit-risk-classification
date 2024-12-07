# Module 20 Report

## Analysis Overview

The purpose of the present challenge was to use various techniques to train and evaluate a model based on loan risk. A provided dataset of historical lending activity from a peer-to-peer lending services company was used to build a model that could identify the credit worthiness of borrowers. Briefly, the dataset included information regarding loan size ($), interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt and loan status.
In order to predict healthy and high-risk loans, labels sets (y) from the "loan_status" column were created. In addition, a features (X) dataframe was created from the remaining columns. The data were split into training and testing sets using train_test_split, and a random state of 1. A logistic regression model was created using the original data and the function LogisticRegression() from sklearn.
Finally, the model's performance was evaluated using a confusion matrix and a classification report.

## Results

The confusion matrix results of the model showed the following values:
 * TP: 18673
 * FP: 32
 * FN: 86
 * TN: 593

The number of true positives (TP) greatly surpassed the values of false positives (FP) and false negatives (FN), which usually will provide an indication of how good the precision, recall and f1-score values will be.

The classification report results showed that the precision, recall and f1-score values for healthy loans were excellent (i.e., 1.00). While the precision, recall and f1-score values for predicting high-risk loans were not as high as predicting healthy loans (i.e., 0.87, 0.95 and 0.91, respectively), the prediction was still very good. See results below:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.95      0.91       625

    accuracy                           0.99     19384
   macro avg       0.94      0.97      0.95     19384
weighted avg       0.99      0.99      0.99     19384


## Summary

The tested model seemed to have performed well in both cases where healthy and high-risks loans were predicted. The prediction of healthy loans was excellent compared to high-risk loans, but the latter was also very good. These results suggest that performance may dependend on the variables being predicted, but also on the robustness of the data, and the models being applied.
