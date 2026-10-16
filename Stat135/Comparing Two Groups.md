

## Assumptions we need to make
1) Determining what to estimate
	1) Usually a function of the parameters i.e. the difference in their means
		$\Delta = u_x - u_y$
2) Independence
	1) the data must be independent for the following to work but there is the case of paired data
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


## Paired Data
What if the two groups are not independent?

Paired data ($X_i$, $Y_i$), where $n_X=n_Y$ 

Interested in the difference
$$
D_i=n_X-n_Y
$$
$$
E[D_i]=u_X-u_Y
$$
$$
\sigma^2_D=Var(X_i) +Var(Y_i) - 2Cov(X_i, Y_i)
$$
$$
\sigma^2_D = \sigma^2_X +\sigma^2_Y - 2p \sigma_{X_i} \sigma_{Y_i}
$$