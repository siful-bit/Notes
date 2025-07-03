---
Clear Concept: true
tags:
  - javascript
  - basic
aliases:
  - Javascript Values
Created At: 2025-07-03T10:03:00
---

Variables are Containers for Storing Data.

### Declaring, Assigning and Identifiers
 declaring and assigning are two terms in javascript variables.
 All JavaScript **variables** must be **identified** with **unique names** and
declared like `(Keyword) (Identifiers) ;`

> [!Example]
> ```js
> let x; // declaring but not assigned yet
> x = 5; // assigned the variable
> const  y = 10; // Both declared and assigned
> ```
> Here `let` and `const` is ***keyword*** and `x` and `y` is ***identifiers***

> [!Info] When Declared But Not Assigned
> Javascript will auto assigned undefined into it
> ```js
> let x = undefined // ;
> ```
> same as writing `let x;`

> [!Warning]
> You can't assign variable before it declared. But ***Hoisting*** is another topic to clear this concept

---

### Variable Declartion
> JavaScript Variables can be declared in 4 ways,
1. [[#Automatically]]
2. [[#Using `var`]]
3. [[#Using `let`]]
4. [[#Using `const`]]
#### Feature Table

| Keyword | Redeclaration | Scope    | Changeable | Hoisted |
| ------- | :-----------: | -------- | :--------: | ------- |
| var     |       ✔       | Function |     ✔      | ✔       |
| let     |       ❌       | Block    |     ✔      | ✔(TDZ)  |
| const   |       ❌       | Block    |     ❌      | ✔(TDZ)  |


---

#### Automatically
Javascript variable is automatically declared when first used. That's why people says it's a weird language. But it isn't a problem rather that is smartness of javascript.

> [!Example]
> ```js
> x = 5
> y = 10
> z = x + y // 15
> ```

> [!Warning] It can create confusion. So we should avoid it.

---

#### Using `var`
-  Can be redeclared

> [!Example] Receclaration
> ```js
> var x = 10
> var x = 5 // No error
> ``` 

 - It is **function scoped (Not Block Scoped)** 

The variable declare by `var` is accessible outside block scope but can't in function scope

> [!Example] Block Scope
> ```js
> var x = 10
> if(true) { var x = 5; }
> console.log(x) // 5
> ``` 

> [!Example] Function Scope
> ```js
> var x = 10
> function Test() {var x = 5}
> console.log(x) // 10
> ```

- `var` is hoisted with assigning undefined in it

> [!Example] Hoisting
> ```js
> console.log(x); // undefined
> x = 10;
> ```
> Behind the scene javascript hoisted like
> ```js
> var x = undefined
> console.log(x) //undefined
> x = 10
> ```

> [!Tip] Why should avoid **var**
> 1. It breaks expectations around scoping.
>
> 2. It hoisting method can causes ghost bugs

---

#### Using `let`
 - It is **Block Scoped** 
 
The variable declare by `let` is not accessible outside block scope.

> [!Example] Block Scope
> ```js
> let x = 10
> if(true) { let x = 5; }
> console.log(x) // 10
> ``` 

- `let` is hoisted but stays in TDZ (Temporal Dead Zone)

> It causes Reference error.

> [!Example] Hoisting
> ```js
> console.log(x); // reference error
> let x = 10;
> ```
> Behind the scene javascript hoisted like
> ```js
> let x; // (TDZ) JS knows it will exist but don't know anyting about it
> console.log(x) // reference error
> let x = 10;
> ```

-  Can't be redeclared

> [!Example] Receclaration
> ```js
> let x = 10
> let x = 5 // Error
> ``` 

#### Using `const`
- Can't be redeclared and also reassigned
> [!Example] Reassign + Redeclare
> ```js
> const x = 10
> x = 5 // Reassign | Error
> const x = 5 // Redeclare | Error
> ``` 

 - It is also **Block Scoped** 

The variable declare by `const` is not accessible outside block scope.

> [!Example] Block Scope
> ```js
> const x = 10
> if(true) { const x = 5; }
> console.log(x) // 10
> ``` 

---

> [!Note] When to Use **var**, **let** or **const**
> 1. Always use `const` if the value should not be changed
>
> 2. Always use `const` if the type should not be changed (Arrays and Objects)
>
> 3. Only use `let` if you can't use `const`
>
> 4. Only use `var` if you MUST support old browsers.

> [!Tip] One Statement, Many Variables
> ```js
> let person = "John Doe", carName = "Volvo", price = 200;
> ```

