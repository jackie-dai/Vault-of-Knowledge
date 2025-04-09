
Inter query
parallelizing with multiple queries

Intra query
Parallelizing within a single query

**Partitioning Schemes**
Network cost: cost to send data
Units: KB

Range partitioning: 
divides data based on the range of key

Calculating network cost:
1. Number of tuples that each machine gets (number of keys in each range)
2. M-1
3. N/M x M-1

Hash partitioning: hashing keys into n partitions

Round robin partitioning: iterates through data and sorts into partitions

Advantage of organizing by keys
- Can easily access the key by either hashing and taking the range
Disadvantage
- Overhead for insertions and deletion

**Parallel Sorting**
1. Partition the data over machines with range partitioning
2. Perform external sorting on each machine independently (each machine holds a different range of data)

**Parallel Sort Merge Join**

**Parallel Hashing**
