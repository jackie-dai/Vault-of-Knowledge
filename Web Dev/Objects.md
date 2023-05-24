
**Object Declaration**
let student = {
	name: "John";
	age: 6;
	cool: false;
}

Short-hand
function makeStudent(name,  age) {
	return {
		name,
		age,
	}
}

Iterating Over Properties
for (let key in student) {
	console.log(key + ": "student[key])
}

Computed Properties 

let fruit = prompt("What fruit would you like to store?");

let basket = {
	[fruit + "s"] : 5
}




**Exercises**
![[Pasted image 20230524111416.png]]

```
let user = {};
user.name = "John";
user.surname = "Smith";
user.name = "Pete";
delete user.name;
```


![[Pasted image 20230524111834.png]]

```
function isEmpty(obj) {
	for (let key in obj) {
	return false;
	}
	return true;
}
```