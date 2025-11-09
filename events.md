
## 1. What are Events? How are events triggered?

Events are actions or occurrences that happen in the browser, such as clicking, typing, scrolling, or submitting a form.  
JavaScript can listen to these events and run code in response, making web pages interactive.

Events can be triggered in 3 ways:
1. **User actions** (click, input, mouseover, submit)
2. **Browser actions** (page load, resize, scroll)
3. **Programmatically** using `element.click()` or dispatching custom events

---

## 2. What are the types of events in JavaScript?

Common event categories:

| Category | Examples |
|-----------|------------|
| Mouse Events | click, dblclick, mouseover, mouseout |
| Keyboard Events | keydown, keyup, keypress |
| Form Events | submit, change, focus, blur |
| Window Events | load, resize, scroll, unload |
| Clipboard Events | copy, paste, cut |
| Touch Events (Mobile) | touchstart, touchend, touchmove |

---

## 3. What is the Event Object in JS?

The Event Object is an object automatically passed to event handlers that contains **details about the event** such as target element, type of event, mouse position, key pressed, etc.

Example:
```js
button.addEventListener("click", function(event) {
  console.log(event.target);   // element clicked
});
````

---

## 4. What is Event Delegation in JS?

Event Delegation is a technique where instead of adding event listeners to multiple child elements, we **attach a single event listener to a parent element** and handle child events based on `event.target`.

Benefits:

* Better performance
* Fewer event listeners
* Works for dynamically added elements

Example:

```
document.querySelector("ul").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    console.log("Item clicked:", e.target.textContent);
  }
});
```

---

## 5. What is Event Bubbling in JS?

Event Bubbling is the phase where an event starts from the **target element** and travels **upward to its parent elements** until the root (`document`).

Order: Child → Parent → Document

---

## 6. How can you stop event propagation or event bubbling in JS?

Use:

```
event.stopPropagation();
```

This prevents the event from moving to its parent elements.

---

## 7. What is Event Capturing in JS?

Event Capturing is the opposite of bubbling.
The event travels from the **document down to the target element**.

Order: Document → Parent → Child

To enable capturing:

```
element.addEventListener("click", handler, true);
```

(3rd argument `true` enables capturing phase)

---

## 8. What is the purpose of the event.preventDefault() method in JS?

`event.preventDefault()` prevents the **default browser behavior** of an event.

Examples:

* Stop form submission
* Prevent right-click context menu
* Prevent link navigation

```
form.addEventListener("submit", (e) => {
  e.preventDefault(); // stops form from reloading page
});
```

---

## 9. What is the use of "this" keyword in the context of event handling in JS?

Inside a regular function event handler, `this` refers to the **DOM element that received the event**.

Example:

```
button.addEventListener("click", function() {
  console.log(this);  // refers to button
});
```

> Note: In arrow functions, `this` does NOT refer to the element (it inherits from parent scope), so regular functions are recommended for event handlers.

---

## 10. How to remove an event handler from an element in JS?

Use `removeEventListener()` and ensure the same function reference is used for removal.
