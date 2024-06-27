# Module 12 Report Template

## Overview of the Analysis

This analysis is to test that accuracy to which machine learning models can predict whether a loan is healthy or high-risk, based on factors such as loan size, income, borrowing amount, and number of accounts. To do this analysis, train test split was used to split the dataset, then a logistic regression model was fitted using the training data, predictions were made using the testing and training data, and this was then used to create a confusion matrix and a classification report.

This created reports assessing the accuracy of classification by the machine learning model, as well as providing an understanding of how the class imbalance affects the model.

## Results

* Machine Learning Model 1:
    * Positive Prediction
        * Precision: 1.00
        * Recall: 0.99
        * F1 Score: 1.00
    * Negative Prediction
        * Precision: 0.85
        * Recall: 0.89
        * F1 Score: 0.87
    * Accuracy: 0.99
    * Macro Average
        * Precision: 0.92
        * Recall: 0.94
        * F1 Score: 0.93
    * Weighted Average
        * Precision: 0.99
        * Recall: 0.99
        * F1 Score: 0.99

## Summary

In this case, false positives could cause issues for the bank and other users of the bank. Failing to act cautiously could drive interest rates up for other loans, damaging the business. Using false negatives could also be damaging, as safe customers could unfairly miss out on loans, however this is more of a customer service concern than a business concern. 

For this reason, False Negatives would be less damaging than False Positives, however this is also the area where the model struggles most, potentially up to 15% of loan requests could be falsely flagged as Negative.

Ultimately, the client may be best not using this model. The cautious option of Negatives is too inaccurate, and even though it is much more accurate, using Positives could potentially lose the bank a large sum of money from far fewer mistakes. Instead, it may be better to train a Random Forest Model, which would be robust to outliers and non-linear data like this, and runs efficiently on larger databases like the bank database.