# Django cheat sheet to get running fast

## Creating a new project

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


## The Model

### What is a model?

Basically, that's how the data looks in the database. In our model class we can define schemas, which then gets written to our database using migrations. This is the single source of truth for the data in our app. 

Concepts to pay attention to:




## The view
