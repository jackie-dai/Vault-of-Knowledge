
## Calculating the MLE

MLE is useful because it can be applied to a number of problems and has nice theoretical properties

Algorithm *if the join density is i.i.d*
1.  find liklihood function
	1. $lik(\theta)= \Pi_f(X_i|\theta)$
2. Log liklihood
	1. $l(\theta)=\Sigma log[f(X_i|\theta)]$
3. Find partial derivatives with respect to the parameters
4. Set each partial derivative equal to zero and solve for the parameter to find the MLE

## Calculating the MLE with Multiple Parameters

This beginning steps are the same as MLE with one parameter
1. choose a parametric model
2. find likelihood function
3. find log likelihood functin
This is where it starts to get different
4. Partial derivatives wrt to each parameter
5. Set first partial derivative to zero and solve
6. Plug in the estimate for the first parameter into the second equation
7. Rinse and repeat until estimates for all parameters have been found

Theorem
*The MLE will always tell you that the best way to estimate the mean of any distribution is the mean itself*

## Simple Regression
This is useful when we apply MLE to linear regression and we are able to estimate the best parameters to $\beta_0, \beta_1,$
