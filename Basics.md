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
