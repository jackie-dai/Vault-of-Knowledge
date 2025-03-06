Appendix
Lecture 1 - SQL
[[Lecture 11 - Iterators and Relational Algebra]]


# Lecture 1 - SQL

Relational database
- Columns (attributes)
- Records (tuples)
- Cardinality (# of records)
- Flat (no nested tables)

Primary key
- Can be greater than 1 column
- Must be unique

Foreign key
- reference to key in different table

![[Pasted image 20250126123210.png]]




# Lecture 2 - SQL II

Types of operations
- Aggregate
	- When we group by we have to call an aggregate function (i.e. SUM, MIN, MAX, etc..) to determine which row/value to return per group
- Group by

valid 

'''
SELECT age
FROM students
GROUP BY major, age
'''


Conceptual order of SQL evaluation

```
1.FROM <single table> which table are we drawing from
1. WHERE only keeps rows where <predicate> is satisfied
2. GROUP BY <column list>
3. HAVING only keeps groups having <predicate> satisfied (can only be used after group by)
4. SELECT [DISTINCT] <col exp. list>
5. ORDER BY <column list>
6. LIMIT <integer>
```



Inner and Natural Joins
https://docs.google.com/presentation/d/1G_K2BImiDLMXYf-JHXzU6Yyo5Gzv4dO6/edit#slide=id.p34

![[Pasted image 20250128174051.png]]

Default = INNER JOIN
- Cross product
- intersection 

Natural Join
- Only retains rows with common columns

Left Outer Join
- Returns all matches and rows from the left side
RIght Outer Join
- Returns all matches rows, and preserves all unnmatched rows from the table on the right of the clause
Full Outer Jin
- Returns all (matched or unmatched0 rows from the tables on both sides of the join clause)

Null values
Problematic 

Find new boolean logic to incorporate nulls

![[Pasted image 20250128165244.png]]



**Fixed Length Records**
How do we add and delete records
To add 
- Append
To delete
- Pop, shift, and update
	- if we remove the last item, no need to update

**Variable Length Records**

Each record stores length and pointer

Discussion 2 - Disks, files, and buffers

Fixed Length Records
	- Each record/row is a constant size
Variable Length Records
	- Lengths are stored in header
	- Why do we point to the end of the field instead of the beginning
		- Easier to calculate length 
		- Aside: not sufficient for storing nulls
![[Pasted image 20250204172016.png]]

Page Header
The page header is a portion of the page reserved to define the header
- stored at the end of the page to allow for growth

Fragmentation
Problem with space. We can't store 4 byte file if the 4 bytes are fragemented.
- only a problem with unpacked layout

Reading and writing takes two I/Os

File Types
There are two types of heap file implementations
- Linked List
![[Pasted image 20250210174622.png]]
- Page Directory
![[Pasted image 20250210174632.png]]
Generally page directory has faster insertion time than linked list because we only need to read the header pages

However, this means search for a record is not efficient because it is unordered. 


Packed and unpacked pages for FLR
A packed page means there are no gaps between records.
	- A benefit of this is we can easily compute the next avaliable slot by: # of records * length of each record
A unpacked page reserves slots for records
	- Page headers will contain bitmaps that keep track of which slots are full or empty

![[Pasted image 20250222234934.png]]


# Lecture 5 - 

Indexes
An index is a data structure that enables fast lookup and and modification of data entries by search key



```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.3.5 - 21.24pm (2).drawing",
	"width": 500,
	"aspectRatio": 1
}
```


This is a b+ tree

okay today we will be covering minimum spannin trees


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.3.5 - 21.28pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```


okay that is all for today.

It it too late for that.

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.3.5 - 21.33pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
