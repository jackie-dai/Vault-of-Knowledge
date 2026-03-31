

## First-in-first-out (FIFO)
![[Pasted image 20260331112828.png]]
Waiting time:
Completion time: 

## Round-Robin Scheduling (RR)
Quantum time *q*
Each n process gets 1/n burst time that does not exceed *q*

## Comparing RR and FIFO
![[Pasted image 20260331113431.png]]

## Strict Priority Scheduling
Assign priorities to jobs and execute jobs in order of priority

Problem
- Starvation: lower priority jobs never run because of high priority jobs


We need to implement **scheduling fairness**

Shortest job first (SJF)
Shortest remaining time first (SRTF)