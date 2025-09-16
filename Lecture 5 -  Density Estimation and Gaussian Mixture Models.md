
## Probability Review

The variance of a random variable is defined as 

$$
var[X] = E[(X - E[X])^2]
$$

We can break this with linearity of expectation
$$
var[X] = E[X^2] - E[X]^2
$$

Properties of variance
$$
var[aX + b] = a^2 var[X]
$$

**Covariance**


## Density Estimation

Methods for estimating the best parameters for a distribution

Maximum Likelihood Estimation (MLE): choosing the parameters that maximize the likelihood of the data (frequentist)


Maximum A Posteriori (MAP) Estimation: choose the parameters that maximize the posterior given the data and the prior (Bayesian)
- recommended when you don't have a lot of data

Most of ML uses MLE because there is usually abundant amount of data.