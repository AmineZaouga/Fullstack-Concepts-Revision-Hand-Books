# 📘 JavaScript Mid-Junior Concepts Revision Sheet


## 📑 Table of Contents
- [🔄 Async/Await & Promises](#-asyncawait--promises)
- [🌀 Event Loop & Concurrency](#-event-loop--concurrency)
- [⚙️ Closures & Lexical Scope](#️-closures--lexical-scope)
- [🏗️ Modules (ESM vs CommonJS)](#️-modules-esm-vs-commonjs)
- [🧩 Higher-Order Functions](#-higher-order-functions)
- [📦 Destructuring & Spread](#-destructuring--spread)
- [🏛️ The `this` Keyword](#️-the-this-keyword)
- [📝 Summary & Tips](#-summary--tips)

---

## 🔄 Async/Await & Promises

**Definition:**  
`async/await` makes asynchronous code look synchronous. A `Promise` represents a future value (success ✅ or failure ❌).  

**When to use:**  
- Use **Promises** when chaining multiple async operations.  
- Use **async/await** for cleaner, readable async flow.  

```javascript
// ✅ Using Promises
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("📦 Data received"), 1000);
  });
}

fetchData().then(data => console.log(data));

// ✅ Using async/await
async function getData() {
  const data = await fetchData(); // pauses until resolved
  console.log(data);
}

getData();
````

---

## 🌀 Event Loop & Concurrency

**Definition:**
The **event loop** handles execution of code, events, and async tasks in JavaScript (single-threaded but asynchronous).

**When to use:**

* Important when debugging async issues.
* Helps understand why `setTimeout` doesn’t block execution.

```javascript
console.log("Start");

setTimeout(() => console.log("⏱️ Timeout callback"), 0);

Promise.resolve("✅ Promise resolved")
  .then(console.log);

console.log("End");

// Output:
// Start
// End
// ✅ Promise resolved
// ⏱️ Timeout callback
```

---

## ⚙️ Closures & Lexical Scope

**Definition:**
A closure is a function that **remembers variables** from its outer scope even after the scope is gone.

**When to use:**

* Data encapsulation
* Function factories
* Maintaining state without global variables

```javascript
function counter() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}

const myCounter = counter();
console.log(myCounter()); // 1
console.log(myCounter()); // 2
```

---

## 🏗️ Modules (ESM vs CommonJS)

**Definition:**

* **CommonJS (`require`)** → used in Node.js (older).
* **ESM (`import/export`)** → modern standard in browsers and Node.js.

**When to use:**

* Prefer **ESM** for frontend and modern projects.
* Use **CommonJS** in legacy Node.js projects.

```javascript
// ✅ CommonJS
const fs = require('fs');

// ✅ ES Modules
import fs from 'fs';
```

---

## 🧩 Higher-Order Functions

**Definition:**
Functions that **take other functions as arguments** or **return functions**.

**When to use:**

* Array transformations (`map`, `filter`, `reduce`).
* Functional programming patterns.

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(n => n * 2); // [2, 4, 6, 8, 10]
const evens = numbers.filter(n => n % 2 === 0); // [2, 4]
const sum = numbers.reduce((acc, n) => acc + n, 0); // 15
```

---

## 📦 Destructuring & Spread

**Definition:**

* **Destructuring** → extract values from arrays/objects easily.
* **Spread (`...`)** → expand arrays/objects into new ones.

**When to use:**

* Cleaner object handling
* Avoid repetitive property access

```javascript
const user = { name: "Amine", age: 25, country: "🇹🇳" };

// Destructuring
const { name, age } = user;
console.log(name, age);

// Spread
const newUser = { ...user, role: "Dev" };
console.log(newUser);
```

---

## 🏛️ The `this` Keyword

**Definition:**
`this` refers to the execution context of a function.

**When to use:**

* In objects → refers to the object itself.
* In classes → refers to the class instance.
* With `bind`, `call`, `apply` → explicitly set `this`.

```javascript
const person = {
  name: "Amine",
  greet() {
    console.log(`Hello, my name is ${this.name}`);
  }
};

person.greet(); // Hello, my name is Amine

const greet = person.greet;
greet(); // ❌ 'this' is undefined

const boundGreet = person.greet.bind(person);
boundGreet(); // ✅ Hello, my name is Amine
```

---

## 📝 Summary & Tips

* ✅ Use `async/await` for clean async code.
* ✅ Remember the event loop order: **sync → microtasks → macrotasks**.
* ✅ Closures help maintain private state.
* ✅ Prefer modern **ESM imports/exports**.
* ✅ Master `map`, `filter`, and `reduce`.
* ✅ Use destructuring for cleaner syntax.
* ✅ Always check the value of `this`.

---



