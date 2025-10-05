
## Transition matrix

## Irreducibility
 i -> j indicates there is a path from state i to state j
 
i communicates with j if  i->j and j->i 

If all chains communicate with each other, then the chain is irreducible.
## Aperiodicity
Periodicity is the return time for i

*In a irreducible chain, all states have the same period.*

An aperiodic chain is one in which return times are not multiples of some d > 1.


### Long Run Behavior

### Balance

$$
	\pi(k) * P(k, j)
$$
= the proportion of k moving to j

Balance is defined as the proportion leaving j equals the proportion entering j.


$$
\pi=\pi*P
$$
where P = transition matrix

and

$$
\pi=[\pi(1),\pi(2),...,\pi(n)]
$$
$\pi$ = 1

The detailed balance equations might not have a solution. But if they do, then it is the stationary distribution of the chain

For all irreducible birth and death chains,
![[Pasted image 20251005123550.png]]
after finding the stationary probability for one, we can find the rest with this equation

We can only apply this if the chain is irreducible AND birth and death chain

irreducible: all states communicate with each other
birth and death rate: transitions are only between neighbors (state 4 can't go to state 1)
### Metropolis - Hastings Algorithm

Goal: design a procedure for sampling from any distribution, without enumerating P, only knowing pi up to some scaling constant

Idea: Start with some x_o to update it by proposing some "small" change, check whether our proposal is an improvement or not


Algorithm:
1. for i = 0, 1, 2, ...
	1. current x_i
	2. given x_i,  draw a proposal Y ~ Q(x_i, :)
	3. decide whether to accept or reject
		1. if score(Y) >- score(X_i)
			1. then accept X_i+1 = Y
		2. if score(Y) < score(X_i)
			1. compute acceptance ratio
				1. r(x_i,y) = score(Y) / score(X_i)
			2. accept the step with probability = r(X_i->Y), reject otherwise


