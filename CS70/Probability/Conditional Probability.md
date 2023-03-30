
Course notes
https://www.eecs70.org/assets/pdf/notes/n14.pdf

Montonocity Prop
$A \subset B \Rightarrow \mathbb{P}(A) \le \mathbb{P}(B)$


Conditional Probability 
$$\mathbb{P}[A | B] = \frac{\mathbb{P}(A \cap B)} {\mathbb{B}}$$

Total Probability 
$$P(B) = P(B | A)P(A) + P(B | \bar{A})P(\bar{A})$$
Used for problems to calculate probablity of event B given you don't know which initial event happend first (A or $\bar{A}$)

Bayes Rule
$$
P(A|B) = \frac{P(B|A)P(A)}{{(B)}}
$$

Useful for when you want to know P(A | B) when you only know P(B | A)

Typically, numerator is given and must find denominator using total probability rule

Independence
$$\mathbb{P}(A | B) = P(A)$$
derived by
$$
P(A \cap B) = P(A)P(B)
$$
$$
	P(A|B) = \frac{P(A \cap B)}{ P(B)}
	=\frac{P(A)P(B)}{P(B)}
	= P(A)
$$

Independence != Disjoint 

Disjoint = Mutual Exclusive
