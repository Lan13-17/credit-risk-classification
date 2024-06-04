# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

The goal of this analysis is to create a model that can accurately identify whether a loan is risky or healthy. We take a look at people's loan size, the interest rate, income, debt to income ratio, number of accounts, derogatory marks, and total debt in order to predict their loan status. To construct the model we first seperate the data into our target and our features before spliting them for training and testing using `train_test_split`. We then create a new model using `LogisticRegression` and train it using the training data before having it make predictions of the target with the features test data. Then we compare its predictions to the actual target test data and measure its performance by using a confusion matrix (`confusion_matrix`) and a classification report (`classification_report`).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
        * Accuracy: The overall accuracy of the model is 0.99 meaning that 99% of the time it correctly labeled the loans.
        * Precision: The model's precision score for healthy loans is 1 meaning that every loan labeled as healthy was correctly labeled. The model's precision score for risky loans is 0.85 meaning that 85% of loans labeled as risky were correctly labeled.
        * Recall:The model's recall score for healthy loans is 0.99 meaning that 99% of healthy loans were identified. The model's recall score for risky loans is 0.91 meaning that 91% of risky loans were identified.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Based off the confusion matrix we can see that almost all of the healthy loans were identified correctly, however a larger number of risky loans were incorrectly labeled. The model is much better at correctly predicting healthy loans most likely due to the lack of data for risky loans in comparison. It's better to try and predict if it's a healthy loan when using this model.