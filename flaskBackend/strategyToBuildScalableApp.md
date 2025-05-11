
# 🔥 Scalable Flask Project Structure + Common Mistakes

## ✅ Recommended Folder Layout (Application Factory Pattern)

```
/your_project
├── app/
│   ├── __init__.py       # create_app() initializes app
│   ├── routes/           # Blueprints: auth.py, main.py, etc.
│   ├── models.py         # SQLAlchemy models
│   ├── services/         # Business logic layer
│   └── extensions.py     # db, migrate, jwt, etc.
├── config.py             # Dev/Test/Prod config
├── run.py                # Entry point
├── .env                  # Secrets & environment variables
└── tests/                # Test cases
```

---

## ⚠️ Common Beginner Errors & Fixes

### 1. Missing App Factory or Blueprint Registration
- ❌ All logic in `app.py`
- ✅ Use `create_app()` + `app.register_blueprint()`

### 2. Circular Imports
- ❌ Importing models/routes too early
- ✅ Use centralized `extensions.py`

### 3. No Blueprints (Poor Structure)
- ❌ Routes in one file
- ✅ Separate by feature in `routes/`

### 4. Hardcoded Secrets/DB URI
- ❌ `SECRET_KEY = 'abc'`
- ✅ Use `.env` + `os.environ.get()`

### 5. No Error Handlers
- ❌ No feedback on 404/500
- ✅ Add custom `@app.errorhandler()`

### 6. No Testing Setup
- ❌ No `tests/`
- ✅ Use `pytest`, Flask test client

---

## 🧠 Best Practices Recap

| Practice                   | Benefit                           |
|---------------------------|-----------------------------------|
| App Factory Pattern        | Modular, scalable, testable       |
| Blueprints per feature     | Clean separation of concerns      |
| Config class + .env        | Secure, flexible config           |
| Logging + error handling   | Easier debugging & maintenance    |
| Testing with pytest        | Reliability & refactor-safe code  |

---

