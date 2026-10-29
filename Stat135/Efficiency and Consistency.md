To determine if a estimator is efficient, the variance must be low, near zero. 

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
$$
\lim_{n \to \infty} P(|\hat{\theta}_n-\theta|>\epsilon) = 0
$$
Equivalently, 
$$
\lim_{n \to \infty} P(|\hat{\theta}_n-\theta|<\epsilon) = 1
$$
*By the continuous mapping theorem, $g(\hat{\theta})$ is a consistent estimator of $g(\theta)$*![[Pasted image 20261029070000.png]]

Theorem 
if the MSE($\hat{\theta}_n$) converges to zero, then $\hat{\theta}_n$ is a consistent estimator of $\theta$.

The MSE is equal to Bias($\hat{\theta})^2$ + Var($\hat{\theta}$), so in order to prove the estimator is consistent, we need to prove 
the bias 
$$
Bias(\hat{\theta}_n) = E[\hat{\theta}_n] - \theta \to 0 \ as \ n \to \infty
$$
and variance 
$$
Var(\hat{\theta}_n) \to 0 \ as \ n \to \infty
$$
of the estimator both converges to zero.


However the reverse is not true, a consistent estimator does not mean the MSE is zero

## Robustness
How well does the estimate respond to "strange data" that doesn't match its underlying assumptions?

### Sensitivity Curve
$x_0$ being the added data point. The difference divided by 1/n+1
$$
SC(x_0) = \frac{\hat{u}(x1,...,x_n, x_0) - u(x_1,...,x_n)}{1/n+1}
$$
![[Pasted image 20261029091921.png]]x-axis: the value x0 being added
y-axis: sensitivity = the difference between the estimate and estimate + added point x0 