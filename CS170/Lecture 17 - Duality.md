
Weak duality: all feasible solutions *x* to primal LP <= all feasible solutions *y* to dual LP

### Bipartite Perfect Matching
Input: Graph G=(L, R, E) 
- L = left
- R = right
Output: A perfect matching from L to R

Theorem: G has a perfect matching if Max-flow(G') = n

Case 1: (perfect match => max-flow):
1. Let M be a perfect matching in G
2. Put 1 unit of flow on every edge in M and every s->r edge and every l->t edge
3. Then this is a flow of size n
*Because G' is a perfect match, no flows overlap. This proves flow is at least n*

Case 2 (max-flow => perfect match):
1. Let f be an integral flow of size n in G'
	1. Integral flow = all flow values are 0 or 1
2. 