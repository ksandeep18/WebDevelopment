
# ⚙️ TypeScript Setup and Debugging - Part 3

This part explains how to create a TypeScript project from scratch, configure the compiler, and set up debugging in **Visual Studio Code (VS Code)**.

---

## 🛠️ Step 1: Create a TypeScript Project

### Open Command Prompt and run:
```bash
cd Desktop
mkdir typescriptPractice
cd typescriptPractice
code .
```
> This opens VS Code in the new folder.

---

## 📄 Step 2: Create Your First TypeScript File

Inside the VS Code editor:
1. Create a file named `index.ts`.
2. Add some basic TypeScript code:
```ts
let userName: string = "Sandeep";
let age: number = 25;

console.log(`Hello, ${userName}. You are ${age} years old.`);
```

---

## ⚙️ Step 3: Initialize and Configure TypeScript Compiler

### In Terminal:
```bash
tsc --init
```
> This command generates a `tsconfig.json` file with default compiler settings.

---

## ✏️ Step 4: Modify `tsconfig.json`

Make the following changes:

```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "sourceMap": true,
    "noEmitOnError": true,
    "strict": true
  }
}
```

### Explanation:
- `"rootDir"`: Tells TypeScript where `.ts` files are located (e.g., `src` folder).
- `"outDir"`: Tells it where to output the compiled `.js` files (e.g., `dist` folder).
- `"sourceMap"`: Generates `.map` files to help debug TypeScript in JS.
- `"noEmitOnError"`: Stops compilation if there's a TypeScript error.

---

## 🧱 Step 5: Folder Structure

Organize your files like this:
```
typescriptPractice/
│
├── src/
│   └── index.ts
│
├── dist/
├── tsconfig.json
```

To compile:
```bash
tsc
```

---

## 🐞 Step 6: Set Up Debugging in VS Code

1. Go to the **Run and Debug** tab in VS Code.
2. Click **create a launch.json file**.
3. Choose **Node.js** as the environment.

This creates a `.vscode/launch.json` file.

### Default `launch.json`:
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/dist/index.js"
    }
  ]
}
```

---

## ⛓️ Step 7: Add Prelaunch Task

To automatically compile TypeScript before debugging, add this to `launch.json`:
```json
"preLaunchTask": "tsc: build - tsconfig.json"
```

### Updated `launch.json`:
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/dist/index.js",
      "preLaunchTask": "tsc: build - tsconfig.json"
    }
  ]
}
```

---

## ▶️ Step 8: Debug Your Code

1. Click the green **Run** button in the Debug tab.
2. VS Code will:
   - Compile your TypeScript (`tsc` runs).
   - Launch the compiled JS file from the `dist/` folder.
   - Open the debugger to set breakpoints, inspect variables, and step through your code.

---

## 🏁 Summary

- You created a TypeScript project with a proper folder structure.
- Configured `tsconfig.json` for custom build settings.
- Set up VS Code debugging with `launch.json`.
- Linked TypeScript compilation as a **pre-launch task**.
- Learned how to debug `.ts` code using `.map` files in VS Code.

