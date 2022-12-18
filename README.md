# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![entity](https://user-images.githubusercontent.com/115707860/208310917-ecaee74e-4d23-47e6-81a1-2874d6ecd843.png)


## DESIGN STEPS

### STEP 1:
Create a project and inside the project folder, create an application using - django-admin startproject <projectname> and django-admin startapp <appname>.Inside the applicaton folder, open setiings.py and allow all the hosts.
### STEP 2:
Now in the application folder, open models.py and write the code for your desired table here. Go to admin.py and migrate all your data.
### STEP 3:
On running the server, open the html page.Here you can add or get the desired data from the table you have created.

## PROGRAM
```
from django.db import models
from django.contrib import admin
# Create your models here.
class Books(models.Model):
    bookno=models.IntegerField(primary_key=True)
    bookname=models.CharField(max_length=100)
    author=models.CharField(max_length=100)
    qty=models.IntegerField()
    price=models.IntegerField()

class BooksAdmin(admin.ModelAdmin):
    list_display=('bookno','bookname','author','qty','price')

from django.contrib import admin
from .models import Books,BooksAdmin
# Register your models here.
admin.site.register(Books,BooksAdmin)
```

## OUTPUT

![Screenshot (4)](https://user-images.githubusercontent.com/115707860/208310994-acb4547f-bdb2-45f4-9a35-a8317d08536d.png)



## RESULT
In the end, you would have created a small database  where you can store and retrieve your data using Objecct Realtional Mapping(ORM).
