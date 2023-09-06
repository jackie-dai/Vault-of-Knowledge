
int x = 18
&x - address of x
*p = pointer of x



```
void addOne(int x)
{
	x = x + 1;
}

int y = 3;
addOne(y)
```
Won't work

```
void addOne(int *p)
{
	*p = *p + 1;
}

int y = 3;
addOne(&y);
```
Will update with pointers