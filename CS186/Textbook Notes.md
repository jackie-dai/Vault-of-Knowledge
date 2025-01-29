Appendix
Lecture 1 - SQL


Lecture 1 - SQL

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




Lecture 2 - SQL II

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

1. FROM <single table> which table are we drawing from
2. WHERE only keeps rows where <predicate> is satisfied
3. GROUP BY <column list>
4. HAVING only keeps groups having <predicate> satisfied (can only be used after group by)
5. SELECT [DISTINCT] <col exp. list>
6. ORDER BY <column list>
7. LIMIT <integer>

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


Lecture 3 - 

**Fixed Length Records**
How do we add and delete records
To add 
- Append
To delete
- Pop, shift, and update
	- if we remove the last item, no need to update

**Variable Length Records**

Each record stores length and pointer