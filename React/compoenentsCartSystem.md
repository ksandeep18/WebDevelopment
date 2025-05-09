## 🧱 Step 6: Components - Designing a Shopping Cart System

In this section, we'll begin creating components for a shopping cart system like Amazon or Flipkart.

### 🎯 Goal:
Design a simple shopping cart interface using React components.

---

### ✅ Step 1: Create a New React Project

Open your terminal or CMD and run:

```bash
npx create-react-app cart-app
```

Navigate into your project folder and start the development server:

```bash
cd cart-app
npm start
```

This will start your app at `http://localhost:3000`.

---

### ✅ Step 2: Open the Project in VS Code

- Launch **Visual Studio Code**.
- Open the folder `cart-app` that you just created.

---

### ✅ Step 3: Install Bootstrap

You can either:

🔹 **Option A: Install via npm**  
```bash
npm install bootstrap
```

Then import Bootstrap CSS into your `index.js`:

```js
import 'bootstrap/dist/css/bootstrap.css';
```

🔹 **Option B: Use CDN**  
Paste the CDN link inside the `<head>` tag of `public/index.html`:

```html
<link
  rel="stylesheet"
  href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
/>
```

---

### ✅ Step 4: Create Your First Component

1. In the `src` folder, create a folder named `components`.
2. Inside `components`, create a file named `Counter.jsx`.

Use VS Code shortcuts to scaffold the component:

- Type `imrc` → Press `Tab`: Auto-import React.
- Type `cc` → Press `Tab`: Create a class component.

Rename the class to something meaningful like `Counter`.

```js
// Counter.jsx
import React, { Component } from "react";

class Counter extends Component {
  render() {
    return <h1>Hello from Counter Component!</h1>;
  }
}

export default Counter;
```

> 📝 For now, skip defining the `state` variable.

---

### ✅ Step 5: Use the Component in `index.js`

Go to `src/index.js` and import your new component:

```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import 'bootstrap/dist/css/bootstrap.css';
import Counter from './components/Counter';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Counter />);
```

Now when you run the app, it should display:
```
Hello from Counter Component!
```

---

