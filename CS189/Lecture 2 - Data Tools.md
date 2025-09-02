
Pandas is widely used 

**Series**: one dimensional labeled array
components:
- values: actual data
- Index: labels associated with each data value
Properties:
- value_counts(): counts the num of ocurrences of each unique value in a series
- unique(): returns array of every unique element in series
 
**Dataframe**: collection of series
- shares the same index across series
You can create a dataframe from
- CSV file
- dictionary
- series
Properties
- shape(): number of rows and cols of df
- size(): total number of elements in df
- sample(n): randomly sample n rows
	- sample(n=#, random_state=42)
		- for reproducibility


**iloc**
arguments: 
- a list
- a slice
- a single value






