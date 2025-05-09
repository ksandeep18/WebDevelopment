
## 📁 Part 3: Understanding Files & Folders in Create React App

When you create a React app using `create-react-app`, it sets up everything you need for a React development environment. Here's a breakdown of the key files and folders:

### 🚀 Development Server, Webpack, and Babel

- Running `npx create-react-app my-app` installs a development server, **Webpack**, and **Babel**:
  - **Webpack** bundles your code and assets.
  - **Babel** converts modern JavaScript (ES6+) and JSX into browser-compatible JavaScript.

To start your app:

```bash
cd my-app
npm start
```

This launches a local development server at [http://localhost:3000](http://localhost:3000).

---

### 🗂️ Important Folders and Files

#### 📂 `public/`
- Contains **static assets** that are not processed by Webpack.
- Key file: `index.html`
  - This is the single HTML file React injects content into.
  - Inside the `<body>`, there's a `<div id="root"></div>` — this is the **root container** where your entire React app is rendered.

#### 📂 `src/`
- This is where your actual React app code lives.
- Key files:
  - `App.js`: A basic React **component** (initially using ES6 class or function).
    - Uses **JSX syntax** to describe UI.
    - JSX is not understood by browsers, so **Babel** converts it into plain JavaScript.
  - `index.js`: **Entry point** of the application.
    - Renders the root component (`App`) into the `#root` element in `index.html`.
  - `registerServiceWorker.js`: Optional file for enabling offline support (created automatically in older versions).

> 🧠 In React, components are usually written in JSX and are either **functions or ES6 classes**.

---

