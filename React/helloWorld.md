

## 📝 Part 4: Writing Your First React Program – Hello World

Once you've understood the folder structure, let's clean it up and write a simple React program from scratch.

### 🧹 Step 1: Clean the `src` Folder

- Go to the `src/` folder and **delete all the existing files**.
- Create a new file called `index.js`.

---

### ✍️ Step 2: Write the Hello World Program

Here's the code snippet for your first React program:

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const message = "Hello, World!";

ReactDOM.render(
  <h1>{message}</h1>,
  document.getElementById('root')
);
```

---

### 📌 Understanding the Code

- **`import React`**: Required to use JSX.
- **`import ReactDOM`**: Allows you to render React components into the DOM.
- **`const message`**: We use `const` to define a constant variable (other options: `let`, `var`).
- **`<h1>{message}</h1>`**: JSX syntax used to render HTML inside JavaScript.
- **`ReactDOM.render()`**: This renders the JSX (virtual DOM) into the actual browser DOM inside the element with `id="root"` from `index.html`.

---

### 🔁 How React Works

- React maintains a **Virtual DOM** — a lightweight copy of the real DOM.
- When your data (`state`) changes, React **reacts** by:
  1. Updating the Virtual DOM.
  2. Comparing it with the previous version (using a **diffing algorithm**).
  3. Updating only the changed parts in the **real DOM** — this makes React fast and efficient.

> ⚛️ React is fast because it avoids full page reloads and performs **minimal DOM manipulation** using the Virtual DOM.

---

🎉 Congratulations! You just wrote your first React app. Next, we'll explore **JSX deeper and how to pass data using Props**.
