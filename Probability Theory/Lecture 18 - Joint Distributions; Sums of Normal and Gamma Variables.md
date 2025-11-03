
## Standard Normal Basics 


1. The density of $\phi$
$$
\phi(z) = \frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}z^2}
$$
2. The expectation of $\phi$
$$
E(Z) = 0
$$
$$
E(|Z|)=\sqrt{\frac{2}{\pi}}
$$
3. The variance
$$

$$

## Sum of Independent Normal Variables
The distribution of the sum of normal independent variables is the normal distribution with the following parameters:

$$
u = u_x + u_y,\sigma = \sigma_x + \sigma_y 
$$
Example:
X~Normal(20, $5^2$), Y~Normal(75, $10^2$)

f(x) = Y-2X

Expectation
$$
E[Y-2X] = E[Y]-2E[X]
$$

Variance
$$
Var(Y-2X)=Var(Y) + 4Var(X)
$$
*Variance of the square of the deviations, so negative signs always turn positive*

## Gamma

### The rate $\lambda$
For a fixed r, the larger $\lambda$ is, the smaller X will be.

The random variable Y = cX has the gamma(r, $\lambda$/c)

## The Shape Parameter $r$


## Chi Distribution
Let X be a gamma distribution with parameters $r=\frac{1}{2}$ and $\lambda = \frac{1}{2}$

This is the chi distribution with 1 degree of freedom. If we keep adding i.i.d standard normal variables
$$
Z = Z_1+Z_2 = Gamma(\frac{1}{2} + \frac{1}{2}, \frac{1}{2})
$$
Now Z is the chi distribution with 2 degrees of freedom

### Expectation
The expectation of a chi-squared random variables is its degrees of freedom
$$
E[T] = \frac{r}{\lambda}
$$
$$
X~Gamma(\frac{n}{2},\frac{1}{2})
$$
$$
E[X] = \frac{n/2}{1/2} = n
$$

