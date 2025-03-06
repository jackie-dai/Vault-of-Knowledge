
## Knapsack Algorithm


## Traveling Salesperson Problem (TSP)

Definition of a Tour
1) starts from city 1
2) visits every city exactly once
3) returns to city 1

Naive bruteforce algorithm
- (n-1)! tours
- each O(n) to compute distance
- Total runtime: o(n!)

Dynamic program algorithm runtime: O(n^2 * 2^n)

How to design a DP algorithm for TSP

Step 1: Subproblems of TSP
Input: cities 1...n
output: A tour of minimum total distance

Think of the subproblem as a partial tour
Start from city 1 and end in city j (passing through all cities in set S)


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.3.6 - 15.11pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```


Step 2: Recurrence Relation for TSP

Recurrence relation: we don't know which icty i is the 2nd to last
Solution: Take the minimum over all i such that i != j (what does this mean)

Base cases and final solution

Base cases: 
- T[{1}, 1] = 0 (graph is itself)
- T[S, 1] = inf (rules out size 2 graphs to prevent cycles)
