
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


## Loss Functions

L1 Loss (absolute loss)
$$
l(y, \hat{y}) = |y-\hat{y}|
$$
L2 Loss (squared loss)
$$
l(y, \hat{y}=(y-\hat{y})^2)
$$

Huber's loss
$$
l(y, \hat{y}) = 
\begin{cases}
	\frac{1}{2}(y-\hat{y}(\theta))^2 & |y-\hat{y}| < \epsilon \\
	\epsilon(|y-\hat{y}(\theta)|-\frac{1}{2}\epsilon) & otherwise \\
\end{cases}
$$
*Because L1 loss is not differentiable at 0, it is difficult to work with. Huber's loss was made to make the best of both losses. For small values, we use L2 squared loss, and for big values, use L1 absolute loss*

![[Pasted image 20261001013550.png]]Different loss functions function differently. Here, the L2 loss is more "pulled" towards the outliers due to the square in the L2 loss. Huber acts more like L1, but still gives a slightly different estimate.

## M-Estimators
A more general way to describe loss functions

$$
min\frac{1}{n}\sum p(y, \theta)
$$
the theta that minimizes the average loss is called the M-estimator

### Principle Component Analysis (PCA)
Take the regression line

Find distance between actual point(x,y) to the regression line by taking the squared distance of the orthogonal projection

Take the distance and treat this as a our loss function. The goal is to minimize the distance by finding the MLE of the parameters

TODO: revisit another time to fill in the details https://stat135.berkeley.edu/fall-2026/Modules/06-SamplingDist.html