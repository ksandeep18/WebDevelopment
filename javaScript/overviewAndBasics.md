# 📝 JavaScript Notes 

## ⚙️ JavaScript Engines and Environment
- **V8 Engine**: Used by Chrome and written in C++. It powers JavaScript execution inside browsers.
- **Node.js**: Allows JavaScript to run outside the browser. It is built on top of the V8 engine and written in C++.

## 🧪 First JavaScript Program
1. Open **VS Code** and create a `.js` file.
2. Write your first program:
   ```js
   console.log("Hello, JavaScript!");
   ```
3. In a webpage, add your JS at the **bottom of the HTML** using `<script>` tag to allow the page content to load first.
4. Use **Live Server** to open the page and view logs in the **browser console**.
5. You can also debug JavaScript using the **Sources** tab in browser dev tools.

## 🧮 Variables and Data Types
- Declare using: `let`, `const`, `var`
- Use `typeof(variable)` to check the type.
- JS is **dynamically typed** – the variable type can change.

### Primitive Types:
- `boolean`, `number`, `string`, `undefined`, `null`

### Reference Types:
- `object`, `array`, `function`
- These copy **references**, not values.
- Mutating a reference type (e.g., object) affects the original.

```js
let course = {}; // object
let nums = [1, 2, 3]; // array
```

## 🔄 Value vs Reference
- Primitives: copy the **value**.
- Reference Types: copy the **memory address**.

## 🧠 Functions in JavaScript
- Declaring functions in multiple ways:
```js
function greet() { }
const greet = function() { };
const greet = () => { };
```

- Functions are **first-class citizens**: can be
  - assigned to variables,
  - passed as arguments,
  - returned from other functions.

### Higher-Order Function
A function that takes another function as argument or returns it.
```js
function operate(a, b, fn) {
  return fn(a, b);
}
```

### Arrow Function (ES6+)
```js
const add = (a, b) => a + b;
```

## 🔁 Hoisting and Execution
- **Hoisting**: JS moves declarations (not initializations) to the top of their scope.
- You can access variables and functions before their declaration (var and function only).

## ⚙️ Execution Context (EC)
- Created for every function call and the global scope.
- Two phases:
  1. **Memory phase** – variables/functions are stored (undefined/functions).
  2. **Code phase** – line-by-line execution.

- **Call Stack** manages ECs.
- JS is **synchronous** and **single-threaded**.

## 🪟 `window` and `this`
- In browsers, `window` is the global object.
- `this` refers to `window` in global context.

## 🛑 var vs let vs const
- `var` is **function scoped**.
- `let` and `const` are **block scoped**.
- Avoid using `var` due to hoisting issues and **Temporal Dead Zone (TDZ)**.

## 🔒 Scope and Lexical Scope
- Lexical scope: Functions can access variables from their parent (outer) scope.
```js
function outer() {
  let outerVar = 10;
  function inner() {
    console.log(outerVar); // accessible due to lexical scoping
  }
  inner();
}
```

## 🔐 Closures
- A closure is created when a function remembers variables from its **lexical scope**, even when executed outside that scope.

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}

const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```
