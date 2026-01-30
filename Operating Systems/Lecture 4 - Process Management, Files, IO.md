
## Concurrent Threads
Threads are non-deterministic
- can run in any order

### Race Conditions
If threads are accessing the same memory, variables could be different values each time it is run.

We can prevent this from happening by using **locks**.

### Locks
Not the fastest parallezation but its correct and works
- Lock.acquire()
- Lock.release()
![[Pasted image 20260129155840.png]]


## Safe Kernel Mode Transfers
- Atomically transfer  to well defined entry pointers while entering kernel mode

Separate kernel stacks!
Each threads has both user stack and kernel stack 