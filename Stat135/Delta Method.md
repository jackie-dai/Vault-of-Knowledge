
## Estimating functions of the distribution
So far we estimate the parameters of the distribution by finding the MLE of $\theta$

To find the estimate of a function of the distribution, such as the mean of a exponential distribution $\frac{1}{\lambda}$, we can simply substitute the MLE $\hat{\lambda}$ into the mean $\frac{1}{\hat{\lambda}}$

To estimate the mean or variance, the function must be linear. If it is nonlinear, we can apply the Taylor expansion to linearize it.

## Taylor Expansion 
$$
g(x) = \frac{g^{i}(a)}{i!}(x-a)^i + R_k(x)
$$


1st order:
$$
g(x) = g(a) + g'(a)(x-a)
$$
with a single parameter

1st order
$$
g(x, y) = g(a, b) + \frac{\partial}{\partial a}g(a, b)(x-a) + \frac{\partial}{\partial b}(a, b)(y -b)
$$
with multiple parameters


Delta method
$$
	Var(g(\hat{\theta})) = [g'(x)]^2Var(X)
$$