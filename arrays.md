Here is **ONE single Markdown block** with **all 13 Array questions + answers**, clean and ready to use:

---

````markdown
## 1. What are Arrays in JS? How to get, add and remove elements from arrays?

- An Array is a data structure used to store multiple values in a single variable.
- It is index-based, starting from index 0.

### Get Elements
```js
arr[0];       // get first element
arr[arr.length - 1];  // get last element
````

### Add Elements

```js
arr.push(4);     // add at end
arr.unshift(0);  // add at beginning
```

### Remove Elements

```js
arr.pop();       // remove from end
arr.shift();     // remove from beginning
```

---

## 2. What is the indexOf() method of an Array?

* `indexOf()` methods gets the index of a specified element in the array.
* Returns `-1` if not found.

```js
[10, 20, 30].indexOf(20);   // 1
```

---

## 3. What is the difference between find() and filter() methods of an Array?

| Method     | Returns             | Returns How Many | Use Case                         |
| ---------- | ------------------- | ---------------- | -------------------------------- |
| `find()`   | First matched value | One value        | When you need only one result    |
| `filter()` | All matched values  | Array of values  | When multiple results are needed |

```js
arr.find(x => x > 5);
arr.filter(x => x > 5);
```

---

## 4. What is the slice() method of an Array?

* `slice()` returns a **shallow copy** of a portion of the array **without modifying** the original array.
* Syntax: `slice(start, end)`

```js
[1, 2, 3, 4].slice(1, 3);   // [2, 3]
```

---

## 5. What is the difference between push() and concat() methods of an Array?

| Method     | Use                     | Modifies Original?     |
| ---------- | ----------------------- | ---------------------- |
| `push()`   | Add elements to **end** | Yes                    |
| `concat()` | Merge arrays            | No (returns new array) |

```js
arr.push(4);
arr.concat([4, 5]);
```

---

## 6. What is the difference between pop() and shift() methods of an Array?


| Method    | Removes From | Returns         | Modifies Original? |
| --------- | ------------ | --------------- | ------------------ |
| `pop()`   | End          | Removed element | Yes                |
| `shift()` | Beginning    | Removed element | Yes                |

---

## 7. What is the splice() method of an Array?

* `splice()` **adds, removes or replaces** elements in the array and **modifies the original array**.
* Syntax: `splice(start, deleteCount, itemsToAdd...)`

```js
arr.splice(1, 2, "x");  // remove 2 items from index1 and add "x"
```

---

## 8. What is the difference between the slice() and splice() methods of an Array?
- The slice() method is used get a subset of the array from the start index to the end index( end not included).

-the splice() method is used to add , remove or replace elements in an array

| Feature                 | slice()   | splice()           |
| ----------------------- | --------- | ------------------ |
| Changes original array? | ❌ No      | ✅ Yes              |
| Purpose                 | Copy part | Add/remove/replace |
| Returns                 | New array | Removed items      |

---

## 9. What is the difference between map() and forEach() array methods?
- The map() method is used when you want to mofify each element of an array and create a new array with the modified values. 

- The forEach() method is used when you want to perform some operation on each element of an array without creating a new array

| Method      | Return Value      | Used For                 |
| ----------- | ----------------- | ------------------------ |
| `map()`     | Returns new array | Transform values         |
| `forEach()` | Returns undefined | Iterate / perform action |

```js
arr.map(x => x * 2);
arr.forEach(x => console.log(x));
```

---

## 10. How to sort and reverse an array?

```js
arr.sort();      // Sorts array (as strings by default)
arr.reverse();   // Reverses array
```

> For numeric sort use:

```js
arr.sort((a, b) => a - b);
```

---

## 11. What is Array Destructuring in JS?

* A way to **extract values** from an array into variables.

```js
const [a, b, c] = [10, 20, 30];   // a=10, b=20, c=30
```

---

## 12. What are array-like objects in JS?
- Array-like object are objectt that have indexed element and a length property , similar to array, but they may not have all the methods of array like push(),pop() & others.

* Objects with **index-based values** and a **length property**, but not real arrays.

Examples: `arguments`, NodeList, HTMLCollection

---

## 13. How to convert an array-like object into an array?

```js
Array.from(arrayLike);
[...arrayLike];
...spread
```

