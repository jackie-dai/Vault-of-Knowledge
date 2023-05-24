
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


Computed Properties 

let fruit = prompt("What fruit would you like to store?");

let basket = {
	[fruit + "s"] : 5
}


