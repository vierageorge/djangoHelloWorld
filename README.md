# Django Hello World

Here I'll be adding the file used to learn the basics on Django.

## Prerequisites
Basically, have Python and Virtualenv installed on your PC with PATH correctly configured.

## Initial Instructions
First, create a virtual environment, activate it and install Django
```
virtualenv django_venv
.\django_venv\Scripts\activate
pip install django
```
Create a project and verify if it works on the development server. Then start and app.
```
django-admin startproject mysite
python manage.py runserver
python manage.py startapp polls
```
## Hands on Django Code
Here, I'll be describing things done out of the code.
### Working with views.
The following files where modified to start working with views:
* polls/views.py: where the actual view is defined.
* polls/urls.py: Created manually, the URL-to-View Mapping is defined in it.
* mysite/urls.py: This file is used in the project's url file (mysite/urls.py) with 'include' instruction.

Take into account that view here doesn't refer to views in the MVC Model. It's more like the Controller part. The MVC's views will be Django's templates.

### Databases and Models
I'll start the tutorial with SQlite, so I'll be using default values. TODO -> Migrate to MySQL or PostgreSQL. Generate the database schema. This will perform actions on the actual database only for INSTALLED_APPS in setting.py.
```
python manage.py migrate
```
Add the app to the project's setting.
```
polls.apps.PollsConfig
```
Then create the models in polls/models.py file. In this case, models for Question and Choice were added. After that, generate migration instructions for the model just created and check how SQL would look like. Makemigrations will track changes in the models. Finally, apply the migration to the database.
```
python manage.py makemigrations polls
python manage.py sqlmigrate polls 0001
python manage.py migrate
```

## Deployment
TODO -> Add additional notes about how to deploy this on a live system

## Authors
* **Jorge Viera** - *Initial work* - [viergeorge](https://github.com/Viergeorge)

## License
TODO -> Understand this part.

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
