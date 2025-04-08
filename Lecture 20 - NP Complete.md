
Minimum spanning trees O((n + m) log(n))
All pairs shortest paths O(n^3)

Def: A problem is efficiently solvable if it can be solved inn polynomial time O(n^k)

Preferably practical algorithms should be linear or nlog(n)

**What is P?**
Def P: "Complexity class" if all problems which are efficiently solvable

**What is NP?**
Def NP: class of problems whose solutions can be verified efficiently

Example problem: 3-coloring

Input: Graph G = (V,E)
Def coloring c: V -> {Red, ,Green, Blue} s.t each edge receives two different colors

Verification: for every edge, check if c(u) != c(v)

Possible algorithm: 

Example problem: Factorization
Input: n-bit number N
p, q  .1 S.T. p * q = N

Algorithm: 
1. Try dividing N by every 1 < p  N

Factorization is NP

Proof:
verify(Input N, Solution p and q)
- check p,q > 1
- Check p * q = N <- O(n^2) time or better

**Example problem: Rudrata Cycle (Hamiltonian cycle)**
