
When we talk about runtime, we always talk about worst case. In other classes, you will learn about average cases.

In asymptotics, we only care about the behavior of large 
- ignore constants and focus on the largest dependence on n.

O(n) - "order of n"

How fast is grade school integer multiplcation?
=> O(n^2) + O(n) => O(n^2)
- we ignore lower dependences of n

Can we do better than O(n) for addition?
=> No, it takes at least n steps to just read the numbers

Can we do better than O(n^2) for multiplication?
=> Egyptian multiplication


![[Pasted image 20250204183914.png]]

Not actually faster!

There are ways to do better for multiplication:
- Karatsuba: O(n^1.6)
- Toom-3/Toom-Cook: O(n^1.465)
- Harvey and van der Hoeven: O(nlog(n))
