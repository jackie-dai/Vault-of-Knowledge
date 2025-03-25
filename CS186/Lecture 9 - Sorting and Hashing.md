
Where we are at in DBMS Architecture
![[Pasted image 20250325120005.png]]

Single-pass Streaming
- Read a chunk from INPUT to Input Buffer
- Write f(x) for each item to an Output Buffer
- When input buffer is consumed, read another chunk
- When output buffer fills -> write to OUTPUT

*It's okay if there is leftover data in Output Buffer*


Double buffering
Main thread: runs f(x) on pair of I/O buffers
Second thread: drains/fills unused I/O buffers in parallel

Sorting: 2-way

![[Pasted image 20250325121936.png]]

Each input buffer is individually sorted. Take the min of 

