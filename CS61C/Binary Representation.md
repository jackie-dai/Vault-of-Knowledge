
Everything is represented via analog signals

Binary addition  & multiplication 

	1 0 1 0
+ 0 1 0 1
----------
= 1 1 1 1



Hack: Binary shift
11110

01111 = 15
shift to left, multiply by base -> 15 * 2 = 30


Two ways to include negative numbers in binary:
- Two's complement 
	- Left most bit is used as a sign
	- Flip all the bits
	- + 1
- Bias encoding 
	- Unsigned and apply a bias (ex. -15)