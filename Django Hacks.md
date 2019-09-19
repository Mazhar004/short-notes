# Django Information to Start a Project #

## Django Environment Setup ##
- Python install ```python sudo apt install python3 ```
- Virtual environment install ```sudo apt install python3-venv```
- Create environment ‘venv’ ```python3 -m venv venv``` (2nd venv is your virtual environment name )
- Running virtual environment ```source venv/bin/activate```
- requiremnets.txt  ( Create a file and include, what i need to install )
- Example: Django~=2.2.3 ( Write inside requiremnets.txt )
- ```pip install -r requirements.txt```

## Django Projcet ##
* ### Create project with a name ‘myfirst’: ###
  * ``` django-admin startproject myfirst ```
* ### Create new app with a name ‘blog’: ###
  * ``` python manage.py startapp blog ```
* ### Run evertime if any changes made in django model: ###
  * ``` python manage.py makemigrations ```
  * ``` python manage.py migrate ```
* ### Run project: ###
  * ``` python manage.py runserver ```
* ### Create super user for login page: ###
  * ``` python manage.py createsuperuser ```

## Django Short Information: ##
* ### Template ###
  * Form submission must include ```{% csrf_token %} ```
* ### Django database access ###
  * ``` python manage.py shell ```
  * ``` objects.all() ```
* ### Django kill port: ###
  * ``` sudo lsof -t -i tcp:8000 | xargs kill -9 ```
* ### Django database backup ###
  * ``` python manage.py dumpdata > data_dump.json ```

## Django Settings: ##
  * ``` TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates') ```
  * ``` Change in Templates   ‘DIRS': [TEMPLATE_DIR], ```
  * ``` STATIC_DIR = os.path.join(BASE_DIR, 'assets') ```
  * ``` STATIC_URL = '/static/' ```
  * ``` STATIC_ROOT = os.path.join(BASE_DIR, 'static') ```
  * ``` MEDIA_URL = '/media/' ```
  * ``` MEDIA_ROOT = os.path.join(BASE_DIR, 'media') ```
  * ``` STATICFILES_DIRS=[STATIC_DIR,MEDIA_ROOT,] ```
  * ### Example: ###
    * ``` {% load static %} ```
    * ``` link rel="stylesheet" href="{% static 'css/custom.css' %}"> ```


## Start Celery & Rabbitmq-Server for Asynchronous Process: ##
  * [Procedure Link](https://simpleisbetterthancomplex.com/tutorial/2017/08/20/how-to-use-celery-with-django.html) ( Celery and Rabbitmq with Django )
  * ``` systemctl enable rabbitmq-server ```
  * ``` systemctl start rabbitmq-server ```
  * ``` systemctl status rabbitmq-server ```
  * ``` rabbitmq-server ```
  * ``` celery -A mysite worker -l info ```  (‘mysite’ is my project name)
  * ``` systemctl stop rabbitmq-server ```
  * ``` systemctl status rabbitmq-server ```
  * ``` systemctl disable rabbitmq-server ```

## Django Localization & Internationalization: ##
  * ``` from django.utils.translation import ugettext_lazy (in views) ```
  * ``` from django.utils import translation (in views) ```
  * ``` language_code='es-ES' ```
  * ``` translation.activate(language_code) ```
  * ``` output=ugettext_lazy(‘Welcome to my site’) ```
  * Go to the app root directory:
    * ``` django-admin makemessages -l es_ES ```
    * ``` django-admin makemessages -a ``` ( To compile all language once )
    * It will create .po file
    * After declare translation need to run ``` django-admin compilemessages ```
    * It will create .mo file (Binary file)
