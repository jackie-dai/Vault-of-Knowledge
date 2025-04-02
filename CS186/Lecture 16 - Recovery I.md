
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
-

Flush(A) = write from memory A to disk A

**Page Log Sequence Number (LSN)**

