---
Clear Concept: true
tags:
  - important
  - basic
Created At: 2025-07-06T21:44:00
---
Javascript function is simply a group of statement for doing particular task. 

- [[#Function Declaration]]
	- [[#Function Statement]]
	- [[#Function Expressions]]
	- [[#Arrow Function]]
	- [[#Function Constructor]]
- [[#Function Invocation]]
- [[#Immediately Invoked Function (IIFEs)]]
- [[#Anonymous Function]]

## Function Declaration

### Function Statement
```js
function name(parameter1, parameter2) {
	// Compute tasks
	return value;
}
```


> [!Info] Hoisting
> Function declarations are "hoisted" to the top of their scope. This means you we call them before they are declared in our code


---

### Function Expressions
```js
const name = function (parameter1, parameter2) {
	// Compute tasks
	return value;
}
```

> [!Info] Hoisting
> Unlike function declarations, function expressions are not hoisted. You must define them _before_ you call them

---

### Arrow Function
```js
const name = (parameter1, parameter2) => {
	// Compute tasks
	return value;
}
```


> [!Info] Arrow Function
> Not hoisted
> 
> Cannot be used as constructors. (No support of `new`)

---

### Function Constructor
The **last argument** is the string representing the **body** of the function. 

```js
new Function(arg1, arg2, ..., argN, functionBody)

// With no argument
new Function(functionBody)
```

---

## Anonymous Function
Functions without a name. They are often used as arguments to other functions (callbacks) or in function expressions

```js
setTimeout(function() {
	console.log('hello world')
}, 2000)
```

---

## Immediately Invoked Function (IIFEs)
Functions that are defined and executed immediately. Often used to create a private scope for variables or execute asynchronized tasks.

```js
(function() {
	let name = 'sanin';
	console.log(name);
})()
```

---

## Function Invocation
Invocation is the process of calling the function. We can actually pass the parameter during Invocation.

```js
functionName(parameter1, parameter2)
```

---


### Important Topics
- **Scope :** Functions create their own scope, meaning variables declared inside a function are not accessible from outside it.
- **Closures :** When a function returns a function and it depends on a parent scope memory it stores the data in closure.
	```js
	const add = (function() {
		let count = 0;
		return function() {
			count++;
		}
	}) // as add depends on count it wont kill count
	
	add() // change the count 1
	add() // change the count 2
	add() // change the count 3
	```


> [!Tip] Semicolon
> Semicolons are used to separate executable JavaScript statements.  
Since a function **declaration** is not an executable statement, it is not common to end it with a semicolon.
