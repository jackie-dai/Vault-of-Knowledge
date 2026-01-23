
## Thread
- describes program state
has its own program counter, registers, execution flags, stack, and memory

*Threads use shared memory*

Threads are like multiple cores.

So we need a TCB
Thread Control Block (TCB)
- holds contents of registers when thread not run

Address pace
- set of memory addresses

process
- one or more threads

Dual mode operation
- only the system has the ability to access certain resources
- combined with translation, isolates programs from each other and the OS from programs