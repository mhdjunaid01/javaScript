## 1. What is a String in JavaScript?

A string is a **primitive data type** used to store and manipulate data .
It is a sequence of characters enclosed in single quotes (`' '`), double quotes (`" "`).

Example:
```
let message = "Hello World";
````

---

## 2. What are template literals and string interpolation in JavaScript?

Template literals are a **modern way to create dynamic strings** using backticks (`` ` ``).
String interpolation allows embedding variables or expressions using `${ }`.

Example:

```
const name = "Junaid";
const greeting = `Hello, ${name}! Welcome to the MERN world.`;
```

I would use template literals especially when working with JSX, logging dynamic data, or writing multi-line strings.

---

## 3. What is the difference between single quotes ('), double quotes ("), and backticks ( ` )?

| Feature              | Single Quotes `' '` | Double Quotes `" "` | Backticks `` ` `` |
| -------------------- | ------------------- | ------------------- | ----------------- |
| Basic Strings        | ✅ Yes               | ✅ Yes               | ✅ Yes             |
| String Interpolation | ❌ No                | ❌ No                | ✅ Yes             |
| Multi-line Support   | ❌ No                | ❌ No                | ✅ Yes             |

* In real projects, I prefer **backticks** because they support interpolation and multi-line strings, which are useful in React and Node.js development.

---

## 4. What are some important string operations in JavaScript?

Some commonly used string operations are:

| Operation              | Method           | Example                              |
| ---------------------- | ---------------- | ------------------------------------ |
| Length                 | `.length`        | `str.length`                         |
| Convert to Lowercase   | `.toLowerCase()` | `"MERN".toLowerCase()`               |
| Convert to Uppercase   | `.toUpperCase()` | `"mern".toUpperCase()`               |
| Extract Part of String | `.slice()`       | `"JavaScript".slice(0,4)` → `"Java"` |
| Replace Text           | `.replace()`     | `"Hi Junaid".replace("Hi","Hello")`  |
| Remove Spaces          | `.trim()`        | `"  Hello  ".trim()`                 |
| Check Substring        | `.includes()`    | `"Hello".includes("ell")`            |
| Split String           | `.split()`       | `"a,b,c".split(",")`                 |

---

## 5. What is string immutability?

String immutability means **strings cannot be changed once created**.
Any modification returns a **new string** instead of editing the original one.

Example:

```
let str = "Hello";
str[0] = "M";  // ❌ Won’t modify the string
str = "Mello"; // ✅ Creates a new string
```

This concept is important when managing performance in large-scale MERN apps, especially when handling large string operations.

---

## 6. In how many ways can you concatenate strings?

There are 3 commonly used ways:

### 1. Using `+` Operator

```
"Hello" + " World";
```

### 2. Using `concat()` Method

```
"Hello".concat(" World");
```

### 3. Using Template Literals (Modern & Recommended)

```
`${"Hello"} World`;
```

> In interviews, I mention that **template literals** are preferred today, especially in React JSX and Node.js logging.

---

## 🔥 Additional Important Interview Questions on Strings

### 7. How do you compare two strings in JavaScript?

We use `===` to compare both value and type:

```
"hello" === "hello"   // true
"Hello" === "hello"   // false (case-sensitive)
```

---

### 8. How do you convert a string to a number in JavaScript?

```
Number("50");     // 50
+"50";            // 50
parseInt("50");   // 50
```

---

### 9. How do you check if a value is a string?

```
typeof str === "string";
```

Or:

```
str instanceof String; // for String objects
```

---

### 10. How do you reverse a string in JavaScript?

```
"hello".split("").reverse().join("");
```

---

### 11. How do you handle multi-line strings in JS?

Using backticks:

```
const text = `
Welcome to MERN
Stack Development
`;
```
