

## Classification Problems



### Train-test split
1. shuffle the training data
2. split into two parts
	1. training part (80% of data): train and develop model
	2. testing part (20% of data): test and validate model

### Feature Engineering

We can either **select features** or **encode features**

**One-hot encoding**

**Feature Standardization**
Using the training data to compute the mean and variance of the feature x and then apply the following transformation
![[Pasted image 20250904144904.png]]
to obtain the new feature z with zero mean and unit variance

Encoding image (we will do this in the homework)

**Regularization** is the process of adding constraints or penalties to the learning process to improve generalization

## Logistic Regression Model

Logistic regression is a linear model for classification

**Hyperparameters** are the parameters held constant during optimization (training) algorithm

## Making Predictions

**Inference* is the process of making predictions with a model

Label prediction

Predicted distribution