
Inter query
parallelizing with multiple queries

Intra query
Parallelizing within a single query

**Partitioning Schemes**
Network cost: cost to send data
Units: KB

Range partitioning: divides data based on the range of key

Hash partitioning: hashing keys into n partitions

Round robin partitioning: iterates through data and sorts into partitions

Advantage of organizing by keys
- Can easily access the key by either hashing and taking the range
Disadvantage
- Overhead for insertions and deletion
