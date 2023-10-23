# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The financial information the data was on inlcuded the following : The size of the loan, the interest rate, the borrowere's income, the debt to income ratio, the number of accounts the borrower held, derogatory marks against the borrower, and the total debt. The goal was to predict the loan status based on the avaialbale data.

During the first stage of the machine learning process the "train_test_split" function of the scikit-learn library was used to split the data into two sets, one for training and the othe for testing. The training set was used to train the logisitic regression model using "LogisticRegression" function from the scikit-learn library, while the testing set was used to test the performance of the trained logistic regression model at classifying the borrower as a high or low risk. 

During the second stage of the machine learning process the "RandomOverSampler" function from the imbalanced-learn library was used to resample the training data in order to ensure that the logistic regression model had an equal number of data points to draw from since the intitial model was drawing from a dataset that had 75,036 low-risk loan data points and 2,500 high-risk data points. The resampling of the training data resulted in having 56,271 data points for both low and high risk loans. 

## Results

### Before using the "RandomOverSampler" function the results were as follows:

- According to the the balanced_accuracy score, the logistic regression model was 95% accurate at predicting the healthy vs high-risk loan labels. 
- According to the classification report, the results were as follows:
    - Precision for the healthy loans was 1.00, the recall was 0.99, and the f1-score was 1.00, meaning that the model is pretty accurate at predicting healthy instances.
    - Precision for high-risk loans was 0.85, the recall was 0.91, and the f1-score was 0.88, meaning that the model not very accurate at predicting high-risk instances.

### After using the "RandomOverSampler" function the results were as follows:

- According to the the balanced_accuracy score, the logistic regression model was 99% accurate at predicting the healthy vs high-risk loan labels. 
- According to the classification report, the results were as follows:
    - Precision for the healthy loans was 1.00, the recall was 0.99, and the f1-score was 1.00, meaning that the model is pretty accurate at predicting healthy instances.
    - Precision for high-risk loans was 0.84, the recall was 0.99, and the f1-score was 0.91, meaning that the model not very accurate at predicting high-risk instances.

## Summary

According to the balanced_accuracy score, the logistic regression model performed much better after resampling the data, its accuracy went from 95% to 99%. According to the classification report, both models performed really well at prediticing healthy loans, however, for high risk laons, resampling resulted in better recall and accuracy ratios but slightly lower precision. In summary, the second model had overall fewer false predictions and it's better to be used based on its higher acccuracy and recall. 


