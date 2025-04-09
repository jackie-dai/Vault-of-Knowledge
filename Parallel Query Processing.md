
Inter query
parallelizing with multiple queries

Intra query
Parallelizing within a single query

## **Partitioning Schemes**
Network cost: cost to send data
Units: KB

### Range partitioning: 
divides data based on the range of key

Calculating network cost:
1. Number of tuples that each machine gets (number of keys in each range)
2. M-1
3. N/M x M-1

### Hash partitioning: hashing keys into n partitions

### Round robin partitioning: iterates through data and sorts into partitions

Advantage of organizing by keys
- Can easily access the key by either hashing and taking the range
Disadvantage
- Overhead for insertions and deletion
## **Sorting**

### Parallel Sorting
1. Partition the data over machines with range partitioning
2. Perform external sorting on each machine independently (each machine holds a different range of data)

### Parallel Sort Merge Join
*Requires all machines to have the same range partitions*

### Parallel Hashing


### Parallel Hash Joins

### Symmetric Hash Joins
Build two hash tables at the same time

If tuple from R:
	probe hash table for S
	Add tuple into hash table for R
if tuple from S:
	probe hash table for R
	Add tuple into hash table for S
Each match during probing gets joined and outputted

### Parallel Aggregation
We use *hierarchical aggregation* to calculate aggregate functions (SUM, COUNT).

### Asymmetric Shuffles
If relation is already partitioned in the way we want, we don't need to repartition

### Broadcast Joins
Sometimes, one table is tiny and one is huge (unevenly distrbuted)
To save IO cost: broadcast smaller table to each machine rather than trying to partition the biggest table