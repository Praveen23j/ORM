# Ex02 Django ORM Web Application
## Date: 17.11.2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![image](https://github.com/user-attachments/assets/2d4d9f64-f8c2-437d-b4bc-077743a7dca1)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:from django.contrib import admin
from .models import Bank_loan,Bank_loanAdmin
admin.site.register(Bank_loan,Bank_loanAdmin)
Execute Django admin and create details for 10 books

## PROGRAM
models.py

from django.db import models
from django.contrib import admin
class Bank_loan (models.Model):
    customer_id=models.IntegerField(primary_key=True)
    customer_name=models.CharField(max_length=100)
    loan_amount=models.IntegerField()
    customer_age=models.IntegerField()
    email=models.EmailField()

class Bank_loanAdmin(admin.ModelAdmin):
    list_display=('customer_id','customer_name','loan_amount','customer_age','email')

admins.py

from django.contrib import admin
from .models import Bank_loan,Bank_loanAdmin
admin.site.register(Bank_loan,Bank_loanAdmin)
## OUTPUT

![Screenshot 2024-11-18 091402](https://github.com/user-attachments/assets/7c92af09-b6fa-48be-8d2d-c49c569b77e2)

![Screenshot 2024-11-18 091316](https://github.com/user-attachments/assets/e8d098a2-d830-493e-a3e7-b7fe6a4761f4)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
