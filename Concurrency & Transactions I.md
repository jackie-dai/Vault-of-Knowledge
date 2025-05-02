
Why is concurrent execution important?
	I want to run instructions in parallel while avoiding any conflicts

Advantages of concurrency
- faster latency
- faster throughput (queries per second)

### Transaction
A sequence of multiple actions to be executed as an atomic unit

### ACID
Atomcity: All actions in the txn happen, or don't
	If there is an abort in the middle of the transaction, nothing is changed
Consistency: if the DB starts out consistent, it ends up consistent at the end of the txn
	
Isolation: Execution of each txn is isolated from that of others
	how do we interleave transactions properly?

Durability: if txn commits, its effects persist
	if we know there was a transaction, the effects of the txn remains until change

### Serial Schedule
each txn runs from start to finihs without any interfering actions
complete isolation

We need to design a schedule that have the same net effect as serial schedule (mimics isolation) but interleaves transactions

#### Conflicting Operations
Two operations conflict if 
- different txn
- are on the same object
- at least one of them is a write

*The order of non-conflicting operation has no effect on the final state of the database*

Def: Schedule S is conflict serializeable if:
- S is conflict equivalent to some serial schedule
- which implies that S is also Serializable 