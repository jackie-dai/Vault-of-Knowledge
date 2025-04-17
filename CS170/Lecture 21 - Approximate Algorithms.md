
**Suppose you show your problem P is NP-hard. How do you solve the NP-hard problem?**
- Learn more about the inputs
- Heuristics
	A example of a heuristic algorithm is the Simplex Algorithm
- Approximation algorithm
	- Min-TSP problem


Def: for a minimization problem P. an algorithm A is an $\alpha$-approximation algorithm  if for all instances I of P A(I) <= $\alpha$

#### Vertex Cover
def: vertex cover is a set of vertices such that each edge is incident to one of them

NP-hard problem

Algorithm #1
1. Compute a maximal matching M in G
Def: