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
- Group by

Conceptual order of SQL evaluation

5. SELECT [DISTINCT] <col exp. list>
1. FROM <single table>
2. WHERE <predicate>
3. GROUP BY <column list>
4. HAVING <predicate>
6. ORDER BY <column list>
7. LIMIT <integer>

Inner and Natural Joins

Default = INNER JOIN
- Cross product

Natural Join
- 