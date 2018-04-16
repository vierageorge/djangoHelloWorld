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
```
polls/views.py
polls/urls.py
mysite/urls.py
```
In the first file, the actual view is defined. The second file is created manually and in it, the URL-to-View Mapping is defined. This filed is then used in the project's url file (mysite.urls).

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
