
# 🌐 HTML Notes for Placement Prep

---

## 🧭 0. Index / Navigation

1. [HTML Basics](#1-html-basics)
2. [HTML Forms (Detailed)](#2-html-forms-detailed)

---

## 📘 1. HTML Basics

HTML stands for **HyperText Markup Language** and is used to build the structure of web pages. It helps in displaying text, images, videos, audio, and links on the web. To start writing HTML, it's common to use an editor like **Visual Studio Code (VSCode)**. After downloading VSCode, create a folder for your project and begin by making a file named **index.html**, which is usually the homepage.

To improve workflow, install the **Live Server** extension in VSCode. It helps you see changes in the browser live as you edit your HTML file. A basic HTML document structure includes tags like `<html>`, `<head>`, and `<body>`.

To add **links**, use the `<a>` tag with an `href` attribute. For example, `<a href="https://google.com">Google</a>`. To open links in a new tab, use `target="_blank"`.

To add **images**, use the `<img>` tag with `src` and `alt` attributes:  
`<img src="cat.jpg" alt="A cute cat">`. You can control size using `width` and `height`.

To add **audio**, use the `<audio controls>` tag with a `<source>` inside. Similarly, for **video**, use the `<video controls>` tag with `<source>`.

A **favicon** is the small icon in the browser tab, added using `<link rel="icon" href="favicon.png">` in the `<head>`.

For **text formatting**, use tags like `<b>` or `<strong>` for bold, `<i>` or `<em>` for italic, `<u>` for underline. Use `<br>` for line breaks and `<hr>` for horizontal lines.

The **`<div>`** is used to group block elements, and **`<span>`** is used for inline content. These help with layout and styling.

To make **lists**, use `<ol>` for ordered lists and `<ul>` for unordered lists. List items go inside `<li>` tags. You can also use `<dl>`, `<dt>`, and `<dd>` for description lists.

To create **tables**, use `<table>`, with `<tr>` for rows, `<th>` for headers, and `<td>` for data cells.

For **buttons**, you can use `<button>` or `<input type="button">`. These can perform actions or submit forms.

---

## 📝 2. HTML Forms (Detailed)

HTML **forms** are used to collect user input. Forms are defined using the `<form>` tag and commonly include fields like text boxes, passwords, checkboxes, and buttons.

The **`action`** attribute specifies where the form data should be sent after submission. The **`method`** attribute controls how data is sent:

- **`GET`**: Sends data via the URL. Best for non-sensitive data like search queries.
- **`POST`**: Sends data in the request body. Safer for sensitive or large data, like login forms or file uploads.

For uploading large files, use **`enctype="multipart/form-data"`** in the form tag.

Use the **`<label>`** tag to describe input fields. Link them using the **`for`** attribute (which matches the `id` of the input). This improves accessibility and UX.

### 🔢 Common Input Types

- **`text`**: For basic text input  
- **`password`**: Hides the characters  
- **`email`**: Validates for email format  
- **`tel`**: For phone numbers  
- **`date`**: Date picker  
- **`number`**: Only numbers allowed  
- **`radio`**: Choose one from a group. Use the same `name` for grouping  
- **`checkbox`**: Allows multiple selections  
- **`file`**: For file uploads. Use `accept` to limit file types (e.g., `accept=".jpg,.png"`)

### ⬇️ Select, Option, and Others

- **`<select>`**: Creates a dropdown list  
- **`<option value="">`**: Represents each item in the dropdown  
- **`<textarea>`**: For multi-line input. Customize with `rows` and `cols`

### 🏷️ Useful Attributes

- **`required`**: Field must be filled out
- **`minlength` and `maxlength`**: Limits input length (**inclusive**)  
- **`pattern`**: Defines regex for allowed input  
- **`value`**: Sets default value  
- **`placeholder`**: Shows a hint in the field  
- **`readonly`**: Prevents editing  
- **`disabled`**: Disables the field completely

### 🔘 Buttons in Forms

- **Submit Button**: Sends form data (`<input type="submit">`)
- **Reset Button**: Resets form fields to default (`<input type="reset">`)
- **Custom Button**: With JavaScript (`<button type="button">Click</button>`)

These tags and attributes help make powerful and accessible forms for any website. Understanding them well is key for web development and placements.

---
