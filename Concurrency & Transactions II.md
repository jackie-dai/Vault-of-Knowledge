In order to ensure serialized schedules, transactions need to acquire locks to read and write data. 

Types of locks
- Shared lock S (for reading)
- Exclusive lock X (for writing)

Only one transaction can have a exclusive lock per resource while many transactions can share a lock.