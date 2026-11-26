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

# Overfitting & underfitting
test the model on training and test data to make sure when the model is over fitted and underfitted
Bias is error from overly simple model assumptions that miss real patterns, while variance is error from a model reacting too strongly to training data noise
• High Bias (Underfitting): The model is too rigid or simple. It produces high error on both training and unseen test data.
• High Variance (Overfitting): The model memorizes training data and random noise. Training error is low, but test error spikes on new data.