
## Concurrent Threads
Threads are non-deterministic
- can run in any order

### Race Conditions
If threads are accessing the same memory, variables could be different values each time it is run.

We can prevent this from happening by using **locks**.

### Locks
Not the fastest parallezation but its corre
- Lock.acquire()
- Lock.release()
