
**Estimator**: the function that maps sample data to a number
**Estimate**: the actual observed value after applying the estimator on the observed data

![[Pasted image 20260126120759.png]]

Now we need to measure how good our estimator is compared to the actual value.

By taking random samples and creating estimators out of the random samples, we can create a probability distribution of the estimator.
![[Pasted image 20260126120945.png]]

We can measure how good our estimator is by measuring the spread of the sampling distribution around the mean (target: population parameter), this is the square root of the variance, called the standard error or mean squared error

$$
MSE=E[(\hat{\theta}-\theta)^2]
$$$$
	Bias(\hat{\theta}) = E[\hat{\theta}] - \theta
$$
A estimator is unbiased if $E[\hat{\theta}]=\theta$
