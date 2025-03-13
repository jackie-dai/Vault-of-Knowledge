
Why do we ignore smaller values?
- Constants depend on the platform and computer
- Easier to compare the performance of algorithms on large inputs


T(n) is O(g(n)) if and only if there exists a constant c and n_0
such that all n is greater than n_0, T(n) is upper bounded by c * g(n)

**How to prove T(n) is O(g(n))**
Give a constant c and constant n_0, such that all n > n_0 
$$
T(n) <= c * g(n)
$$

![[Pasted image 20250308121137.png]]
*For all n > n_0 (to the right of n_0)  c * g(n) is larger than T(n)*

**Disclaimer: Don't trust pictures!**

dx T(n) <= dx g(n)
Check if the inequality still holds


Recurrence relations are closely related to trees
![[Pasted image 20250308123815.png]]




```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.3.13 - 13.43pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
