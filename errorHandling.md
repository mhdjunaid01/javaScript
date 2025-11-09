
# ✅ Chapter 9: Error Handling — Interview-Style Q&A

## 1. What is Error Handling in JavaScript?

Error handling in JavaScript allows us to **gracefully manage and respond to runtime errors** instead of crashing the application.  
It helps maintain app stability and a better user experience, especially in MERN applications where frontend ↔ backend communication can fail.

The main keywords used for error handling are:  
`try`, `catch`, `finally`, and `throw`.

---
<img width="1075" height="535" alt="image" src="https://github.com/user-attachments/assets/ef5bbe58-b086-40ff-9e67-dbcbb0f98cd4" />

## 2. What is the role of the finally block in JS?

- The `finally` block executes **regardless of whether an error occurs or not**.
- It is commonly used for cleanup operations such as closing a DB connection, stopping a loader, or freeing resources.

Example:
```
try {
  // code that may throw error
} catch (error) {
  console.log(error.message);
} finally {
  console.log("Always runs");
}
````

---

## 3. What is the purpose of the throw statement in JS?

* The `throw` statement is used to **manually create and throw an error**.
* It helps in custom error handling and validation.

Example:

```
function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero");
  }
  return a / b;
}
```

> In MERN, we often throw custom errors in Express APIs for validation and business logic checks.

---

## 4. What is Error Propagation in JS?

Error propagation means **how errors move through the call stack** until they are caught by a `catch` block.

If an error occurs inside a nested function and is not handled there, it propagates up the call stack to the parent function until it finds a `catch`.

Example:

```
function a() {
  b();
}
function b() {
  throw new Error("Error occurred");
}
try {
  a();  // error propagates to here
} catch (e) {
  console.log("Handled:", e.message);
}
```

---

## 5. What are the best practices for error handling?

Here are some industry-standard practices (often evaluated in MERN interviews):

* Use `try...catch` for risky code blocks
* Throw descriptive custom errors
* Centralize error handling in backend using **Express error middleware**
* Do not expose internal errors to users (send safe messages)
* Log errors for debugging (Winston, Morgan, Sentry)
* Use `finally` to close connections or clean up resources

Example (Node/Express best-practice):

```
app.use((err, req, res, next) => {
  console.error(err);
  res.status(500).json({ message: "Something went wrong!" });
});
```

---

## 6. What are the different types of errors in JS?

| Error Type         | Meaning                                     | Example                        |
| ------------------ | ------------------------------------------- | ------------------------------ |
| **SyntaxError**    | Incorrect code syntax                       | `console.log("Missing quote);` |
| **ReferenceError** | Using variable that is not defined          | `x is not defined`             |
| **TypeError**      | Invalid operation on incompatible data type | `null.toUpperCase()`           |
| **RangeError**     | Number out of range                         | `new Array(-1)`                |
| **URIError**       | Incorrect URI handling                      | `decodeURI("%")`               |
| **EvalError**      | Issues with `eval()` usage                  | Rare in modern JS              |
