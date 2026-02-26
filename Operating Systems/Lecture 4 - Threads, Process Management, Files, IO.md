
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
- Atomically transfer  t well defined entry pointers while entering kernel mode

**Atomic**: executed in a instant

Separate kernel stacks!
Each threads has both user stack and kernel stack 
![[Pasted image 20260225235013.png]]
*three states of a thread. doesn't use kernel stack while thread is running*

So before a interrupt or exception, registers point at user stack, but after a interrupt it points at the kernel stack
![[Pasted image 20260225235323.png]]

![[Pasted image 20260129162739.png]]