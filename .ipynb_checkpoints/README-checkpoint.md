# Credit Risk Analysis Report

## Purpose of the analysis. 

The purpose of credit analysis with logistic regression is to assess the creditworthiness of borrowers and predict the likelihood of default or non-performing loans using a logistic regression model. Logistic regression is a statistical modelling technique used for binary classification problems, making it suitable for predicting credit risk outcomes.

The key purposes of credit analysis with logistic regression are:

1. Credit Risk Assessment
2. Model Development
3. Probability Estimation
4. Risk Modeling and Validation
5. Interpretability and Transparency
6. Continuous Monitoring and Model Enhancement

## What financial information the data was on, and what you needed to predict. 

The dataset used was of historical lending activity from a peer-to-peer lending services company. Through analysing this information, we can build a model that can identify the creditworthiness of borrowers

## Basic information about the variables you were trying to predict (e.g., value_counts). 

* value_counts() - used in data analysis to obtain the frequency count of unique values in a column or series of data
* train_test_split - used to split a dataset into training and testing subsets to ensure that the data is shuffled before the split to prevent any biases
* balanced_accuracy_score - used to calculate the balanced accuracy score, which is a metric for evaluating the classification performance of a model, especially in imbalanced datasets where class distribution is unequal
* confusion_matrix - provides a summary of the predictions made by the model and how they compare to the actual labels or ground truth
* classification_report_imbalanced - used to generate a classification report, which includes various evaluation metrics for each class in a classification problem

## Stages of the machine learning process you went through as part of this analysis. 

To fulfil this analysis, the data had to be split into Training and Testing Sets through the use of train_test_split. Then a Logistic Regression Model was created with the Original Data. To do this, a logistic regression model was fitted by using the training data (X_train and y_train). Then the predictions were saved on the testing data labels by using the testing feature data (X_test) and the fitted model. After the model was created and fitted and predictions were created, the accuracy score of the model was calculated and a confusion matrix and classification report was generated.

Then this process was repeated with resampled training data. This was done with the RandomOverSampler module from imbalanced-learn

## Methods you used (e.g., LogisticRegression, or any resampling method).

* RandomOverSampler - class provided by the imbalanced-learn library in Python. It is used for oversampling the minority class in imbalanced datasets by randomly duplicating instances from the minority class until the class distribution becomes balanced.
* LogicsticRegression - statistical model used for binary classification problems, where the target variable has two possible outcomes

## Results
Here's a breakdown of the metrics for each model:

Model 1:
* Precision (pre): 1.00 for class 0, 0.85 for class 1
* Recall (rec): 0.99 for class 0, 0.91 for class 1
* Specificity (spe): 0.91 for class 0, 0.99 for class 1
* F1 score (f1): 1.00 for class 0, 0.88 for class 1
* Geometric mean (geo): 0.95
* Index of balanced accuracy (iba): 0.91
* Support (sup): 18765 for class 0, 619 for class 1


Model 2:
* Precision (pre): 1.00 for class 0, 0.84 for class 1
* Recall (rec): 0.99 for class 0, 0.99 for class 1
* Specificity (spe): 0.99 for class 0, 0.99 for class 1
* F1 score (f1): 1.00 for class 0, 0.91 for class 1
* Geometric mean (geo): 0.99
* Index of balanced accuracy (iba): 0.99
* Support (sup): 18765 for class 0, 619 for class 1

As supervised learning models, both Model 1 and Model 2 demonstrate high performance with high precision, recall, specificity, and F1 scores.

In terms of overall performance, Model 2 appears to have slightly better metrics across the board, including higher specificity for both classes and a slightly higher precision for class 1. This suggests that Model 2 might have better generalization and discrimination capabilities, making it a potentially stronger choice. However due to these higher metrics, this may make model 2 “too good to be true” making this model less desirable.
