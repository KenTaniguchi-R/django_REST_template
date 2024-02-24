This is a template for Django REST freamawork project.
This template gives you a basic structure for a Django REST framework project.

This project is based on the following technologies:
- Django
- Django REST framework
- CORS headers
- environment variables
- dj-database-url

## How to use this template
1. Clone this repository
2. Rename the folder to your project name
3. Change the remote origin to your repository
4. Install the requirements
`pip install -r requirements.txt`
5. Create a .env file based on the .env.example file
6. Run the migrations
`python manage.py migrate`
7. Run the server
`python manage.py runserver`
8. Start coding!

## How to use the environment variables
The environment variables are loaded from the .env file. You can access them using the `os` module.
```python
import os
import environ

env = environ.Env()
environ.Env
# SECURITY WARNING: keep the secret key used in production
SECRET_KEY = env('SECRET_KEY')

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = env('DEBUG', default=False)

ALLOWED_HOSTS = env.list('ALLOWED_HOSTS', default=['*'])
```

## How to use CORS headers
The CORS headers are already configured in the settings.py file. You can change the CORS_ORIGIN_WHITELIST to your needs.
```python
CORS_ORIGIN_WHITELIST = env.list('CORS_ORIGIN_WHITELIST', default=['http://localhost:3000'])
```

## How to use dj-database-url
The dj-database-url package is already installed and configured in the settings.py file. You can change the DATABASE_URL environment variable to your needs.
```python
DATABASES = {
    'default': env.db('DATABASE_URL', default='sqlite:///db.sqlite3')
}
```

