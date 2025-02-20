# JavaScript-Interview
---

## Differences between Java and JavaScript

### 1. Java:
- Java is a general-purpose, object-oriented programming language.
- It is a compiled language.
- Java is commonly used for server-side applications, desktop applications, and mobile applications.
- Java uses classes and objects as the primary units.

### 2. JavaScript:
- JavaScript is a client-side scripting language.
- It is an interpreted language, which means the code is executed directly by the browser or runtime environment without a compilation step.
- JavaScript is mainly used for web development to create dynamic content on websites.
---
### 3. Primitive Data Types in JavaScript
The predefined data types provided by JavaScript are known as primitive data types:
- Numbers
- Strings
- Boolean
- Symbol
- Undefined
- Null
- BigInt

### 4. Non-Primitive Data Types in JavaScript
Data types derived from primitive data types are known as non-primitive data types:
- Objects
- Functions
- Arrays
- --
### 5. What is the use of the `isNaN` function?
The `isNaN()` function in JavaScript is used to determine if a value is NaN (Not-a-Number). It returns a boolean value: `true` if the value is NaN and `false` if the value is a valid number.

---

### 6. What is negative infinity?
Negative infinity is a constant value that represents the lowest available value. It means that no other number is lesser than this value.

---

### 7. Which company developed JavaScript?
Netscape developed JavaScript, and it was created by Brendan Eich in the year 1995.

---

### 8. What are global variables?
Global variables are variables that are defined outside of functions. These variables have a global scope, so they can be used by any function without passing them as parameters.
- It is difficult to debug and test the code that relies on global variables.
- ---
### 9. What do you mean by `null` in JavaScript?
`null` is a primitive data type in JavaScript that represents the intentional absence of a value or object.

---
### 10. What is the `this` keyword in JavaScript?
The `this` keyword in JavaScript refers to the context in which the function is called. It can represent different things depending on how a function is invoked.

---
###  11. Difference Between ViewState and SessionState

**Scope**: ViewState is page-specific, whereas SessionState is session-specific (across multiple pages).

**Storage Location**: ViewState is stored on the client-side, and SessionState is stored on the server-side.

**Duration**: ViewState lasts only for the duration of the page lifecycle (until the page is reloaded or navigated), while SessionState lasts as long as the user’s session persists (until the browser is closed or the session expires).

---

### 12. What is a template literal in JavaScript?
A template literal in JavaScript is a way to define strings that allow embedded expressions and multi-line formatting. It uses backticks (``) instead of quotes and supports `${}` for embedding variables or expressions inside the string.

---
### 13. What is a higher-order function in JavaScript?
A higher-order function is a function that either takes one or more functions as arguments or returns a function as its result. These functions enable functional programming patterns.

#### Example:
```js
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8]
```
---
### 14. What is called Variable typing in JavaScript ? 
The variable typing is the type of variable used to store a number and using that same variable to assign a “string”.
```js
let value = 42;
value = "GeeksforGeeks"; // Allowed in JavaScript
```
---
### 15. What is hoisting in JavaScript? 
Hoisting in JavaScript behavior in which you can reference variables and functions before they are declared in the code. However, only declarations are hoisted, not initializations.

---
### 16. How to convert the string of any base to integer in JavaScript? 
In JavaScript, parseInt() function is used to convert the string to an integer.

---
### 17. What is the use of void(0) ? 
The void(0) is used to call another method without refreshing the page during the calling time parameter “zero” will be passed.

---
### 18. What are the types of popup boxes available in JavaScript?
1. `alert()` – Displays an alert message.
2. `confirm()` – Displays a confirmation dialog.
3. `prompt()` – Allows user input.

---
### 19. What are JavaScript modules, and how do you import/export them?
JavaScript modules allow you to split your code into smaller, reusable pieces. They enable the export of variables, functions, or objects from one file and the import of them into another. To export an element, you use export (either named or default). To import it, you use import.

**Example:**
```js
// In file1.js
export const greet = () => "Hello";

// In file2.js
import { greet } from './file1.js';
console.log(greet()); // Outputs: Hello
```
----
### 20. What are WeakMap and WeakSet, and how are they different from Map and Set?
 A WeakMap is a collection of key-value pairs where keys are objects and the values can be any data type lincluding (function and object) The key-value pairs in a WeakMap are “weakly” held, meaning if no other references to a key exist, the entry can be garbage collected. 
 
 A WeakSet is a collection of unique objects, and like WeakMap, the objects are weakly held. 

The main difference from Map and Set is that in Map and Set, entries are strongly held, meaning they prevent garbage collection, while in WeakMap and WeakSet, entries can be garbage collected if no other references to the objects exist.

---
### 21.  What is async/await in javascript What is async? 
The async keyword is used to define a function as asynchronous. An asynchronous function always returns a promise, whether you explicitly return a promise or return a value directly. When a function is marked as async, it can contain await expressions inside it. 

#### What is await? 

The await keyword can only be used inside an async function. It is used to pause the execution of the asynchronous function until the promise is resolved (either fulfilled or rejected). Essentially, await makes asynchronous code look and behave like synchronous code. 

 - When await is used, it waits for the promise to resolve or reject before continuing the execution of the code that follows it.
 - If the promise is resolved, the result is returned. 
 - If the promise is rejected, it throws an error, which can be caught using try/catch.
 
 
**Example:**
```js
async function fetchData() {
  let response = await fetch("https://api.example.com/data");
  let data = await response.json();
  console.log(data);
}
fetchData();
```
