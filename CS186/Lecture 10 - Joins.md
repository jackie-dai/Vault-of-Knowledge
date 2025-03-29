
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


Page Nested Loop Join
```
forach rpage in R:
	foreach spage in S:
		foreach record r in R:
			foreach record s in S:
```

Block Nested Loop Join (BNLJ)

![[Pasted image 20250326101801.png]]
Compare all records in each *chunk* of R to all records for each page of S.

```
for each rchunk of B-2 pages of R:
	for each spage of S:
		for all matching tuples in spage and rchunk:
			add<rtuple, stuple> to result in buffer
```

*Difference: modifying the outermost loop to loop through chunks instead of pages*

**Grace Hash Join**
*Divide:*
Partition tuples from R and S by join key to store on disk.
- Each partition has the same keys or hash value
```
for each page in {R,S}:
	read page into input buffer
	for each tuple on page
		place tuple in output buffer that corresponds to their hash value
		if the output buffer is full -> flush to disk		
```

*Conquer:*

**Sort Merge Join (SMJ)**
First sort both files by the key we are joining on

Compare L1 to R1 
- If match -> right.mark()
- keep iterating the right side until we don't have a match. Once there is a mismatch -> right.reset()
- next call next on leftside and next on right side


Sorting 
- Good if input is already sorted or you need a sorted output table

Hashing
- Con: prone to key skew
- Good for large inputs