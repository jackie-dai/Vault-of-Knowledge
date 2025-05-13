
*Whether we allow modified pages to be flushed to disk BEFORE commit*

No steal:  

Steal: allows uncommited changes to end up on disk to maintain atomcity

*Whether or no modified pages from a transaction are forced to disk or not. This is decided at flushing to disk ON commit*

Force: 

No force: doesn't guarantee changes are flushed to disk on commit

![[Pasted image 20250401172336.png]]
ARIES uses steal, no force

Logging
- Before a transaction is committed, all logs must be written to disk first
- Log changes before changes are made

Write Ahead Logging (WAL)
1. Force the log record for an update before the corresponding datapage gets written to disk
2. Force all log records for a Xact before commit

In order to write to memory we need to satisfy:
	pageLSN <= flushedLSN
This guarantees all updates are before we flushed

Flush(A) = write from memory A to disk A

![[Pasted image 20250401173444.png]]
*Operation can either be COMMIT or ABORT*
*Whenever there is a WRITE(X), we undo log the value that X changed to*

UNDO: undoes all updates for *running* transactions
REDO: logging redoes all updates for *committed* transactions

ARIES Recovery System

Data structures
- The Log (WAL)
- FlushedLSN

![[Pasted image 20250513134621.png]]

Start from last checkpoint
Recovery phases
1. Analysis: recreate transaction table at time of crash
2. Redo: all actions (reconstruct state of the DB before crash)
3. Undo effects of failed transactions

Analysis
recreate xact table

Scan log forward from checkpoint
if End => 
- remove xact from xact table
elif Update =>
- if page P not in dirty tab, add to DPT
elif End => 
- add xact to xact table,
- set lastLSN=LSN
- change xact status to commit or abort

TODO
- Worksheet problem 2A
Put on cheatsheet
![[Pasted image 20250401180220.png]]

**Page Log Sequence Number (LSN)**

