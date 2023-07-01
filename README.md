# credit-risk-classification


## Overview of the Analysis
The purpose of the credit risk analysis exercise is to evaluate the performance of 2 Logistic Regression Models and determine which one provide best balance accuracy. The models were used to predict the results of a'healthy loan' and 'high risk loan' applicants. The financial information used for the analysis included the loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogetory marks, and total debt. We will then test this model to determine how effective it is at classifying both categories.

## Results

**Under Model 1** - used a dataset of 77,536 loans application, which 75,036 where for healthy loans and 2500 for high-riks loans and presented the results below:

* Machine Learning Model 1:
![Classification Report](./credit-risk/classification_report.png)

**Question:** How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** 
- Model precision: the precision (which measures the accuracy of positive predictions made by the model, in other words, number of correct positive predictions), shows that for healthy loans, (0), the model accuracy is very high - 100%. For high-risk loans the model accuracy is 85%. This means that the model has a very low rate of false positives for the healthy loans (basically 100% accuracy), but it is not 100% accurate in identifying all the false positives for the high-risk loans.

- Model recall: which is the true positive rate for the total number of positive predictions. For health loans,(0), it can predict 99% of positive and for unhealthy 91% of total positive, meaning, that the model has a low rate of false negatives for healthy loans, and a very fairly rate for high-risk loans; although it cannot predict all the false negatives for the high-risk loans.

- F1 = which is the mean of the precision and recall and considers both the false positives (precision) and false negatives (recall).

In general, the model 1 was highly efficient in predicting the healthy loans and has a moderate to high precision to predict the high-risk loans, but still a very accurate model.

**Under Model 2** - We used the "resampled training data" to normalize the size of healthy loans and high-riks loans, the total dataset for both were 56,271 loans and presented the results below:
* Machine Learning Model 2:
 ![Classification Report](./credit-risk/classification_report2.png)

**Question:** How well does the logistic regression model, fit with oversampled data, predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** 
Model precision: the precision (which measures the accuracy of positive predictions made by the model, in other words, number of correct positive predictions), shows that the model accuracy is very high - 100% for both healthy and a moderate accuracy of 84% for high-risk loans. This means that the model has a very low rate of false positives for healthy loans, but a moderate rate for high-risk loans.

Model recall: which is the true positive rate for the total number of positive predictions. The model predict 99% of total positive, meaning, that the model has a low rate of false negatives for both healthy and high-risk loans.

F1 = which is the mean of the precision and recall and considers both the false positives (precision) and false negatives (recall).


## Summary

In general, the logistic regression model 2 is highly efficient in predicting the healthy and high-risk loans with a balance accuracy of 99% versus the  balance accuracy of 95% calculated under model 1. My suggestion is to use Model 2 for the credit risk analysis.
