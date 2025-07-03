---
Clear Concept: true
tags:
  - javascript
  - basic
  - huge
aliases:
  - Fixed Values
  - Variable Values
  - Literals
Created At: 2025-07-02T17:47:00
---


The JavaScript syntax defines two types of values:
1. Fixed values
2. Variable values

> [!NOTE]
> Fixed values are called **Literals**.
> Variable values are called **Variables**.

#### Javascript Literals
There are 8 main types of literals in JS.
1. Numeric
	>Represent integer or floating-point numbers:
	
	>[!Example] 
	>```js
	>10.50  // with decimal
	>1001 // without decimal
	>```

2. String
	>Represent sequences of character
	
	>[!Example]
	>```js
	>'Sanin' // enclosed with (') single quotes
	>"Sakin" // enclosed with (") double quotes
	>`Tahera` // enclosed with (`) template literals
	>```
3. Boolean
	>Represent only truth or false
	
	>[!Example]
	>```js
	>true    false
	>```
4. Array
	>Represent ordered collections of values and enclosed in square brackets (`[]`)
	
	>[!Example]
	>```js
	>[ 1, 2.3, 'one', "two", true ]
	>```
5. Object
	>Represent collections of key-value pairs and enclosed in curly braces (`{}`)
	
	>[!Example]
	>```js
	>{ name: 'Alice', age: 30 }
	>```
6. Regular Expression #hard #important
	>Represent patterns used for matching character combinations in strings and enclosed between forward slashes (`/pattern/flags`)
	
	>[!Example]
	>```js
	>/sanin/g // it will select 'sanin' globally
	>```
	
	>[!Tip]
	> Regular Expression is a vast topic to discuss. But, to understand javascript and execute operation with string, it's important.
7. Null
	>Represents the intentional absence of any object value
	
	>[!Example]
	>```js
	>null
	>```
8. Undefined
	>Represents a variable that has been declared but not yet assigned a value, or a non-existent property
	
	>[!Example]
	>```js
	>undefined
	>```

#### Javascript Variables
Just like math, **variables** are used to **store** data values in also programming languages.
> JavaScript uses the keywords `var`, `let` and `const` to **declare** variables.

> [!Example] 
> ```js
> var x = 1
> let y = 5
> const pi = 3.1416
> ```
