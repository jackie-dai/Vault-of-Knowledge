
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