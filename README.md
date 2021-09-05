# ML-Telecom-Customer-Retention
Machine Learning Models about telecom customer retention rate, given customers behavior data, the selected model will be able to predict whether customer will stay with the service. It will help company to make important business decision.

## Background
Telecom operator would like to be able to forecast their churn of clients. If it's discovered that a user is planning to leave, they will be offered promotional codes and special plan options. Its marketing team has collected some of their clients' personal data, including information about their plans and contracts.
Supervised models are developed to predict customer behavior in order to help.

## Work Plan
### Step 1.
 - 1.1 We found there are mismatch in numbers of users in different dataframe, we first join all four data sets, then we fill them with a value 'NA', so when we encode the features, the customers who did not use internet or phone service will be recognized by the model.
 - 1.2 When we encode features, we use label encoding on only catagorical features because we want to keep the numerical properties of some of the features like 'longevity', 'monthlycharges' and so on.
### Step 2.
 - 2.1 We will split the data, normalize the data in training set and validation set. 
 - 2.2 We will use a logistic regression model as a dummy model for comparison.
 - 2.3 The evaluation metric will be AUC-ROC and we will use accuracy as a additional metric to evaluate the model.
 - 2.4 We found there is a class imbalance in target, so we will upsample the data and train models to both original data and upsampled data to compare.
 - 2.5 Cross validation will be used for better accuracy.
### Step 3.
 - 3.1 We will train a catboost classifier model and evaluate the model with AUC-ROC and accuracy metrics.
 - 3.2 We will also implement dense neural network to our model with 'sigmoid' activation and one output.

## Result
We found catboost model is best in quality by using metrics to measure, it succefully predict customer churn tendancy with high accuracy and good AUC-ROC score.
