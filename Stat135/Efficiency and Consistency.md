To compare two estimators, we can look at the efficiency

For example, the mean and median

Efficiency of two estimators
$$
Eff(\hat{\theta}, \tilde{\theta}) = \frac{Var(\hat{\theta})}{Var(\tilde{\theta})}
$$
If Eff < 1, then $Var(\hat{\theta}) < Var(\tilde{\theta})$ => $Var(\hat{\theta})$ is better

## The Cramer-Rao Inequality
$$
Var(\hat{\theta}_n) \ge \frac{1}{nI(\theta_0)}
$$
$I(\theta_0)$ the fisher information
$$
I(\theta_0) = -E_\theta[Log''(f(X;\theta))]
$$


## Consistency
Prereqs: convergence, markov's inequality, and chebyshevs inequality.

A estimator is consistent if it converges in probability to the true population parameter 

if the MSE($\theta$) converges to zero.

The MSE is equal to Bias($\hat{\theta})^2$ + Var($\hat{\theta}$), so in order to prove the estimator is consistent, we need to prove the bias and variance of the estimator converges to zero.

However a consistent estimator does not mean the MSE is zero
