# 🌐 HTML

### 📌 What is HTML?
**HTML** (HyperText Markup Language) is the standard language used to **create and structure webpages**.

---

## 🧱 Basic Structure of an HTML Document

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Website</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is my first webpage.</p>
  </body>
</html>
```

| Tag          | Purpose                               |
|---------------|----------------------------------------|
| `<!DOCTYPE>`  | Declares the HTML version              |
| `<html>`      | Root element                           |
| `<head>`      | Metadata (not displayed on the page)   |
| `<title>`     | Title shown on the browser tab         |
| `<body>`      | Visible page content                   |

---

## 🔤 Text Formatting Tags

```html
<h1>This is Heading 1</h1>
<p>This is a <strong>bold</strong> and <em>italic</em> paragraph.</p>
<a href="https://example.com">Visit Example</a>
```

| Tag        | Use                            |
|------------|---------------------------------|
| `<h1>`–`<h6>` | Headings                    |
| `<p>`      | Paragraph                      |
| `<br>`     | Line break                     |
| `<hr>`     | Horizontal line                |
| `<strong>` | Bold text                      |
| `<em>`     | Italic text                    |
| `<a href="">` | Link to another page       |

---

## 📋 Lists

### 🔹 Unordered List
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

### 🔸 Ordered List
```html
<ol>
  <li>First</li>
  <li>Second</li>
</ol>
```

---

## 🖼️ Images and Media

```html
<img src="image.jpg" alt="My Image" width="200">
<video controls width="300">
  <source src="video.mp4" type="video/mp4">
</video>
```

---

## 🧾 Forms (User Input)

```html
<form action="/submit" method="post">
  <label>Username:</label>
  <input type="text" name="username">
  <input type="submit" value="Submit">
</form>
```

| Element          | Description            |
|------------------|------------------------|
| `<form>`         | Defines a form         |
| `<input>`        | Input field            |
| `<label>`        | Text label             |
| `method="post"`  | Send data via POST     |

---

## 🧩 Div and Span

```html
<div style="background: lightgray;">
  <p>This is in a div.</p>
</div>
<span style="color: blue;">Inline text</span>
```

| Tag     | Use                          |
|---------|------------------------------|
| `<div>` | Block container              |
| `<span>`| Inline container             |

---

## 📊 Tables

```html
<table border="1">
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>23</td>
  </tr>
</table>
```

| Tag     | Use                  |
|---------|-----------------------|
| `<table>` | Table element       |
| `<tr>`    | Table row           |
| `<th>`    | Header cell         |
| `<td>`    | Data cell           |

---

## 🎨 Adding CSS (Styling HTML)

### Inline CSS
```html
<p style="color: red; font-size: 20px;">Styled Text</p>
```

### External CSS
```html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

---

## 🧠 JavaScript in HTML

```html
<button onclick="alert('Hello!')">Click Me</button>
```

---

## ✅ Summary

HTML builds the **structure** of your website:
- Headings, paragraphs, links
- Images, videos, and media
- Forms for user input
- Tables, lists, and layout containers
- Inline and external styling
- JavaScript for interactivity

---

