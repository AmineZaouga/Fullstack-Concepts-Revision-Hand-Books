

````markdown
# 📖 JavaScript Skill Test – Complete Revision Sheet

![JavaScript Banner](https://raw.githubusercontent.com/github/explore/main/topics/javascript/javascript.png)

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)  
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)](#)  
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)  
[![Made with Love](https://img.shields.io/badge/Made%20with-Love-red?logo=heart)](#)  
[![GitHub last commit](https://img.shields.io/github/last-commit/AmineZaouga/Fullstack-Concepts-Revision-Hand-Books)](https://github.com/AmineZaouga/Fullstack-Concepts-Revision-Hand-Books/commits/main)  
[![GitHub repo size](https://img.shields.io/github/repo-size/AmineZaouga/Fullstack-Concepts-Revision-Hand-Books)](https://github.com/AmineZaouga/Fullstack-Concepts-Revision-Hand-Books)

> A complete, one-stop revision file for JavaScript skill test topics.  
> Includes clear explanations, icons, code examples, and MDN references for each subject.  
> Now with emoji navigation 🚀  

---

## 📚 Table of Contents  

- [📦 Variables](#variables)  
- [🍏 Arrays](#arrays)  
- [🔀 Conditionals](#conditionals)  
- [🖱️ Events](#events)  
- [⚙️ Functions](#functions)  
- [📄 JSON](#json)  
- [🔁 Loops](#loops)  
- [🧮 Math](#math)  
- [🗂️ Object Basics](#object-basics)  
- [🔤 Strings](#strings)  
- [🏛️ OOP in JavaScript](#oop-in-javascript)  
- [📌 How to Use This Sheet](#how-to-use-this-sheet)  

---

<a name="variables"></a>
## 📦 Variables

**Explanation:**  
Variables store data values.  
- `let` → block-scoped, reassignable.  
- `const` → block-scoped, **not** reassignable.  
- `var` → function-scoped (avoid in modern code).

```javascript
let age = 25;       // can be changed
const PI = 3.1416;  // cannot be changed
var name = "Amine"; // old syntax, avoid if possible

age = 26;           // ✅ works
// PI = 3.14;       // ❌ error
````

**Learn more:** [MDN Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations)

Navigation:
[⬅️ Home](#) | [➡️ Arrays →](#arrays)

---

<a name="arrays"></a>

## 🍏 Arrays

**Explanation:**
Arrays hold multiple values in a single variable.

```javascript
let fruits = ["apple", "banana", "cherry"];

console.log(fruits[0]); // "apple"
fruits.push("orange");  // add at the end
fruits.pop();           // remove last element
fruits.unshift("kiwi"); // add at the start
fruits.shift();         // remove first element

// Iterating
fruits.forEach(fruit => console.log(fruit));
```

**Learn more:** [MDN Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

Navigation:
[⬅️ Variables](#variables) | [⬅️ Home](#) | [➡️ Conditionals →](#conditionals)

---

<a name="conditionals"></a>

## 🔀 Conditionals

**Explanation:**
Conditionals execute code blocks based on conditions.

```javascript
let score = 85;

if (score >= 90) {
  console.log("A");
} else if (score >= 80) {
  console.log("B");
} else {
  console.log("C");
}

// Ternary
let result = score >= 50 ? "Pass" : "Fail";
console.log(result);

// Switch
let color = "red";
switch (color) {
  case "red": console.log("Stop"); break;
  case "green": console.log("Go"); break;
  default: console.log("Wait");
}
```

**Learn more:** [MDN Conditionals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#conditional_statements)

Navigation:
[⬅️ Arrays](#arrays) | [⬅️ Home](#) | [➡️ Events →](#events)

---

<a name="events"></a>

## 🖱️ Events

**Explanation:**
Events respond to user interactions (clicks, keypresses, form submissions, etc.).

```html
<button id="btn">Click Me</button>
<script>
  document.getElementById("btn").addEventListener("click", () => {
    alert("Button clicked!");
  });
</script>
```

**Learn more:** [MDN Events](https://developer.mozilla.org/en-US/docs/Web/Events)

Navigation:
[⬅️ Conditionals](#conditionals) | [⬅️ Home](#) | [➡️ Functions →](#functions)

---

<a name="functions"></a>

## ⚙️ Functions

**Explanation:**
Functions are reusable blocks of code.

```javascript
// Function declaration
function greet(name) {
  return `Hello, ${name}`;
}

// Function expression
const greet2 = function(name) {
  return `Hi, ${name}`;
};

// Arrow function
const greet3 = name => `Hey, ${name}`;

console.log(greet("Amine"));
console.log(greet2("Amine"));
console.log(greet3("Amine"));
```

**Learn more:** [MDN Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

Navigation:
[⬅️ Events](#events) | [⬅️ Home](#) | [➡️ JSON →](#json)

---

<a name="json"></a>

## 📄 JSON

**Explanation:**
JSON (JavaScript Object Notation) is a text format for storing and transmitting data.

```javascript
// JSON string
let jsonString = '{"name":"Amine","age":25}';

// Convert JSON string to object
let obj = JSON.parse(jsonString);
console.log(obj.name); // "Amine"

// Convert object to JSON string
let str = JSON.stringify(obj);
console.log(str);
```

**Learn more:** [MDN JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)

Navigation:
[⬅️ Functions](#functions) | [⬅️ Home](#) | [➡️ Loops →](#loops)

---

<a name="loops"></a>

## 🔁 Loops

**Explanation:**
Loops execute code repeatedly while a condition is true.

```javascript
// For loop
for (let i = 0; i < 3; i++) {
  console.log(i);
}

// While loop
let count = 0;
while (count < 3) {
  console.log(count);
  count++;
}

// Do...while
let num = 0;
do {
  console.log(num);
  num++;
} while (num < 3);

// For...of (arrays)
for (let fruit of ["apple", "banana"]) {
  console.log(fruit);
}

// For...in (objects)
let person = {name: "Amine", age: 25};
for (let key in person) {
  console.log(key, person[key]);
}
```

**Learn more:** [MDN Loops and iteration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

Navigation:
[⬅️ JSON](#json) | [⬅️ Home](#) | [➡️ Math →](#math)

---

<a name="math"></a>

## 🧮 Math

**Explanation:**
The `Math` object provides mathematical constants and functions.

```javascript
console.log(Math.max(1, 5, 10));   // 10
console.log(Math.min(1, 5, 10));   // 1
console.log(Math.random());        // random between 0 and 1
console.log(Math.floor(4.9));      // 4
console.log(Math.ceil(4.1));       // 5
console.log(Math.round(4.5));      // 5

let x = 5;
x++; // increment
x--; // decrement
```

**Learn more:** [MDN Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

Navigation:
[⬅️ Loops](#loops) | [⬅️ Home](#) | [➡️ Object Basics →](#object-basics)

---

<a name="object-basics"></a>

## 🗂️ Object Basics

**Explanation:**
Objects store data as key-value pairs.

```javascript
let person = {
  name: "Amine",
  age: 25,
  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
};

console.log(person.name);
person.city = "Berlin";
delete person.age;
person.greet();
```

**Learn more:** [MDN Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

Navigation:
[⬅️ Math](#math) | [⬅️ Home](#) | [➡️ Strings →](#strings)

---

<a name="strings"></a>

## 🔤 Strings

**Explanation:**
Strings are sequences of characters.

```javascript
let str = " Hello World ";

console.log(str.length);                // 13
console.log(str.toUpperCase());         // " HELLO WORLD "
console.log(str.toLowerCase());         // " hello world "
console.log(str.trim());                // "Hello World"
console.log(str.includes("World"));     // true
console.log(str.indexOf("World"));      // 7
console.log(str.slice(1, 5));           // "Hell"
console.log(str.replace("World", "JS")) // " Hello JS "
console.log("a,b,c".split(","));        // ["a", "b", "c"]
```

**Learn more:** [MDN Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

Navigation:
[⬅️ Object Basics](#object-basics) | [⬅️ Home](#) | [➡️ OOP in JavaScript →](#oop-in-javascript)

---

<a name="oop-in-javascript"></a>

## 🏛️ OOP in JavaScript

**Explanation:**
JavaScript supports Object-Oriented Programming using **classes**, **constructors**, and **prototypes**.

```javascript
// Class syntax
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, I'm ${this.name}, ${this.age} years old.`);
  }
}

let p1 = new Person("Amine", 25);
p1.greet();

// Inheritance
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age);
    this.grade = grade;
  }

  study() {
    console.log(`${this.name} is studying in grade ${this.grade}.`);
  }
}

let s1 = new Student("Lina", 20, "A");
s1.greet();
s1.study();
```

**Learn more:** [MDN Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

Navigation:
[⬅️ Strings](#strings) | [⬅️ Home](#) | [➡️ How to Use This Sheet →](#how-to-use-this-sheet)

---

<a name="how-to-use-this-sheet"></a>

## 📌 How to Use This Sheet

1. Review each section before taking the **JavaScript skill tests**.
2. Run the examples in your browser console or Node.js to understand behavior.
3. Modify examples to explore variations.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

**Author:** Zaouga Amine
**Date:** August 2025
**Purpose:** Part of my GitHub JavaScript Knowledge Repository

