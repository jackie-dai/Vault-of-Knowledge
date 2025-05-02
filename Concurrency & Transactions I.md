
Why is concurrent execution important?
	I want to run instructions in parallel while avoiding any conflicts

Advantages of concurrency
- faster latency
- faster throughput (queries per second)

### Transaction
A sequence of multiple actions to be executed as an atomic unit

### ACID
Atomcity: All actions in the txn happen, or don't

Consistency: if the DB starts out consistent, it ends up consistent at the end of the txn

Isolation: Execution of each txn is isolated from that of others
	how do we interweave transactions properly?

Durability: if txn commits, its effects persist

