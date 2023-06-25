# django-crm

# For connect MySQL to Django  and Create first app

(env) $ pip install mysql
(env) $ pip install mysql-connector
(env) $ pip install mysql-connector-python
(env) $ django-admin startproject NAME_PROJECT
(env) $ cd/NAME_PROJECT
(env) (NAME_PROJECT) $ python manage.py startapp NAME_APP

# Install NAME_APP to setting.py and change DB default
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'NAME_APP',
]

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'melux',
        'USER':'root',
        'PASSWORD':'1234',
        'HOST':'localhost',
        'PORT':'3306',
    }
}

# Create mydb.py to root folder with theas details
