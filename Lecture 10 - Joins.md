
Cost Notation
[R] : The number of pages to store R
p_R : The number of records per page of R
|R|: The cardinality (number of records) of R
	- |R| = [R] * p_R


Simple Nested Loops (SNLJ)
```
foreach record r in R do:
	foreach record s in S do:
		add (r,s) to buffer
```
Cost: [R] + |R|*|S|