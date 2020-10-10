# Django cheat sheet to get running fast

## Creating a new project

This is a bunch of "How do I do x?" type questions that needs to be answered in order to get a project going in Django. 

### Starting the project

Follow these steps to get a Django app running.


After install Django, run the following to start a new project.

```
django-admin startproject <project-name>
```

### Create a new app under the project

```
python manage.py startapp <appname>
```

### Running the development server

```
python manage.py runserver
```


### 


## The Model

### What is a model?

Basically, that's how the data looks in the database. In our model class we can define schemas, which then gets written to our database using migrations. This is the single source of truth for the data in our app. Generally speaking, each model maps to a single table in the DB. 

#### The basics
* Each model is a python class that subclasses django.db.models.Model
* Each attribute of the model represents a database field
* A


Concepts to pay attention to:




## The view


Views are fairly loosely defined in Django. Generally, a view is responsible for two things:
1. Returns an HTTpResponse Object containing the content of the requested page, or,
2. Raise an exception such as 404.

Usually, the view retrieves data according to the parameters, loads a template and renders the template with the data. 


### Setting up views:

It doesn't really matter where you put your view functions, or what the functions are called, other than following good coding conventions. 

Conventionally, we put them into a file called views.py

Here is an example of a view function. Notice how it takes a request and produces an HttpResponse. 
```
def detail(request, question_id):
    return HttpResponse("You're looking at question %s." % question_id)
```

After defining the view, make sure to register it in urls.py under the app's directory. 