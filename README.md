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

# Isso aqui ignora maiúscula
Restaurant.objects.filter(name__startswith='casa')

Restaurant.objects.last().product_set.all()

Restaurant.objects.last().product_set.create(title='Feijoada Grande', description='Feijoada para duas pessoas')

Product.objects.filter(restaurant__pub_date__year=2022)
