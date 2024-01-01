# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://github.com/SAIDARSHINI27072005/django-orm-app/assets/147474227/e3c6fa1b-ae67-4ddf-9de7-41cbd6e9b53c)


## DESIGN STEPS

### STEP 1:
clone the problem from github
### STEP 2:
create a new app in django project
### STEP 3:
Enter the code for admin.py and models.py

## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin
# Create your models here.
class Student (models.Model):
referencenumber=models.CharField(max_length=20,help_text="reference 
number")
 name=models.CharField(max_length=100)
 age=models.IntegerField()
 email=models.EmailField()
 mobileno=models.IntegerField()
class StudentAdmin(admin.ModelAdmin):
 list_display=
('referencenumber','name','age','email','mobileno')

 admin.py

from django.contrib import admin
from .models import Student, StudentAdmin
# Register your models here.
admin.site.register(Student,StudentAdmin)
```


## OUTPUT

![image](https://github.com/SAIDARSHINI27072005/django-orm-app/assets/147474227/a7cd7115-2f1b-4ac8-8a25-aea36a19255f)





## RESULT
The program for creating a database using ORM has been executed sucessfully.
