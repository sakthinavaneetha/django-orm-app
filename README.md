# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM)

## Entity Relationship Diagram:
![entity](https://user-images.githubusercontent.com/118671664/208310831-ec238fdf-167c-433e-a7c2-81062d494ed0.png)

## DESIGN STEPS:
### STEP 1:
Create a new Django project using "django-admin startproject",get into the project's terminal and use "python3 manage.py startapp" command.

### STEP 2:
Define a model for the online app customer details in the models.py and allow host access and add the app name under the installed apps in settings.py

### STEP 3:
Register the models with the Django admin site. In admin.py under app folder, register the models with Django admin site.


## PROGRAM

```
#IN models.py:-

from django.db import models
from django.contrib import admin
#Create your model here.
class Customer(models.Model):
    Customerid = models.CharField(max_length=8,primary_key=True)
    Customername = models.CharField(max_length=100)
    Mobilenumber = models.IntegerField()
    email = models.EmailField()
    quantity =models.IntegerField()

class CustomerAdmin(admin.ModelAdmin):
    list_display = ('Customerid','Customername','Mobilenumber','email','quantity')

#IN admin.py:-

from django.contrib import admin
from .models import Customer,CustomerAdmin 
# Register your models here.

admin.site.register(Customer,CustomerAdmin)
```

##OUTPUT:
![web ](https://user-images.githubusercontent.com/118671664/208310844-c3085ccb-f894-477d-bb40-d14668eba5a2.png)


## RESULT:
Thus a Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.
