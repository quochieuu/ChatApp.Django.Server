# ChatApp
Techonologies used:
* Django REST FRAMEWORK
* ReactJs
* NodeJs
  
## Create Project
```
mkdir backend
cd backend
```
## Environment
```
python3 -m venv virtualenv
source virtualenv/bin/activate
```

## Install Pip
```
python3 -m pip install --upgrade pip
```

## Install Django & Django Rest
```
pip install Django
pip install djangorestframework
```
### Add 'rest_framework' to your INSTALLED_APPS setting.
```
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

## Create a Django Project
```
django-admin startproject core .
```

## Create a Django Application
```
python manage.py startapp account
python manage.py startapp orders
python manage.py startapp payment
python manage.py startapp store
```

## Start Server
```
python manage.py runserver
```

## PostgreSQL database
To connect to a PostgreSQL server with Python, please first install the psycopg2 library
```
pip install psycopg2
```

In your settings.py, add an entry to your DATABASES setting
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'leotech_site',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

## Migrate the Database
### Create a migration 
```
python manage.py makemigrations store
```

### Create a migration file
```
python manage.py migrate account
python manage.py migrate orders
python manage.py migrate payment
```

### Use the Django shell
```
python manage.py shell
```

### Import your models
```
from account.models import Accounts
p1 = Accounts(
title = 'Lorem Ipsum',
summary = 'Lorem Ipsum is simply dummy text of the printing and typesetting industry',
description = 'Lorem Ipsum is simply dummy text of the printing and typesetting industry',
text = 'Lorem Ipsum is simply dummy text of the printing and typesetting industry',
company = 'Lorem Ipsum',
image = 'img/lorem-ipsum.png',
status = '1'
)
p1.save()
```