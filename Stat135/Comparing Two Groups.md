

## Assumptions we need to make
1) Determining what to estimate
	1) Usually a function of the parameters i.e. the difference in their means
		$\Delta = u_x - u_y$
2) Independence
	1) Paired data ($X_i$, $Y_i$) where $n_x=n_y$ 
	2) Each pair $X_i, Y_i$ isn't neccesarily independent.
3) Model to use
	1) Use the same model for both groups?

## Estimating the parameters
$$
E[\Delta] = u_x-u_y
$$
The variance
$$
var(\Delta)=var(X) + var(Y) - 2Cov(X,Y)
$$
If it is independent, then the cov cancels out to zero
$$
var(\Delta)=\frac{\sigma^2_x}{n_x} + \frac{\sigma^2_y}{n_y}
$$
The standard error
$$
S_\bar{\Delta}=\sqrt{\frac{S^2_x}{n_x} + \frac{S^2_y}{n_y}}
$$
### The T-statistic/distribution
Previously for small sample sized CI, we have 
$$
T=\frac{\bar{X}-u}{S/\sqrt{n}}
$$
For a two sample comparison, it would be
$$
T=\frac{\bar{\Delta}-\Delta}{S_\bar{\Delta}}
$$
When n is small and assuming independence, the confidence interval becomes
$$
\bar{\Delta} \pm t_a/2,v S_\bar{\Delta}
$$
where v = the degrees of freedom = min($n_X -1$, $n_Y - 1$)

