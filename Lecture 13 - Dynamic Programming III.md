
Traveling Salesperson Problem (TSP)

Definition of a Tour
1) starts from city 1
2) visits every city exactly once
3) returns to city 1

Naive bruteforce algorithm
- (n-1)! tours
- each O(n) to compute distance
- Total runtime: o(n!)

Dynamic program algorithm runtime: O(n^2 * 2^n)
