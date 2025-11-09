
# ✅ Chapter 10: Objects — Interview-Style Q&A

## 1. What are Objects in JavaScript?

An object in JavaScript is a **collection of key–value pairs** used to store structured data and properties with their values.  
Objects allow us to represent real-world entities, making them essential in MERN applications (API responses, user data, configs, etc.).

Example:
```js
const user = { name: "Junaid", age: 22, role: "MERN Developer" };
````

---

## 2. In how many ways can we create an object?

Common ways to create objects:

```
// 1. Object Literal (most common)
const obj1 = {};

// 2. Using new Object()
const obj2 = new Object();

// 3. Constructor Function
function Person(name) { this.name = name; }
const obj3 = new Person("Ali");

// 4. Object.create()
const obj4 = Object.create({ a: 10 });

// 5. Class (ES6)
class User { constructor(name){ this.name = name; } }
const obj5 = new User("Junaid");
```

---

## 3. What is the difference between an array and an object?

| Feature       | Array              | Object                        |
| ------------- | ------------------ | ----------------------------- |
| Structure     | Ordered list       | Key–value pairs               |
| Indexing      | Indexed by numbers | Indexed by keys               |
| Best Used For | Lists of items     | Detailed data with properties |

---

## 4. What is the difference between array and objects?

A repeated question, but answer expected differently in interview:

* Use an **Array** when you need an **ordered collection** of items.
* Use an **Object** when you need to store **properties with values** for an entity.

Example:
User list → Array
User details → Object

---

## 5. How do you add, modify, or delete properties of an object?

### Add / Modify

```
const user = { name: "Junaid" };
user.age = 22;             // add
user.name = "Mohammed";    // modify
```

### Delete

```
delete user.age;
```

---

## 6. Explain the difference between dot notation and bracket notation?

| Notation | Example            | When to Use                                     |
| -------- | ------------------ | ----------------------------------------------- |
| Dot      | `obj.name`         | When key is known & valid identifier            |
| Bracket  | `obj["full-name"]` | When key has spaces, special chars, dynamic key |

```
const user = { "full-name": "Junaid", age: 22 };
user["full-name"];     // must use bracket
```

---

## 7. What are some common methods to iterate over the properties of an object?

```
const obj = { a: 1, b: 2, c: 3 };

// for...in (keys)
for (let key in obj) { console.log(key, obj[key]); }

// Object.keys() → array of keys
Object.keys(obj);

// Object.values() → array of values
Object.values(obj);

// Object.entries() → array of [key, value] pairs
Object.entries(obj).forEach(([k, v]) => console.log(k, v));
```

---

## 8. How do you check if a property exists in an object?

```
"name" in user
user.hasOwnProperty("name")
Object.hasOwn(user, "name")   // modern recommended way
```

---

## 9. How do you clone or copy an object?

### Shallow Copy

```
const copy1 = { ...obj };
const copy2 = Object.assign({}, obj);
```

### Deep Copy

```
const deepCopy = JSON.parse(JSON.stringify(obj));   // simple deep copy
```

---

## 10. What is the difference between deep copy and shallow copy in JS?

| Feature                | Shallow Copy                 | Deep Copy                         |
| ---------------------- | ---------------------------- | --------------------------------- |
| Copies nested objects? | ❌ No                         | ✅ Yes                             |
| Memory Reference       | Shares nested reference      | Duplicate entire structure        |
| Example                | Spread operator `{ ...obj }` | `JSON.parse(JSON.stringify(obj))` |

```
const obj1 = { a: 1, b: { x: 10 } };

const shallow = { ...obj1 };
shallow.b.x = 50;     // affects original!

const deep = JSON.parse(JSON.stringify(obj1));
deep.b.x = 50;        // does NOT affect original
```

---


## 11. What is Set in JavaScript?

A `Set` is a built–in JavaScript object that stores **unique values** (no duplicates allowed).  
It is useful when dealing with unique data like user IDs, tags, and filtering duplicates.

Key features:
- Stores only unique values
- Maintains insertion order
- Can store any data type

Example:
```js
const set = new Set([1, 2, 2, 3]);
console.log(set);      // Set {1, 2, 3}

set.add(4);
set.delete(2);
set.has(1);            // true
````

Use cases in MERN:

* Removing duplicate data
* Maintaining unique user IDs, tokens, permissions
* Efficient searching (faster than array `.includes()`)

---

## 12. What is Map in JavaScript?

A `Map` is a collection of **key–value pairs**, similar to an object, but with enhanced capabilities.

Key features:

* Keys can be of **any data type** (object, function, number, string)
* Maintains insertion order
* Provides built-in methods like `set()`, `get()`, `has()`, `delete()`

Example:

```js
const map = new Map();
map.set("name", "Junaid");
map.set(1, "Number Key");
map.get("name");       // "Junaid"
```

Use cases in MERN:

* Storing dynamic data with non-string keys
* Storing cached results (e.g., DB query caching)
* Mapping users to sockets in real-time apps

---

## 13. What is the difference between Map and Object?

| Feature     | Object                              | Map                                     |
| ----------- | ----------------------------------- | --------------------------------------- |
| Key Types   | Only strings & symbols              | Any type (object, array, number, etc.)  |
| Key Order   | Not guaranteed (older JS)           | Maintains insertion order               |
| Size Check  | No direct way                       | `map.size`                              |
| Iteration   | More manual                         | Easy with `map.forEach()` or `for...of` |
| Performance | Slower for frequent inserts/deletes | Better performance for dynamic data     |

Example difference:

```
const obj = { name: "Ali" };
const map = new Map([["name", "Ali"]]);
```

**When to use what (Interview Tip):**

* Use **Object** when you need a structured data model (like user, product).
* Use **Map** when you need a **dynamic, frequently changing key–value store**, especially when keys are not strings.
