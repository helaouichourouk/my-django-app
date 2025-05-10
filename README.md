```markdown
# 🐍 Django + Docker + venv Starter

A minimal example of running a Django project with:

- ✅ Local development using Python virtual environment (`venv`)
- 🐳 Docker support for containerized deployment
- 🛠️ Simple setup with `docker-compose`

---

## 📁 Project Structure

```
my-django-app/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── .dockerignore
├── .gitignore
├── myproject/
│   ├── manage.py
│   └── myproject/
│       ├── settings.py
│       ├── urls.py
│       └── ...
└── venv/  ← for local dev (ignored in Docker & Git)
```

---

## ⚙️ Requirements

- Python 3.10+
- Docker & Docker Compose
- Git (optional)

---

## 🧪 Local Development (venv)

```bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate

# Install Django
pip install django

# Freeze dependencies
pip freeze > requirements.txt

# Start Django project (only once)
django-admin startproject myproject

# Run the app
cd myproject
python manage.py runserver
```

Then open http://localhost:8000

---

## 🐳 Run with Docker

```bash
docker-compose up --build
```

The app will be available at: http://localhost:8000

---

## 📂 Files to Check or Edit

- **myproject/settings.py**
  - Set `ALLOWED_HOSTS = ["*"]` for Docker.
- **.dockerignore**
  - Make sure `venv/` is ignored in Docker.
- **.gitignore**
  - Make sure `venv/` and `__pycache__/` are ignored in Git.

---

## 🧼 Clean Up

To stop containers:

```bash
docker-compose down
```

To remove images:

```bash
docker image prune
```

---

## 🧑‍💻 Author

Made with ❤️ by CHOUROUK

