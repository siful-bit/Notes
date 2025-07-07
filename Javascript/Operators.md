---
Clear Concept: false
tags:
  - huge
  - javascript
  - List
  - important
  - basic
aliases:
  - Assignment
  - Arithmetic
  - Comparision
  - Ternary
Created At: 2025-07-04T11:52:00
---

Javascript Operators are used to perform different types of mathematical and logical computations.

## Types of Operators
#List 

There are 8 types of Operators in javascript

1. [[#Arithmetic Operators]]
2. [[#Assignment Operators]]
3. [[#Comparison Operators]]
4. [[#String Operators]]
5. [[#Logical Operators]]
6. [[#Bitwise Operators]]
7. [[#Ternary Operator]]
8. [[#Type Operators]]

---

### Arithmetic Operators
#basic #table

Just operate mathematical computation

| Operator | Description                   |
| :------: | ----------------------------- |
|    +     | Addition                      |
|    -     | Subtraction                   |
|    *     | Multiplication                |
|    /     | Division                      |
|    **    | Exponentiation                |
|    %     | Modulus (Division Remainder) |
|    ++    | Increment                     |
|    --    | Decrement                     |


> [!NOTE] Operators and Operands
> The numbers (in an arithmetic operation) are called **operands**.
> 
> The operation (to be performed between the two operands) is defined by an **operator**.
> ```js
> 100 + 50
> ```
> Here `100` and `50` is operand and `+` is operator

#### Operator Precedence
> Operator precedence describes the order in which operations are performed in an arithmetic expression.

Multiplication (`*`) and division (`/`) have higher **precedence** than addition (`+`) and subtraction (`-`). 

> [!Tip] Parentheses `()`
> When using parentheses, operations inside the parentheses are computed first

Operations with the same precedence (like * and /) are computed from left to right

> [!Example]
> ```js
> // same precedence goes left --> right
> let x = 10 * 6 / 3 // 20
> ```


---

### Assignment Operators
Assignment operators assign values to JavaScript variables.

#basic #important

| Operator | Example | Same As    |        Description        |
| :------: | ------- | ---------- | :-----------------------: |
|    =     | x = y   | x = y      |        Assignment         |
|    +=    | x += y  | x = x + y  |    Addition Assignment    |
|    -=    | x -= y  | x = x - y  |  Subtraction Assignment   |
|    *=    | x *= y  | x = x * y  | Multiplication Assignment |
|    /=    | x /= y  | x = x / y  |    Division Assignment    |
|   **=    | x **= y | x = x ** y | Exponentiation Assignment |
|    %=    | x %= y  | x = x % y  |   Remainder Assignment    |

#### Bitwise Assignment
| Operator | Example  | Same As     |
| -------- | -------- | ----------- |
| &=       | x &= y   | x = x & y   |
| \|=      | x \|= y  | x = x \| y  |
| ^=       | x ^= y   | x= x ^ y    |
| <<=      | x <<= y  | x = x << y  |
| >>=      | x >>= y  | x = x >> y  |
| >>>=     | x >>>= y | x = x >>> y |

#### Logical Assignment
#important #hard 

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| &&=      | x &&= y | x = x && y |
| \|=      | x \|= y | x = x \| y |
| ??=      | x ??= y | x = x ?? y |


---

### Bitwise Operators
#important #hard

Operate **directly on the binary bits** of numbers

| Operator | Description          |                             Description                             |
| -------- | -------------------- | :-----------------------------------------------------------------: |
| &        | AND                  |                         Both Bits must be 1                         |
| \|       | OR                   |                      one of two bits must be 1                      |
| ~        | NOT                  |                          Inverts all bits                           |
| ^        | XOR                  |                   only one of two bits must be 1                    |
| <<       | Left Shift           |           Shifts left by pushing zeros in from the right            |
| >>       | Right Shift          | Shifts right by pushing copies of the leftmost bit in from the left |
| >>>      | Unsigned Right Shift |           Shifts right by pushing zeros in from the left            |

#### Example

|Operation|Result|Same as|Result|
|---|---|---|---|
|5 & 1|1|0101 & 0001|0001|
|5 \| 1|5|0101 \| 0001|0101|
|~ 5|10|~0101|1010|
|5 << 1|10|0101 << 1|1010|
|5 ^ 1|4|0101 ^ 0001|0100|
|5 >> 1|2|0101 >> 1|0010|
|5 >>> 1|2|0101 >>> 1|0010|

> [!NOTE] JavaScript Uses 32 bits Bitwise Operands
> JavaScript stores numbers as 64 bits floating point numbers, but all bitwise operations are performed on 32 bits binary numbers.
> 
> Before a bitwise operation is performed, JavaScript converts numbers to 32 bits signed integers.


> [!Tip] Two's Complement
> The most left bit denotes the sign of number. If it 1 it represent it's negative and if 0 it will be positive.
> 
> Simple formula to calculate the binary is `~x = -(x + 1)`

##### AND (`&`)
If both true then true.

| Operation | Result |
| --------- | ------ |
| 0 & 0     | 0      |
| 1 & 0     | 0      |
| 0 & 1     | 0      |
| 1 & 1     | 1      |
##### OR (`|`)
If any one true then true.

| Operation | Result |
| --------- | ------ |
| 0 \| 0    | 0      |
| 1 \| 0    | 1      |
| 0 \| 1    | 1      |
| 1 \| 1    | 1      |
##### XOR (`^`)
If only one is true then true.

| Operation | Result |
| --------- | ------ |
| 0 ^ 0     | 0      |
| 1 ^ 0     | 1      |
| 0 ^ 1     | 1      |
| 1 ^ 1     | 0      |

##### Zero Left Shift (`<<`)
One or more zero bits are pushed in from the right, and the leftmost bits fall off.

| Decimal | Binary                           |
| ------- | -------------------------------- |
| 5       | 00000000000000000000000000000101 |
| 5 << 1  | 00000000000000000000000000001010 |

##### Right Shift With Sign (`>>`)
This is a sign preserving right shift. Copies of the leftmost bit are pushed in from the left, and the rightmost bits fall off.

| Decimal | Binary                           |
| ------- | -------------------------------- |
| -5      | 11111111111111111111111111111011 |
| -5 >> 1 | 11111111111111111111111111111101 |

##### Zero Right Shift (`>>>`)
| Decimal | Binary                           |
| ------- | -------------------------------- |
| 5       | 00000000000000000000000000000101 |
| 5 >>> 1 | 00000000000000000000000000000010 |

### Comparison Operators
Comparison operators are used to test for `true` or `false`

| Operator | Description            | Example                    | Return                |
| :------: | ---------------------- | -------------------------- | --------------------- |
|    ==    | Equal to               | '5' == 5<br>6 == 5         | true<br>false         |
|   ===    | Equal to with type     | '5' === 5<br>6 == 6        | false<br>true         |
|    !=    | Not Equal to           | '5' != 5<br>6 != 5         | false<br>true         |
|   !==    | Not Equal to with type | '5' !== 5<br>5 !== 5       | true<br>false         |
|    >     | Greater than           | 6 > 5<br>4 > 5             | true<br>false         |
|    <     | Less than              | 4 < 5<br>6 < 5             | true<br>false         |
|    >=    | Greater than Equal to  | 6 >= 5<br>4 >= 5<br>5 >= 5 | true<br>false<br>true |
|    <=    | Less than Equal to     | 4 <= 5<br>6 <= 5<br>5 <= 5 | true<br>false<br>true |

---

### Logical Operators
Logical operators are used to determine the logic between variables or values.

> [!Info] Workflow
> Logical operators return right-side operand in the condition of left-side operand.


| Operator | Name               | Description                         |
| -------- | ------------------ | ----------------------------------- |
| &&       | Logical AND        | when left side is truthy            |
| \|\|     | Logical OR         | When left side is falsy             |
| ??       | Nullish Coalescing | When left side is null or undefined |
| !        | Logical Not        | Invert the value                    |

---

### Ternary Operator
It's just a shortcut of if-else statement. It returns the first value when the condition is true rather returns the second value.

> _variablename_ = (_condition_) ? _value1_:_value2_


> [!Example] Ternary Operator
> ```js
> let voteable = (age < 18) ? "Too young":"Old enough";
> ```

---

### Type Operators
There are two types of **Type Operators** in javascript

| Operators    | Description                                                           |
| ------------ | --------------------------------------------------------------------- |
| `typeof`     | Returns the data type                                                 |
| `instanceof` | Returns `true` if an object is an instance of a specified object type |

#### typeof
The `typeof` operator returns the type of a variable or an expression

Javascript has 7 types of primitive data types and only except null, all of them typeof operator returns.

**Primitive case**

1. string
2. number
3. boolean
4. bigint
5. symbol
6. undefined
7. null (***Returns Object***)

**Non-Primitive (or Special) Cases:**

- object (for objects, arrays, `null`, etc.)
- function (for functions)

#### instanceof
The `instanceof` operator returns `true` if an object is an instance of a specified object type or **object constructor function**

```js
const myArray = [1, 2, 3];
const myObject = { a: 1 };

console.log(myArray instanceof Array);  // true
console.log(myObject instanceof Object); // true
console.log(myArray instanceof Object); // true (arrays are also objects)
```

> [!NOTE] Primitive and instanceof
> `instanceof` _only_ works with objects. **It does not work with primitive data types** directly, because primitives do not have a prototype chain. If you try to use `instanceof` with a primitive, it will always return `false`.

---

### String Operators

| Operator | Name          | Description          |
| -------- | ------------- | -------------------- |
| "" + ""  | Concatenation | Adds two string      |
| + "123"  | Unary         | Converts into number |
