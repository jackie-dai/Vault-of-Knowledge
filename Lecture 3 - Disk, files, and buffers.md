
SQL -> parse -> relational algebra graph

Disk space management

Disks
- read from disk to ram
- write from ram to disk
Both api calls are slow!

![[Pasted image 20250324104208.png]]
Big and slow to small and fast

Hard drives 
Similar to reading a vinyl

**Flash (SSD**) drives are organized into random cells. Reading is incredibly fast, but writing is slow
- Read: 4KB ~500MB/sec
- Write: 4KB: ~120MB/sec
Writing is more expensive because it needs to allocate space to write

Disk representation
abstracts into pages. Page is the unit of measurement

Reading from a DB file (collection of pages, each page a collection of records)
Reads: fetch a record by *record id* (pointer to tuple(pageID, location on page))