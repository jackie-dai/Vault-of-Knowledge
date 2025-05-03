In order to ensure serialized schedules, transactions need to acquire locks to read and write data. 

Types of locks
- Shared lock S (for reading)
- Exclusive lock X (for writing)

Only one transaction can have a exclusive lock per resource while many transactions can share a lock.

**REMINDER: a schedule is non-conflict serializable if there is a cycle in its dependency graph**

How to enforce conflict serializability with locks

![[Pasted image 20250503104138.png]]

1. T1 Locks A and reads/write
2. T2 tries to 

### Two Phase Locking (2PL)
*All lock requests must precede unlock requests* 
L -> U 

You cant lock after you've unlocked
L->U->L


