
## Bernoulli(p)
One trial with probability p and possible values 0 and 1

## Binomial(n, p)
*n* independent Bernoulli(p) trials 
- *n*: number of trials
- p: probability of success for each trial

$$
P(S_n=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$
## Poisson($\mu$)
When n is large and p is small, the chance of k successes in n Bernoulli(p) trials is roughly

$$
P(k)=exp({-\mu\frac{u^k}{k!}})
$$
where $\mu$=np

## Geometric(p)
In a sequence of i.i.d bernoulli(p) trials, let X be the number of trials until the **first** success.
$$
P(X=k)=q^{k-1}p
$$
$$
E[X]=\frac{1}{p}
$$
## Hypergeometric(N, G, n)
Let N=G+B, where G is the number of good elements, and B is the remaining number of bad elements

Let X be random variable of the number of good elements in the sample. g is a possible value of X
$$
P(X=g) = \frac{\binom{G}{g}\binom{B}{b}}{\binom{N}{n}}
$$
N=total population size, n=sample size

## Uniform
$$
	\frac{1}{b-a }
$$
The probability of picking x between the interval a and b is equal/uniform.

## Normal($\mu$, $\sigma^2$)

## Exponential($\lambda$)
The exponential distribution is often used as a model for random lifetimes. Think of T as the lifetime of an object like a lightbulb, and t as the chance that the object dies before time t.
$$
	P(X<t) = 1-e^{-\lambda t}
$$

$$
P(X>t) = e^{-\lambda t}
$$
*The exponential distribution is the continuous version of the geometric distribution.*
Geometric: number of trials until the first success
Exponential: time until the first success


## Gamma($r, \lambda$)

## Beta(r, s)

## Chi-Square(n)

