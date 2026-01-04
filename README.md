# 🌐 Building Your First API with Django and Django Rest Framework

Join us for an exciting tutorial 🎓, where we'll dive into the world of web APIs using Python's beloved Django framework and the Django Rest Framework. This session is perfect for Python enthusiasts 🐍 eager to expand their web development skills in a practical, hands-on environment.

📖 **[View the full tutorial online](https://felipythondev.github.io/building-your-first-api-with-django-and-django-rest-framework/)**

**What You Will Learn**

- 🔍 Introduction to API Development with Django: Understand the basics of API construction and the role of Django and Django Rest Framework in modern web development.
- 📊 Django Models: Explore how to create and utilize Django models, the backbone of data handling in Django applications.
- 🔗 URL Mapping and Views: Master URL configuration for efficient API endpoint creation and discover how Django views and ViewSets drive your API's functionality.
- 🔄 Serializers in Action: Learn to implement serializers for converting data formats, a critical step in RESTful API development.
- 💻 Practical Application: Engage in hands-on coding to apply these concepts in building a functional API from scratch.

**Why This Tutorial?**

This tutorial is tailored for those ready to step into API development with Django. We focus not just on theoretical knowledge but also emphasize practical skills. By the end of this session, you'll have a clear understanding of the essential components of Django for API development and hands-on experience in building an API.

Are you already navigating the Django landscape and seeking to deepen your expertise? 🌱 This tutorial provides an immersive opportunity to advance your web development skills and explore the intricacies of API development using Django and the Django Rest Framework. 🚀 Join us for an enriching journey as we delve into mastering the art of building powerful APIs with Django!

## 📋 Prerequisites

- Python 3.13
- Git
- [uv](https://docs.astral.sh/uv/) - Fast Python package installer and resolver

## 🚀 Quick Start

### 1. Install uv

Follow the installation instructions at: [uv installation guide](https://docs.astral.sh/uv/getting-started/installation/#installing-uv)

### 2. Clone the Repository

```shell
git clone git@github.com:felipythondev/building-your-first-api-with-django-and-django-rest-framework.git
cd building-your-first-api-with-django-and-django-rest-framework
```

### 3. Install Dependencies

```shell
# Sync dependencies (uv will automatically create and manage the virtual environment)
uv sync
```

### 4. Run the Application

```shell
# Run Django development server using uv run
uv run task run
# Django will be running at http://127.0.0.1:8000/

# Run documentation server (in a separate terminal)
uv run task docs
# Documentation will be available at http://127.0.0.1:8001/
```

## 🛠️ Available Commands

### Main Commands (using uv and taskipy)

| Command | Description |
|---------|-------------|
| `uv sync` | Install/sync all dependencies (automatically creates venv) |
| `uv pip install <package>` | Install a specific package |
| `uv pip compile pyproject.toml` | Generate requirements.txt from pyproject.toml |
| `uv run task docs` | Run documentation server (MkDocs) on port 8001 |
| `uv run task run` or `uv run task r` | Run Django development server on port 8000 |

### Django Management Commands

```shell
# First navigate to the first_api directory
cd first_api

# Create a new Django app
uv run python manage.py startapp <app_name>

# Make migrations after model changes
uv run python manage.py makemigrations

# Apply migrations
uv run python manage.py migrate

# Create a superuser
uv run python manage.py createsuperuser

# Open Django shell
uv run python manage.py shell

# Run tests
uv run python manage.py test
```

## 📦 Key Dependencies

From `pyproject.toml`:
- **Django** >=5.1 - The web framework for perfectionists with deadlines
- **Django REST Framework** >=3.16.1 - Powerful toolkit for building Web APIs
- **Taskipy** >=1.13.0 - Task runner for Python projects

## 📁 Project Structure

```
.
├── first_api/              # Django project directory
│   ├── first_api/         # Main Django app
│   │   ├── settings.py   # Django settings
│   │   ├── urls.py       # URL configuration
│   │   └── wsgi.py       # WSGI configuration
│   ├── manage.py          # Django management script
│   └── db.sqlite3        # SQLite database (after migration)
├── docs/                  # MkDocs documentation
├── pyproject.toml        # Project configuration and dependencies
├── requirements.txt      # Pinned dependencies
├── mkdocs.yml           # MkDocs configuration
└── README.md            # This file
```

## 🔄 Updating Dependencies

```shell
# Update requirements.txt from pyproject.toml using uv
uv pip compile pyproject.toml -o requirements.txt

# Upgrade all packages to latest compatible versions
uv pip compile --upgrade pyproject.toml -o requirements.txt

# Sync your environment with updated dependencies
uv sync
```

## 📚 Documentation

The full tutorial documentation is available in two ways:
- **Online**: https://felipythondev.github.io/building-your-first-api-with-django-and-django-rest-framework/
- **Locally**: Run `uv run task docs` and navigate to http://127.0.0.1:8001/

## 🎯 Tutorial Steps Summary

1. **Set up the project** - Clone repo, install uv, sync dependencies
2. **Create the music Django app** - `uv run python manage.py startapp music`
3. **Create Django Models** - Artist, Album, Song models
4. **Configure URL Mapping and Views** - Set up routing and view functions
5. **Implement Serializers** - Convert data between Python and JSON
6. **Build the API** - Create ViewSets and wire everything together
7. **Run migrations** - `uv run python manage.py makemigrations` and `uv run python manage.py migrate`
8. **Test your API** - Access http://127.0.0.1:8000/ to see your working API

For the complete step-by-step tutorial, run `uv run task docs` to view the full documentation.
