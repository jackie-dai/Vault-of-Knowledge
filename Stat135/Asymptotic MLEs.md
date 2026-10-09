
## Fisher Information
Start with the log-likelihood $L(\theta)$

The fisher information is 
$$
I(\theta)=-E[\frac{\partial^2}{\partial^2\theta}L(\theta)]
$$
Take the partial derivative of L($\theta$) and then again to get the second derivative.

Plug in E(X) <- should be known

Take the negative expectation of the second deriviative of $Log(\theta)$ to get $I_n(\theta)$


## Confidence Intervals

$$
\theta_n \pm z_{a/2} \hat{SE}
$$
Now for an asymptotic CI, we can calculate the SE like so

$$
SE=I_n(\hat{\theta})^{-1/2}
$$
And plug that into our confidence interval
$$
\theta_n \pm z_{a/2} I_n(\hat{\theta})^{-1/2}
$$


