# Getting Started



### Installation
1. Create a virtual environment (recommended):
    ```bash
    python3 -m venv env
    source env/bin/activate  # Linux/macOS


2. Install Django:
    ```bash
    pip install django
    ```

3. Create a new Django project:
    ```bash
    django-admin startproject myproject  
   
    cd myproject              
   
   python manage.py startapp my_app_name
    ```

### Running the Development Server
1. Start the development server:
    ```bash
    python manage.py runserver
    ```

    This will launch the Django server at http://127.0.0.1:8000/ by default. You can access your application in a web browser.

### Creating Models
1. Models define the data structure for your application. You can modify your models in the `models.py` file within your project's `myproject` directory.

2. Register your models in the admin panel by adding them to the `admin.py` file in the same directory. e.g.  

         from django.contrib import admin
         from .models import Member, CarModel, Task, Review
         
         admin.site.register(Model_01)
         admin.site.register(Model_02)
         admin.site.register(Model_03)
         admin.site.register(Model_etc)
3. 
### Applying Database Changes
1. Create migrations:
    ```bash
    python manage.py makemigrations <app_name>

    This generates migration files that track changes made to your models.

2. Apply migrations:
    ```bash
    python manage.py migrate
    ```

    This applies the generated migrations to your database, ensuring the schema reflects your model updates.

### Creating an Admin User
1. Create a superuser:
    ```bash
    python manage.py createsuperuser

    Follow the prompts to enter a username, email address, and password for your admin account.


2. Start the development server:
    ```bash
    python manage.py runserver

### Additional Notes
1.  http://127.0.0.1:8000/admin/ 