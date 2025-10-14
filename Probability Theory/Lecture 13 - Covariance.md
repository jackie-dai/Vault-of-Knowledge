
$$
Var[X+Y] + Var[X] + Var[Y] + 2E[D_X,D_y]
$$
$$
 Cov[X,Y] = 2E[D_X,D_y]
$$
Covariances are difficult to directly calculate.

Instead use covariance properties.

There are two uses for covariances
1. Normalizing units (correlation)
	$$
	\frac{Cov[X,Y]}{\sigma_x \sigma_y} = E[(\frac{X-u_x}{\sigma_y})(\frac{Y-u_y}{\sigma_y})]
		
	$$
	The expected product of the standard units
	$$
	r(X, Y) = \frac{Cov[X,Y]}{\sigma_x \sigma_y}
	$$
2. Calculating the variances of sums
	$$
	Var(X+Y) = Var(X) + Var(Y) + 2Cov(X, Y)  
	 $$
### Covariance Properties

covariances are symmetric
$$
Cov[X,Y] = Cov[Y, X]
$$

Covariance with a constant is zero
$$
Cov[X, c] = 0
$$

$$
Cov[aX + bY, W] = aCov[X, W] + bCov[Y, W]
$$
Constants don't vary
$$
Cov[X+c, Y] = Cov[X, Y]
$$

$$
Cov[X, X] = Var[X]
$$
$$
Cov[X, Y] = E[(X-u_x)(Y-u_y)] = E[XY-u_xY - Xu_y + u_xu_y] = E[XY] - u_xE[Y] - u_y E[X] + u_x u_y
$$
$$
Cov[X, Y] = E[XY] - u_x u_y
$$

### Addition Rule
If X are independent random variables
$$
 Var(S_n) = \Sigma_{i=1}^{n} Var(X_i)
$$
Directly take the sum of the variances

### Variance of IID Sum
S_n = X_1 + X_2 + ... + X_n

E(S_n) = nu
$$
Var(S_n) = n\sigma^2 
$$

$$
SD(S_n) = \sqrt{n\sigma}
$$



## Indicators

### Covariance of indicators

if i != j
$$
Cov(I_a, I_b) = E[I_aI_b] = E[I_a]E[I_b] = P(I_aI_b)-P(I_a)P(I_b)
$$


### Symmetry
For the variance of a sum, if each X is symmetric, that is, $E(X_1) = E(X_2)$

$$
	Var(S_n) = nVar(X_1) + n(n-1)Cov(X_1, X_2)
$$

