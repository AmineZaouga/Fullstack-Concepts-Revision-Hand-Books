# Fullstack-Concepts-Revision-Hand-Books
This Project is For Sharing Revision Hand Books For Main Concepts and Notions Every Fullstack Engineer Should Know.


# 📖 JavaScript Skill Test – Complete Revision Sheet

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)](#)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

> A complete, **one-stop revision file** for JavaScript skill test topics.  
> Includes **clear explanations**, **icons**, and **code examples** for each subject.  
> Now with **emoji navigation** 🚀  

---

## 📚 Table of Contents
1. [📦 Variables](#1-variables)
2. [🍏 Arrays](#2-arrays)
3. [🔀 Conditionals](#3-conditionals)
4. [🖱️ Events](#4-events)
5. [⚙️ Functions](#5-functions)
6. [📄 JSON](#6-json)
7. [🔁 Loops](#7-loops)
8. [🧮 Math](#8-math)
9. [🗂️ Object Basics](#9-object-basics)
10. [🔤 Strings](#10-strings)
11. [🏛️ OOP in JavaScript](#11-oop-in-javascript)
12. [📌 How to Use This Sheet](#-how-to-use-this-sheet)

---

## 1. 📦 Variables

**Explanation:**  
Variables store data values.  
- `let` → block-scoped, reassignable.  
- `const` → block-scoped, **not** reassignable.  
- `var` → function-scoped (avoid in modern code).

let age = 25;       // can be changed
const PI = 3.1416;  // cannot be changed
var name = "Amine"; // old syntax, avoid if possible

age = 26;           // ✅ works
// PI = 3.14;       // ❌ error
Navigation: ⬅️ None | 🏠 Home | ➡️ Arrays →

2. 🍏 Arrays
Explanation:
Arrays hold multiple values in a single variable.


let fruits = ["apple", "banana", "cherry"];

console.log(fruits[0]); // "apple"
fruits.push("orange");  // add at the end
fruits.pop();           // remove last element
fruits.unshift("kiwi"); // add at the start
fruits.shift();         // remove first element

// Iterating
fruits.forEach(fruit => console.log(fruit));
Navigation: ⬅️ Variables | 🏠 Home | ➡️ Conditionals →

3. 🔀 Conditionals
Explanation:
Conditionals execute code blocks based on conditions.


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
Navigation: ⬅️ Arrays | 🏠 Home | ➡️ Events →

4. 🖱️ Events
Explanation:
Events respond to user interactions (clicks, keypresses, form submissions, etc.).


<button id="btn">Click Me</button>
<script>
  document.getElementById("btn").addEventListener("click", () => {
    alert("Button clicked!");
  });
</script>
Navigation: ⬅️ Conditionals | 🏠 Home | ➡️ Functions →

5. ⚙️ Functions
Explanation:
Functions are reusable blocks of code.

javascript
Copier
Modifier
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
Navigation: ⬅️ Events | 🏠 Home | ➡️ JSON →

6. 📄 JSON
Explanation:
JSON (JavaScript Object Notation) is a text format for storing and transmitting data.


// JSON string
let jsonString = '{"name":"Amine","age":25}';

// Convert JSON string to object
let obj = JSON.parse(jsonString);
console.log(obj.name); // "Amine"

// Convert object to JSON string
let str = JSON.stringify(obj);
console.log(str);
Navigation: ⬅️ Functions | 🏠 Home | ➡️ Loops →

7. 🔁 Loops
Explanation:
Loops execute code repeatedly while a condition is true.


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
Navigation: ⬅️ JSON | 🏠 Home | ➡️ Math →

8. 🧮 Math
Explanation:
The Math object provides mathematical constants and functions.


console.log(Math.max(1, 5, 10));   // 10
console.log(Math.min(1, 5, 10));   // 1
console.log(Math.random());        // random between 0 and 1
console.log(Math.floor(4.9));      // 4
console.log(Math.ceil(4.1));       // 5
console.log(Math.round(4.5));      // 5

let x = 5;
x++; // increment
x--; // decrement
Navigation: ⬅️ Loops | 🏠 Home | ➡️ Object Basics →

9. 🗂️ Object Basics
Explanation:
Objects store data as key-value pairs.


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
Navigation: ⬅️ Math | 🏠 Home | ➡️ Strings →

10. 🔤 Strings
Explanation:
Strings are sequences of characters.


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
Navigation: ⬅️ Object Basics | 🏠 Home | ➡️ OOP →

11. 🏛️ OOP in JavaScript
Explanation:
JavaScript supports Object-Oriented Programming using classes, constructors, and prototypes.


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
Navigation: ⬅️ Strings | 🏠 Home | ➡️ How to Use →

📌 How to Use This Sheet
Review each section before taking the JavaScript skill tests.

Run the examples in your browser console or Node.js to understand behavior.

Modify examples to explore variations.

Navigation: ⬅️ OOP | 🏠 Home | ➡️ None

Author: Zaouga Amine
Date: August 2025
Purpose: Part of my GitHub JavaScript Knowledge Repository

