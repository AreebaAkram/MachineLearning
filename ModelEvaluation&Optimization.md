# Classification model evaluation

## Confusion matrix:
1. used for classification models
TP : actual postives predicted as +ve
TN: actual -ve predicted as -ve
FP : falsely predicted as +ve
FN: falsely predicted as -ve

## Accuracy:
total value of right predictions but can be misleading if one class is more dominant. 

## Precision:
comparison of actual positives with falsely predicted as positive. how many of +ve were actually correct
in comparison with , No of FP added

## Recall:
It shows the proportion of true positives detected out of all the actual positive instances.
w.rt. No of TP missed

## F1 score:
combines precision and recall into single matrix an di useful for imbalanced classes

# Regression model evaluation

## MAE: 
average absolute difference between actual and predicted values. treat all errors equally. provide results in the same unit as target attribute
## MSE:
 average of squared differences between actual and predicted values. penalize the larger errors, sensitive to outliers
## RMSE:
It maintains the strong penalty for large errors while converting the result back to the original unit of the target variable
## R^2 score
the proportion of variance in the target variable that is explained by the regression model e.g., 0.87 means 87%

# Cross-validation
Cross-validation is a technique used to check how well a machine learning model performs on unseen data while preventing overfitting.

it's actually the ml model performance evaluation technique, 

1. Hold out cross validation : data is divided into two parts, train and test
2. Stratfied cross validation: better for imbalanced classes, the class proportion remains balanced in both training and test data
3. K-fold cross validation: splits the dataset into k equal-sized folds. The model is trained on k-1 folds and tested on the remaining fold. This process is repeated k times each time using a different fold for testing.

its just the prerequiite technique to know which model should we use.
we can also use it for hyperparameter tuning, where we can test with diff values

helps you make an informed model-selection decision before committing to a final model.

# What can go wrong with a model?

## Overfitting & underfitting
test the model on training and test data to make sure when the model is over fitted and underfitted
Bias is error from overly simple model assumptions that miss real patterns, while variance is error from a model reacting too strongly to training data noise
• High Bias (Underfitting): The model is too rigid or simple. It produces high error on both training and unseen test data.
• High Variance (Overfitting): The model memorizes training data and random noise. Training error is low, but test error spikes on new data.

## Data Leakage:
Data leakage occurs when information from outside the training dataset—or information that would not be available at the time of prediction—is inadvertently used to train a machine learning model. This causes the model to achieve artificially high scores during training and validation, only to fail when deployed on new, real-world data

## Class imbalance:
A model that predicts the majority class more frequently may achieve an apparently respectable accuracy while performing poorly on the minority class.

## Anomalies:
anomalies and outliers

## Feature scaling
## Multicollinearity
occurs when two or more predictor variables in a regression model are highly correlated or linearly dependent, making it hard to isolate each variable's individual effect on the outcome

## Concept drift and data drift
Data drift	Input feature distributions change
Concept drift	The relationship between inputs and target changes

# Regularization:
Regularization is a technique used to prevent a machine learning model from becoming unnecessarily complex and overfitting the training data. Regularization discourages the model from learning unnecessarily complex patterns.
This means the model now has two objectives:
1. Minimize prediction errors.
2. Avoid unnecessarily large coefficients.

a very high alpha value leads to underfitting

Alpha: It controls how strongly the model penalizes large coefficients.

## Lasso Regularization

Adds the absolute values of coefficients as a penalty.
Can reduce some coefficients to exactly zero. thus selecting only that are imp
Performs feature selection.
Useful when some features may be irrelevant.

## Ridge Regularization
Adds the squared values of coefficients as a penalty.
Reduces coefficient magnitudes.
Usually does not make coefficients exactly zero.
Useful when several features contribute to predictions.

## Elastic Net Regularization
Combines both L1 and L2 penalties.
Can perform feature selection.
Also controls coefficient magnitudes.
Useful when features are highly correlated or when you want a combination of both approaches.


# Hyperparameter tuning:
is the process of selecting the optimal values for a machine learning model's hyperparameters

Model parameters
These are values that a model learns automatically during training. e.g., weights, and bias in linear reg
Model hyperparameters
These are values that we configure before training. They control how the model learns. e.g., regularization, alpha, gamma, kernel type

Our objective is to find hyperparameters that help the model generalize well to unseen data.
Hyperparameters are configured before training; model parameters are learned during training.

## Method 1: Grid Search CV (cross validation)
Grid Search tests every possible combination of hyperparameters that we provide.

## Method 2: Random Search CV
randomnly try diff combinations from the space