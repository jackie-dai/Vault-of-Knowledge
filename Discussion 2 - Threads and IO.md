
## Threads
Threads are single unique execution contexts with their own set of registers and stack

Thread
- Stack
- Code
- Registers
Everything is unique except for shared memory

Threads have nondeterministic behavior

If a thread dies and we try to print something from that thread, we will print garbage
*use pthread_join to make sure the thread finishes running before moving on*
## Syscalls
Run and create threads with syscalls

In order to pass in multiple diff types of arguments to a thread, create a struct and pass a pointer to the struct