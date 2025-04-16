

### SAT
#### 2-SAT

#### Search-TSP


### Reduction
Reduce problem A down to smaller problem B to solve problem A

Instance I from problem A -> reduce -> Instance I from problem B  (we know how to solve problem B) -> solve -> solution to I problem B -> recovery -> solution to I (problem A)

Example: reduce rudrata pat to rudrata cycle
	 

### Types of Complexity Classes

P: Problem that can be solve in polynomial time
NP: problem in which a solution can be reduced in polynomial time
NP-complete: problem in NP which all problems in NP can reduce to 
NP-hard: problem that is at least as hard as an NP-complete problem

*At least as hard represent how hard it is to solve a problem efficiently it doesn't mean the runt time is greater*

When does P=NP?
- if an NP complete problem can be solved in polynomial time
- if you can reduce an NP complete problem to a P problem

