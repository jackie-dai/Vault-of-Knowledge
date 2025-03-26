
**Appendix**
[[Lecture 1 - Recurrence Relations and Algorithms]]
[[Lecture 2 - Asymptotic Notations]]
[[Lecture 13 - Dynamic Programming III]]
[[Lecture 15 - Linear Programming]]

**Lecture 6 - Directed Graphs**

```
DFS(G)
	boolean array visited[n] <- false 
	for all v
		if visited[v] == false
			Explore(G, v)
```
```
Explore(G, u)
	visited[u] = true

	for v in (u,v) { E
		if visited[v] == false
			Explore(G, v)
```

Back edges - a edge that has already been visited (v, u)
Forward edges - a edge that has already been visited (u, v)
Tree edges - occurs in the recursive tree and first time visit

We want to be able to detect these types of edges in our algorithm

```
DFS(G)
	boolean array visited[n] <- false
	**clock = 1**
	**int array pre[n], post[n]** 
	
	for all v
		if visited[v] == false
			Explore(G, v)
```
```
Explore(G, u)
	visited[u] = true
	**pre[u] = clock**
	**clock += 1**

	for v in (u,v) { E
		if visited[v] == false
			Explore(G, v)
	**post[u] = clock**
	**clock += 1**
```

Now we need to classify these edges using the timers

![[Pasted image 20250213135609.png]]

Notice that: pre[u] < pre[v] < post[v] < post[u]

**Application #2 Topological Sort**

Dependency graph
Some nodes to be visited first before others. Nodes depend on each other

DAG - Directed Acyclic Graph

In a topological sort, you can never have a back edge

Topological Sort Algorithm
1. Run DFS
2. Sort vertices from highest post # to lowest post #


##Application #3: Connected Components

![[Pasted image 20250214055957.png]]

Strongly connected components (SCC)
When vertices u,v have a path from both u -> v and v -> u

Meta-graph
Strongly connected components become one vertex with edges from SCC to other SCCs or single vertices.


# Lecture 9 - Huffman Encoding and MST (Greedy II)


Encoding
Can we save space by encoding data (representing the same data without losing meaning)

Example #1:
Binary encoding
00 -> A
01 -> 01

Lossy encoding
000 -> AB or BA, not clear which one

![[Pasted image 20250221133617.png]]

Trees and prefix codes are directly related
![[Pasted image 20250221133802.png]]left = 0
right right left -> 110

Cost of a prefix-code/tree
```
Cost(tree)
```

What makes a optimal tree?
- Full binary trees
	- Every non-leaf node has two children

- Placing more frequent letters higher on the tree
	- allows for quicker access


# Lecture ?: Dynamic Programming

Memo-ization
Caching computations we previously computed

Memoized fibonacci 
```
memo = [0, 1, None, None, ..., None]
```

What are the elements of dynamic programming
- Breaking problems into subproblems.
- Overlapping subproblems means we can save resources by storing the computation once and reusing it when needed

Two ways to do Dynamic Programming
- Top-down
- Bottom-up