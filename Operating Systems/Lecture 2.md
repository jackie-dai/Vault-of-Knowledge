
## Threads
- describes program state
- has its own program counter, registers, execution flags, stack, and memory

*Threads use shared memory*

Threads are like multiple cores.

So we need a TCB
Thread Control Block (TCB)
- holds contents of registers when thread not running
- TCB are stored in the kernel

** Read through thread.h and thread.c in hw0 if interested in threads
**
## Address Space
- set of memory addresses
- high addresses on top and low addresses on bottom
Threads run in address spaces

## Process
Execution environment with restricted rights
- Runs one or more threads


## Dual mode operation
Hardware provides at least two modes
1. Kernel Mode
2. User Mode

- only the system has the ability to access certain resources
- combined with translation, isolates programs from each other and the OS from programs
