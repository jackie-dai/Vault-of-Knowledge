
Background
![[Pasted image 20250408104922.png]]

How do we optimize the transportation from sources to destinations

Max flow algorithm
**Inputs:**
- Directed graph
- One source vertex
- One destination vertex
- Each edge can only had *capacity* amount of water
**Goal:** Route the max amount of water from source to destination

We can break up the flow of water to 1/2 and reconvene at later point to make 1 unit of water

Def *flow*: A *flow* assigns a number f to each directed edge (this is the amount of flow of water through a edge)
- Nonegative
- f <= capacity
Def *size*: The size of a flow in the total quantity sent from s -> t
This is equal to the sum of all the flows

Objective: maximize size(f)

![[Pasted image 20250408114558.png]]

We can create a residual graph by "undoing" the flow (backtracking the flow).
![[Pasted image 20250408153802.png]]
1. Add original flow
2. Add residual flow
3. Cancel out overlapping flows

Ford-Fulkerson Algorithm
1. Find a path P from s to t in the resdiual graph (augmenting path)
2. Send more flow along P
3. Repeat

![[Pasted image 20250408154454.png]]
 ![[Pasted image 20250408154508.png]]

Def Residual: ![[Pasted image 20250410101844.png]]
Example: ![[Pasted image 20250410101945.png]]