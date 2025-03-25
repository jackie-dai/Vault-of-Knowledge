
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

![[Pasted image 20250324121818.png]]

**DB File Structures**
Now how do we organize these DB file files?

Unordered heapfiles: Collection of records in no particular order

Heap files as lists
Two doubly linked lists
![[Pasted image 20250324124958.png]]
Header page has two pointers:
- first page of data
- first page of free space
Cons: difficult to find page with enough space (doesn't store how much free space each page has)

Page Directory
![[Pasted image 20250324125250.png]]


