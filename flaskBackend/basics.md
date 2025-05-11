
# Flask Backend Development Notes 

## 📌 1. Flask Basics: Understanding Execution Flow

### Key Concept: HTML Form Submission Flow (form.html)
- **Form submits to a Flask route (`/login`) using POST.**
- Flask executes routes based on the method defined (`@app.route('/login', methods=['POST'])`).
- `request.form` fetches data submitted via form.
- Response: `render_template()` returns an HTML page OR `redirect()` navigates to another route.

### Beginner Stumbles:
- Mixing up `request.form` vs `request.args` (form is for POST, args is for GET params).
- Forgetting to use `method="POST"` in the `<form>` tag.

---

## 🧠 2. Sessions in Flask

### Key Concept: Flask `session` is a dictionary stored client-side (in a cookie), not a stack!
- Use `session['user'] = name` to store info.
- Use `session.pop('user')` or `session.clear()` to log out.

### Beginner Stumbles:
- Assuming session behaves like a stack (LIFO). It doesn’t. It's just key-value storage.
- Not setting `app.secret_key` leads to session not working!

---

## 🏗️ 3. Scalable Flask Project Structure

```
myapp/
│
├── app/
│   ├── __init__.py       # Initializes app, DB, Blueprints
│   ├── routes/           # Blueprint folders
│   │   └── main.py       # Route handlers
│   ├── models.py         # SQLAlchemy models
│   └── templates/        # HTML Templates (if any)
│
├── run.py                # Entry point
└── config.py             # Config variables
```

### Beginner Stumbles:
- Not using Blueprints, leading to bloated `app.py`.
- Forgetting to import/register Blueprints in `__init__.py`.

---

## 🌐 4. REST APIs with Flask

### Key Concepts:
- REST API = Structured way to define endpoints that return **JSON**.
- Uses HTTP methods: GET, POST, PUT, DELETE.
- Example: `/api/tasks` → returns JSON instead of HTML.

### Route Example:
```python
@app.route('/api/tasks', methods=['POST'])
def create_task():
    data = request.get_json()
    new_task = Task(title=data['title'])
    db.session.add(new_task)
    db.session.commit()
    return jsonify({'id': new_task.id}), 201
```

### Beginner Stumbles:
- Using `request.form` instead of `request.get_json()` in APIs.
- Not returning proper HTTP status codes (`201`, `404`, etc.).
- Forgetting `Content-Type: application/json` when using Postman.

---

## 🔁 REST vs Traditional Web App

| Feature            | Traditional Flask App       | REST API Style             |
|-------------------|-----------------------------|----------------------------|
| Output            | HTML (`render_template`)    | JSON (`jsonify`)           |
| Data Input        | `request.form`              | `request.get_json()`       |
| Frontend          | Browser forms               | React, Vue, Mobile         |
| Session/Auth      | `session` based             | Often uses JWT             |

---

## ✅ Recommendations for Beginners

- Start small: Make a REST API with 2–3 routes.
- Use Postman for testing. Learn to send JSON in body.
- Learn about HTTP methods and status codes.
- Avoid mixing REST API logic with HTML rendering.

---

## 🧰 Useful Libraries

- `Flask-CORS`: Allow frontend (React/Vue) to access Flask APIs.
- `Flask-SQLAlchemy`: ORM for database access.
- `Flask-Marshmallow`: Data validation/serialization.

---

