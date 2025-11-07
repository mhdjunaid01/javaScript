
## 1. What are Functions in JS? What are the types of functions?

- A function is a reusable block of code that performs a specific task when called.
- Functions help in code reusability, cleaner code, and modular development.

### Types of Functions:
1. Named Function
2. Anonymous Function
3. Function Expression
4. Arrow Function
5. Callback Function
6. Higher-Order Function
7. Constructor Function
8. IIFE (Immediately Invoked Function Expression)

---

## 2. What is the difference between named and anonymous functions? When to use what in applications?

### Named Function
- A function with a name.
- Easier to debug and reuse.

```
function add(a, b) {
  return a + b;
}
````

### Anonymous Function

* A function without a name.
* Commonly used as a callback or inside another function.

```
setTimeout(function () {
  console.log("Hello");
}, 1000);
```

### When to Use:

* **Named functions** → Use when function needs reuse or debugging.
* **Anonymous functions** → Use for one-time use, callbacks, and inline operations.

---

## 3. What is function expression in JS?

* A function stored in a variable is called a Function Expression.
* It can be named or anonymous, but mostly used as anonymous.

```
const multiply = function(a, b) {
  return a * b;
};
```

---

## 4. What are Arrow Functions in JS? What is its use?

* Arrow Functions are a shorter syntax for writing function expressions.
* They do not have their own `this`, `arguments`, or `prototype`.

```
const add = (a, b) => a + b;
```

**Use Case:**
Useful for callbacks, cleaner code, and when you don't want `this` binding.

---

## 5. What are Callback Functions? What is its use?

* A callback function is a function passed as an argument to another function.
* Used in asynchronous operations like API calls, setTimeout, event listeners.

```
function greet(name, callback) {
  callback(name);
}

greet("Junaid", (n) => console.log("Hello " + n));
```

---

## 6. What is a Higher-order function in JS?

* A function that **takes another function as an argument** or **returns a function** is called a Higher-Order Function.

```
function higher(fn) {
  return fn();
}
```

Examples: `map()`, `filter()`, `reduce()`

---

## 7. What is the difference between arguments and parameters?

| Term       | Meaning                           | Example              |
| ---------- | --------------------------------- | -------------------- |
| Parameters | Variables in function definition  | `function add(x, y)` |
| Arguments  | Actual values passed when calling | `add(5, 3)`          |

---

## 8. In how many ways can you pass arguments to a function?

1. **By Value**

   * For primitive data types (number, string, boolean)
   * Original value does not change

2. **By Reference**

   * For non-primitive types (arrays, objects)
   * Original value may change since reference is passed

```
let obj = {a: 1};
function change(o) { o.a = 5; }
change(obj); // obj becomes {a: 5}

```
<img width="935" height="444" alt="image" src="https://github.com/user-attachments/assets/168b73bb-24ff-40b2-a85b-7b5abdb76ed7" />

## 9 how do you use default parameter in a function 
<img width="906" height="363" alt="image" src="https://github.com/user-attachments/assets/f04f640a-fa94-4b5f-b587-5f27d19fdecf" />

---
Understood — here is the **same content**, but numbering starts from **9**.

---

````markdown
## 9. What is the use of event handling in JS?

- Event handling allows JavaScript to **respond to user actions or browser events** such as clicks, keypress, mouse movements, form submission, page load, etc.
- It helps make web pages **interactive and dynamic**.

Example:
```js
button.addEventListener("click", function() {
  console.log("Button clicked");
});
````

---

## 10. What are First-Class Functions in JavaScript?

* In JavaScript, functions are treated as **first-class citizens**.
* This means functions can be:

  * Stored in variables
  * Passed as arguments to other functions
  * Returned from other functions
  * Stored in arrays/objects

Example:

```js
const greet = () => "Hello";      // stored in variable
function callMe(fn) { fn(); }     // passed as argument
```

---

## 11. What are Pure and Impure Functions in JS?

### Pure Function

* Returns the **same output for the same input**
* Does **not modify external state** (no side effects)

```js
function add(a, b) {
  return a + b;
}
```

### Impure Function

* Output may vary even with same input
* **Modifies external state** or uses external values

```js
let x = 5;
function addToX(a) {
  x = x + a;   // modifies external variable
  return x;
}
```

---

## 12. What is Function Currying in JS?

* Currying transforms a function with multiple arguments into a **series of functions**, each taking one argument.
* Helps in reusability and functional programming patterns.

Example:

```js
function curry(a) {
  return function(b) {
    return function(c) {
      return a + b + c;
    };
  };
}

curry(1)(2)(3); // 6
```

---

## 13. What are call, apply, and bind methods in JS?

These methods are used to **control the value of `this`** inside a function.

### `call()`

* Calls a function with given `this` value and **arguments separated by commas**.

```js
func.call(obj, arg1, arg2);
```

### `apply()`

* Calls a function with given `this` value and **arguments as an array**.

```js
func.apply(obj, [arg1, arg2]);
```

### `bind()`

* Returns a **new function** with permanently bound `this`.

```js
const newFunc = func.bind(obj);
newFunc();
```

| Method  | Executes Immediately?       | Arguments       |
| ------- | --------------------------- | --------------- |
| call()  | ✅ Yes                       | comma separated |
| apply() | ✅ Yes                       | array           |
| bind()  | ❌ No (returns new function) | comma separated |

