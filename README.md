# Django-crm

# To connect MySQL to Django  and Create the first app

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

# Create mydb.py to the root folder with the details
import mysql.connector

dataBase =  mysql.connector.connect(
    host = 'localhost',
    user = 'root',
    passwd = '1234'
    
)

cursorObject = dataBase.cursor()

cursorObject.execute("CREATE DATABASE melux")

print("All Done!")



# Git Control
1. git config --global user.name "USERNAME_ON_GITHUB"
2. git config --global user.email "YOUR_MAIL"
3. git config --global push.default matching
4. git config --global alias.co checkout
5. git init
6. git add . 
7. git commit -am "Initial"

# CREATE A REPOSITORY ON GITHUB
push an existing repository from the command line
