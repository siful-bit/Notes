---
Clear Concept: true
tags:
  - javascript
  - basic
  - huge
aliases:
  - Fixed Values
  - Variable Values
Created At: 2025-07-02T17:47:00
---


The JavaScript syntax defines two types of values:
1. Fixed values
2. Variable values

#### Javascript Fixed Values
There are 10 types of fixed values

| SL  | Type      | Example          | Has Literals |
| --- | --------- | ---------------- | :----------: |
| 1   | Number    | `123`            |      ✔       |
| 2   | Bigint    | `100n`           |      ✔       |
| 3   | String    | `'Sanin'`        |      ✔       |
| 4   | Boolean   | `true`           |      ✔       |
| 5   | Null      | `null`           |      ✔       |
| 6   | Undefined | 'undefined'      |      ✔       |
| 7   | Object    | `{name:"sanin"}` |      ✔       |
| 8   | Array     | `[1, 'one']`     |      ✔       |
| 9   | RegExp    | `/sanin/g`       |      ✔       |
| 10  | Symbol    | `Symbol('id')`   |      ❌       |


> [!Note] Literals
> In Javascript some some special fixed values which are declared directly. These are called literals. Literal can't be a function, expression and a class or symbol
> ```js
> let x = 5 // Numeric Literal
> let y = Number(5) // ❌ Not a Literal
> ```

---

#### [[Variables|Javascript Variables]]
Just like math, **variables** are used to **store** data values in also programming languages.
> JavaScript uses the keywords `var`, `let` and `const` to **declare** variables.

> [!Example] 
> ```js
> var x = 1
> let y = 5
> const pi = 3.1416
> ```
