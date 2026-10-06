
Before we move to cross validation, it is helpful to understand validation error.

## Validation Error
Using the training data, we split into two groups, training data and validation data. 
X = (X_train, y_train), Y=(X_val, y_val)

Now fit the model on X and compute the loss with the validation data. 

## Cross Validation


This is for one fold
![[Pasted image 20261006113426.png]]
Fit on everything except the kth fold, using kth fold as validation set. *here, the sum is iterating over the data points for a single fold. All folds are equal length N/K *


Now we average the error for the rest of the folds
![[Pasted image 20261006113442.png]]