


Def $\omega$ : outcome of one random trial, **element of the outcome space $\Omega$**
Def $\Omega$ : outcome space, contains all possible outcomes $\omega$
Def event: **subset of the outcome space** $\Omega$


## Third Axiom: Addition Rule
We can add *n* mutually exclusive or disjoint events 

It is a bit more complicated if the events are disjoint


### Multiplication Rule

To find the intersection of two events, we need to find the outcomes that lie in the intersection. 

![[Pasted image 20250912104017.png]]
*Inherently, we are using the division rule, but because we only dividing by one (the entire outcome space), the calculation just becomes P(A and B)*

**Drawing without replacement**
We have three cards (1 red, 1 blue, 1 green)

Drawing two cards w/o replacement, what is the probability we 1st draw = red and 2nd draw=blue {RB}

To find the probability that both events occur we first find the probability of the first event draw 1 = red

$$
P(\texttt{R on first draw}) = \frac{n\texttt{um of favorable outcomes}} {\texttt{total num of outcomes}} = \frac{2}{6} = \frac{1}{3}
$$

$$
P(\texttt{B on second draw | R on first draw}) = \frac{n\texttt{num of favorable outcomes}} {\texttt{total num of outcomes}} = \frac{1}{2}
$$
$$
P(\texttt{RB}) = \frac{1}{3} * \frac{1}{2} = \frac{1}{6}
$$
### Conditional Probability
P(B | A) ~ the probability that B happens given that A happened

The notable difference between conditional probability and intersections P(A and B) is that the possible outcome space of the conditional probability becomes shrunken

![[Pasted image 20250912104003.png]]\

The **division rule** of dividing by the subset of the outcome space we've been **constrained to given the conditional**.