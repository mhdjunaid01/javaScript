#  JavaScript Basics

---

## 1. What is JavaScript? What is the role of the JavaScript Engine?

- **JavaScript** is a programming language used to make static web pages **interactive and dynamic**.
- A **JavaScript Engine** is a program inside a web browser that **compiles and executes JavaScript code**.  
  Example: V8 (Chrome), SpiderMonkey (Firefox), Chakra (Edge)

---

## 2. What are Client-Side and Server-Side?

- **Client:**  
  A device or software (browser/app) that **requests** and uses services or resources from a server.  
  Example: Browser sending request to a website.

- **Server:**  
  A computer/software that **provides** services, data, or resources to clients.  
  Example: Backend server sending response to the browser.

---

## 3.  What is Scope in JavaScript?

Scope refers to the **current context of code** which determines the **accessibility of variables**.

There are **3 types of scopes**:

| Scope Type | Variables Accessible |
|------------|-----------------------|
| **Global Scope** | Accessible everywhere |
| **Function Scope** | Accessible inside the function + global scope |
| **Block Scope** | Accessible only inside the block `{ }` where declared |

> **Note:**  
> - `var` → Function scoped  
> - `let` & `const` → Block scoped

---

## 4. What is the type of variable in JS when declared without `var`, `let`, or `const`?

- If a variable is declared without `var`, `let`, or `const`, it becomes an **implicit global variable** (same as `var`, but **not recommended**).  
  ```js
  x = 10; // Implicit global
## 5. what is hoisting in js ?
   - Hoisting in js behavior where functions and variable declaration are moved to the top of their  scopes during the compilation phase.

## 6. what is json?
   - json ( javascript object notation) is a lightweight data interchange format.
   - json consists of **key-value** pairs.
 `  {
  "name": "Junaid",
  "age": 24,
  "role": "Developer"
    }`

  ## 7 What are Data Types in JavaScript?

- A **data type** defines the type of value that a variable can store.
- JavaScript data types are mainly classified into **2 categories**:
  1. **Primitive**
  2. **Non-Primitive (Reference)**

---

## 8 What are Primitive and Non-Primitive Data Types?

###  **Primitive Data Types**
- Can hold **only a single value**
- Stored directly in memory
- **Immutable** (values cannot be changed)

**Types:**
- `String`
- `Number`
- `Boolean`
- `Null`
- `Undefined`
- `BigInt`
- `Symbol`

###  **Non-Primitive (Reference) Data Types**
- Can store **multiple values and methods**
- Stored as a **reference** in memory

**Types:**
- `Object`
- `Array`
- `Function`

---

## 9 Difference Between `null` and `undefined` in JavaScript

| Feature        | `null` | `undefined` |
|----------------|--------|-------------|
| Meaning        | Intentional empty value | Declared but value not assigned |
| Type           | `object` | `undefined` |
| Assigned By    | Developer | JavaScript |
| Example        | `let a = null;` | `let b;` |

---

## 10 What is Type Coercion?

- **Type Coercion** is the automatic conversion of a value from one data type to another during certain operations or comparisons.

```js
"10" + 5  // "105" → Number converted to String
"10" - 5  // 5     → String converted to Number
```
---
<img width="895" height="483" alt="image" src="https://github.com/user-attachments/assets/0a7e8da8-6734-4aa6-aae8-e1bee3121444" />

---

````markdown
## 1. What are operators? Types of operators

- Operators are symbols used to perform operations on values or variables in JavaScript.

### Types of Operators:
1. Arithmetic Operators → `+`, `-`, `*`, `/`, `%`, `**`
2. Assignment Operators → `=`, `+=`, `-=`, `*=`, `/=`
3. Comparison Operators → `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
4. Logical Operators → `&&`, `||`, `!`
5. Unary Operators → `++`, `--`, `typeof`
6. Ternary Operator → `condition ? value1 : value2`
7. Bitwise Operators → `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>`

---

## 2. Difference between Unary, Binary & Ternary Operators

- **Unary Operator:** Works with one operand.  
  Example:  
  ```js
  let a = 5;
  a++;         // Unary
````

* **Binary Operator:** Works with two operands.
  Example:

  ```js
  5 + 3         // Binary
  ```

* **Ternary Operator:** Works with three operands.
  Syntax:

  ```js
  condition ? value1 : value2
  ```
<img width="905" height="489" alt="image" src="https://github.com/user-attachments/assets/11a74fe7-eab2-4323-98cf-a8ae30045594" />

---

## 3. What is short-circuit evaluation?

* Short-circuit evaluation is the behavior of logical operators (`&&` and `||`) where the second expression is executed only if required.

Examples:

```js
true || false   // true (second value not checked)
false && true   // false (second value not checked)
```

---

## 4. What is operator precedence?

* Operator precedence decides the order in which operators are executed in an expression.
* Higher-precedence operators run before lower-precedence operators.

Example:

```js
2 + 3 * 4      // 14 (* runs before +)
```

---

## 5. Types of conditional statements

1. `if`
2. `if...else`
3. `else if`
4. `switch`
5. Ternary operator (`condition ? value1 : value2`)

---

## 6. When to use which conditional statement

* Use **if** → for a single condition.
* Use **if...else** → when there are two possible outcomes.
* Use **else if** → when checking multiple conditions.
* Use **switch** → when comparing one value against many cases.
* Use **ternary** → for short, simple inline conditions.

---

## 7. Difference between `==` and `===`

| Operator | Meaning         | Compares                            | Example     | Result |
| -------- | --------------- | ----------------------------------- | ----------- | ------ |
| `==`     | Loose Equality  | Only value (performs type coercion) | `5 == "5"`  | true   |
| `===`    | Strict Equality | Value + Data Type                   | `5 === "5"` | false  |

---

## 8. Difference between Spread and Rest operator

* Both use `...` but serve different purposes.

### Spread Operator

* Used to expand array or object values.

```js
let arr1 = [1, 2, 3];
let arr2 = [...arr1, 4, 5];
```

### Rest Operator

* Used to collect multiple values into a single array.

```js
function sum(...numbers) {
  return numbers.reduce((a, b) => a + b);
}
```

```

---

If this is now **exactly correct**, I will turn this into a downloadable `.md` file next — just say:

**"Create .md file"**
```

