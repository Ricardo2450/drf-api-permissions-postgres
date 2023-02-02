# Lab 32, 33

### Lab32: Permissions & Postgresql. Lab33: Authentication & Production Server

### Author: Ricardo Soto-Fabela

### Partners: Aubrey, Angelos

### How to run tests:

python manage.py runserver Navigate to snacks/tests 
Run in terminal: python manage.py test

# Setup
- python3.11 -m venv .venv 
- pip install django 
- pip install djangorestframework
- pip install psycopg2-binary
- django-admin startproject jobs_project . 
- python manage.py startapp jobs
- pip install djangorestframework-simplejwt
- pip install gunicorn
- pip install whitenoise
- python manage.py migrate
- pip freeze > requirements.txt
- python manage.py createsuperuser

# To run:

> gunicorn jobs_project.wsgi:application --bind 0.0.0.0:8000 --workers 4

Load the site at http://0.0.0.0:8000/

### Resources

* https://www.django-rest-framework.org/api-guide/authentication/