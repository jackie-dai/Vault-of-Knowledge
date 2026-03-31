
Atomic Operation: a operation that always runs to completion or not at all

For example, *loads* and *stores* are atomic operations, while increment and decrement are not. This is because loading and storing is one assembly instruction while incrementing takes multiple operations.

We need to create more atomic operations in order to implement a thread safe lock

![[Pasted image 20260331060354.png]]
*Lock simulation in the kernel*
- Disable interrupts
- Check value
	- if value == 0 => no one has lock so proceed
	- if value == 1 => someone has lock so put on wait-queue
- Release after done