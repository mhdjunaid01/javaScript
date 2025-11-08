````
# ✅ Chapter 8: DOM — Interview-Style Q&A

## 1. What is DOM? What is the difference between HTML and DOM?

- **DOM (Document Object Model)** is a programming interface that represents a webpage as a **tree structure of objects**, allowing JavaScript to interact with and manipulate HTML content dynamically.
- The DOM is created by the browser when it reads the HTML.

### Difference Between HTML and DOM

| HTML | DOM |
|------|------|
| Static structure of the webpage | Dynamic, in-memory representation of the webpage |
| Cannot be changed directly | Can be modified using JavaScript |
| Defines content | Allows scripting & manipulation of content |

Simply:  
**HTML is the source**, **DOM is the live version in browser’s memory**.

---

## 2. How do you select, modify, create and remove DOM elements?

### Select Elements
```js
document.getElementById("title");
document.querySelector(".btn");
````

### Modify Elements

```
element.textContent = "Updated Text";
element.style.color = "blue";
```

### Create Elements

```
const div = document.createElement("div");
div.textContent = "Hello";
document.body.appendChild(div);
```

### Remove Elements

```
element.remove();
```

---

## 3. What are selectors in JS?

Selectors are used to **select HTML elements** from the DOM.

Common Selectors:

```
document.getElementById("id");
document.getElementsByClassName("class");
document.getElementsByTagName("tag");
document.querySelector("css-selector");
document.querySelectorAll("css-selector");
```

---

## 4. What is the difference between getElementById, getElementsByClassName and getElementsByTagName?

| Method                     | Returns        | Selector Type | Live/Static |
| -------------------------- | -------------- | ------------- | ----------- |
| `getElementById()`         | Single element | ID            | Static      |
| `getElementsByClassName()` | HTMLCollection | Class         | Live        |
| `getElementsByTagName()`   | HTMLCollection | Tag name      | Live        |

> **Live** means changes in DOM reflect automatically.

---

## 5. What is the difference between querySelector() and querySelectorAll()?

| Method               | Returns               | Output         | Example                             |
| -------------------- | --------------------- | -------------- | ----------------------------------- |
| `querySelector()`    | First matched element | Single element | `document.querySelector(".box")`    |
| `querySelectorAll()` | All matched elements  | NodeList       | `document.querySelectorAll(".box")` |

> NodeList supports `forEach()`, HTMLCollection does not.

---

## 6. What are the methods to modify element properties and attributes?

### Modify Properties

```
element.textContent = "Hello";
element.style.backgroundColor = "yellow";
element.className = "active";
```

### Modify Attributes

```
element.setAttribute("id", "title");
element.getAttribute("id");
element.removeAttribute("id");
```

---

## 7. What is the difference between innerHTML and textContent?

| Method        | Reads HTML tags?       | Safe from XSS? | Use Case               |
| ------------- | ---------------------- | -------------- | ---------------------- |
| `innerHTML`   | ✅ Yes (renders HTML)   | ❌ No           | Insert HTML content    |
| `textContent` | ❌ No (plain text only) | ✅ Yes          | Insert plain text only |

Example:

```ins
element.innerHTML = "<b>Hello</b>"     // Bold text
element.textContent = "<b>Hello</b>"   // Displays tags as text
```
