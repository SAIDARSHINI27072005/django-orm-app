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

models.py

from django.db import models
from django.contrib import admin

class Student(models.Model):
    referencenumber=models.CharField(max_length=20,help_text="refernce number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phonenumber=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phonenumber')

class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text='Employee ID')
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary')

admin.py

from django.contrib import admin
from .models import Student,StudentAdmin,Employee,EmployeeAdmin
# Register your models here
admin.site.register(Student,StudentAdmin)
admin.site.register(Employee,EmployeeAdmin)


## OUTPUT

![image](https://github.com/SAIDARSHINI27072005/django-orm-app/assets/147474227/1f16f3f5-0bb5-486a-8c3c-8b9b27b86511)




## RESULT
The program for creating a database using ORM has been executed sucessfully.
