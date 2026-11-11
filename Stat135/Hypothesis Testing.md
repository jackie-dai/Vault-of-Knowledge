In order to prove if a hypothesis is correct, we state a null hypothesis and test if the observed difference from the null is due to random variation or not. If it is unlikely, we reject the null.

## Definitions
### Null Hypothesis
An assumption that we make so we can use the probabilities under this assumption. 

For example if we want to model if a coin is fair, we can state the null is that the coin is fair and set $\pi = 0.5$

### The T-Statistic
A statistic of the difference to the null.
$$
T=|\hat{\pi}-\pi_0
$$
Estimate - Null

### Null Distribution
The distribution of observed data based on the null.


There are two standard methods: rejecting the null or not (neyman-pearson) or computing a p-values (fisher) measuring how much evidence there is against the null.

## Fisher
### P-Value
It measures how consistent the data is with the null. 
$$
P_{H_0}(T \ge t_{obs})
$$
The probability that T is as extreme or more extreme than the observed t-statistic. under the null distribution.



## Neyman-Pearson

### Rejection Region
The region where if x falls within, results in a rejecting the null hypothesis

## The Significance Level
The probability of a test committing a type 1 error (false positive)

## Power Level
When we successfully reject the null when it is not true.
This leads us to the alternate hypothesis.

The P(type 2 error) = $P_{H_a}(T \le c)$
$$
P_{H_a}(Reject\space H_0) = P_{H_a}(T >c) = 1 - P(Type \space 2 \space error)
$$

The probability of a test committing a type 2 error (false negative)
Power = 1-P(type 2 error)


![[Pasted image 20261110181148.png]]


## Wald Statistics

### T-statistics

## Likelihood Ratio

$$
T=\frac{P_{H_a}(X=x)}{P_{H_0}(X=x)}
$$
The greater T is, the more it favors the alternate hypothesis
The smaller T is, the more it favors the null hypothesis