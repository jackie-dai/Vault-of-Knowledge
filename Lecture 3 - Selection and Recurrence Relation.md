
Select(S,1) - select min
Select(S, n) - select max
Select(S, n/2) - select median

Select(S,1) Algorithm
- Run through list and compare to current min 
- . O(n) runtime

Select(S, 2) Algorithm 
- Run select(s, 1) once to find min. Remove the min
- Run select(s, 1) to find second minimum