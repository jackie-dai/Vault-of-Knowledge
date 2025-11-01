
## **Order Statistic of Uniform IID (0, 1) Variables**
![[Pasted image 20251031003745.png]]

We don't know what the value of U_i is but we can see U_1 < U_2.  This is the called the order statistic. 

How can we find the joint density of two order statistics

![[Pasted image 20251031003947.png]]

## Finding the density for U_k

![[Pasted image 20251031004442.png]]
We can use the multinomial distribution for this:
$$
P(U_k \space \epsilon \space dx) = \frac{n!}{(k-1)! 1! (n-k)!} x^{k-1} \space dx \space (1-x)^{n-k}
$$
Density of U_k is given by 
$$
f(x) = \frac{n!}{(k-1)!(n-k)!} x^{k-1} (1-x)^{n-k}, \space 0 < x < 1
$$


## Beta Density
$$
f(x) = \frac{(r+s-1)!}{(r-1)!(s-1)!}x^{r-1}(1-x)^{s-1}, \space 0<x<1
$$