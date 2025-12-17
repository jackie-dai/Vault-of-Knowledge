
## Simple Regression
Predict Y by $aX+b$

Criterion: Minimize mean squared error

$$
MSE(a,b) = E[(y-(aX+b))^2]
$$
**Best slope a***
$$
a^*= \frac{Cov(X,Y)}{SD(X)SD(Y)}
$$
**Best Intercept b**
$$
b^*=E(Y) - a^*E(X)
$$
Regression line is
$$
y=a^*x+b^*
$$

In order to find the **least squares linear predictor,** we need to minimize the MSE over all a and b

1. Fix a and minimize MSE with respect to b
	1. Take partial derivative with respect to b
	2. Set equal to 0
	3. Solve for b
2. Fix b and minimize MSE with respect to a
	1. Take partial derivative with respect to a
	2. Set equal to 0
	3. Solve for a
