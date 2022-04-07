django-admin startproject myfood
python manage.py migrate

default user and password?
    ???

python manage.py startapp restaurants

python manage.py makemigrations

python manage.py migrate restaurants

python manage.py sqlmigrate restaurants 0001

python manage.py shell

from restaurants.models import Restaurant, Product

from django.utils import timezone

r = Restaurant(name='Casa da Vovó', pub_date=timezone.now())
r.save()