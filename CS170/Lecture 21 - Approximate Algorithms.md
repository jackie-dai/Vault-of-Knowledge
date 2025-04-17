
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

Reduce to: 
	Algorithm #1
	Compute a maximal matching M in G
	
	Def: a matching is set of edges w/ no overlapping every verticies
	*A maximal matching means there are no more edges can be added*
	
	Solution: Can compute by adding edges greedily to M

Now the output of all the vertices in the set are part of the vertex cover

Theorem: C is a vertex cover and |C| <= 2 * Optimal size (OPT)

Claim: C is a vertex cover

The best approximation algorithm is LP

	Algorithm #2 LP
		Varaible x_i, for each vertex i 
			Ideally x_i {1, if i is part of vertex cover,
						0, otherwise}
			Constraints: 
				0 <= x_i <= 1
					x_i + x_j >= 1 
			Objective: min sum of x_i
Claim: LP-OPT <= OPT vertex cover
Proof: OPT vertex cover is feasible solution to LP. But also functional solutions



	