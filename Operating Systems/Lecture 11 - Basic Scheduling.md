
## First-come-first-out (FCFO)
![[Pasted image 20260331112828.png]]
Waiting time:
Completion time: 

## Round-Robin Scheduling (RR)
Quantum time *q*
Each n process gets 1/n burst time that does not exceed *q*

*Give each thread a small amount of CPU time when it executes, cycle between all ready threads*
Pros: better for short jobs

## Comparing RR and FIFO
![[Pasted image 20260331113431.png]]

## Strict Priority Scheduling
Assign priorities to jobs and execute jobs in order of priority

Problem
- Starvation: lower priority jobs never run because of high priority jobs


We need to implement **scheduling fairness**

Shortest job first (SJF)
- In order of least amount to time to complete
Shortest remaining time first (SRTF)
- least amount of remaining time to finish computation

Work-conserving scheduler: does not leave the CPU idle when there is work to do

## Priority Inversion
