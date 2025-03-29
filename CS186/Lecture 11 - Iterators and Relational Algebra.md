
Iterator
```
abstract class iterator {
	void setup(List<Iterator> inputs);
	void init(args);
	tuple next();
	void close();
}
```

Perform relational operators on iterators and output a (modified) iterator

**Operators**

beta
Projection - $$\pi$$
select a set of a table  
- removes duplicates
Sets and multisets

Selection() - lower sigma
equivalent to where

Union

Set difference

Joins

Notation
[R] = # of pages
p_R = # of records per page in R
|R| = number of total records in R 
	- this is the cardinality of R
	- |R|  = p_R * [R]



Simple nested loop join (SNLJ)

Page oriented nested loop join 

Block Nested Loop Join (BNLK)

Index Nested Loop Join (INLJ)

**Merges**

Sort-Merge Join


B+ tree
