
## 1. What is a loop? What are the types of loops in JS?

- A loop is a control structure that repeats a block of code until a specified condition becomes false.

### Types of Loops in JavaScript:
1. `for`
2. `while`
3. `do...while`
4. `for...of`
5. `for...in`
6. `forEach()` (array loop)

---

## 2. What is the difference between while and for loops?
```
- For loop allows to iterate a block if code a specifix number of times.
- for loop is better for condition with initiakization and with increment
  becuase all can be set in just one line of code
| Feature | for loop | while loop |
```
```
- while loop execute a block of code while a certain condition is true.
- while loop is better when there is only condition, no initialization, 
  no increment
```
|--------|----------|-------------|
| Use Case | When number of iterations is known | When iterations count is unknown |
| Structure | Initialization, condition, and update in one line | Initialization outside and update inside loop |
| Example | `for(let i=0; i<5; i++)` | `while(i<5) { i++; }` |

---

## 3. What is the difference between while and do-while loops?

| Feature | while | do...while |
|----------|--------|-------------|
| Condition Check | Before execution | After execution |
| Minimum Execution | 0 times | 1 time |
| Syntax | ```while(cond){...} ``` | ``` do{...}while(cond) ``` |
<img width="944" height="456" alt="image" src="https://github.com/user-attachments/assets/9d5c11e3-bc36-4b00-b190-9a9e6d6e9487" />

Example:
```js
do {
  console.log("Runs at least once");
} while(false);
````

---

## 4. What is the difference between break and continue statement?

| Statement  | Meaning                   | Effect                  |
| ---------- | ------------------------- | ----------------------- |
| `break`    | Exits the loop completely | Stops loop fully        |
| `continue` | Skips current iteration   | Moves to next iteration |

---

## 5. What is the difference between for and for...of loop in JS?

| Loop       | Used For                            | Iterates On                  | Returns                |
| ---------- | ----------------------------------- | ---------------------------- | ---------------------- |
| `for`      | General loop                        | Any iterable or number range | Index controlled logic |
| `for...of` | Collections (Arrays, Strings, Maps) | Values of iterable           | Value                  |

```js
for(let i=0; i<arr.length; i++) {}      // for
for(let value of arr) {}                // for...of
```

---

## 6. What is the difference between for...of and for...in loop?

| Loop       | Used For              | Iterates On  | Returns |
| ---------- | --------------------- | ------------ | ------- |
| `for...of` | Arrays, Strings, Maps | Values       | Value   |
| `for...in` | Objects               | Keys/Indexes | Key     |

```js
for (let key in obj) {}    // keys
for (let value of arr) {}  // values
```

---

## 7. What is forEach method? Compare it with for...of and for...in loop? vimp

* `forEach()` is an array method used to execute a function for each array element.

| Feature        | forEach()    | for...of              | for...in  |
| -------------- | ------------ | --------------------- | --------- |
| Works On       | Arrays only  | Arrays, strings, maps | Objects   |
| Returns        | Nothing      | Values                | Keys      |
| Break/Continue | ❌ Cannot use | ✅ Can use             | ✅ Can use |

---

## 8. When to use for...of loop and when to use forEach method in applications?
- for...of loop is suitable when you need more control over the loop , such as using break statement inside.
- foreEach method iterate over each element of the array and perform some action on each element.
* Use **for...of** when:

  * You need to loop through values
  * You need break/continue control
  * Better for async/await usage

* Use **forEach** when:

  * You want to perform an action for each element
  * No need to break or stop in between
  * Cleaner and shorter callback-based code

Example:

```js
// Better: for...of with break
for (const item of arr) {
  if(item === 3) break;
}

// Better: forEach for simple iteration
arr.forEach(item => console.log(item));
```
