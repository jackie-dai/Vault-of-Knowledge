
Course notes
https://www.eecs70.org/assets/pdf/notes/n14.pdf

Montonocity Prop
$A \subset B \Rightarrow \mathbb{P}(A) \le \mathbb{P}(B)$


Conditional Probability 
$\mathbb{P}[A | B] = \frac{\mathbb{A \cup B}, \mathbb{B}$

Total Probability 
$P(B) = P(B | A)P(A) + P(B | \bar{A})P(\bar{A})$

Bayes Rule
$$
P(A|B) = \frac{P(B|A)P(A)}{{(B)}}
$$
Used for problems to calculate probablity of event B given you don't know which initial event happend first (A or $\bar{A}$)

Typically, numerator is given and must find denominator using total probability rule

Independence
$\mathbb{P}(A | B) = A$
derrivation -
$$
	P(A|B) = \frac{P(A \cup B)}{ P(B)}
	=\frac{P(A)P(B)}{P(B)}
	= P(A)
$$

Independence != Disjoint 

Disjoint = Mutual Exclusive
