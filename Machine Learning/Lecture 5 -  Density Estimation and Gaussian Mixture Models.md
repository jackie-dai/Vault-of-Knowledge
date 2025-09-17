
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

**The Likelihood Function** describes the probability of the observed data under a particular distribution.

$$
p(D|w) = \prod_{n=1}p(x_n|w)
$$
x is the observation and the w is the parameter. We are trying to find a w that maximizes the chance of success 

We usually take the log of the likelihood function, so we can work with summations

$$
ln p(D|w) = ln\Sigma{p(x_n | w)}
$$


### Normal (Gaussian) Distribution

$$
X-N(x|\mu, \sigma^2)
$$


$E[X] = \mu$, $Var[X] = \sigma^2$
