# Django notes

#### Django is a framework for building webapps that's supposed to be quick and easy, wrapping up a lof of webdev hassle into nice structures. 

### Installation
Django package contains sqlparse: apparently, for parsing sql requests.

`startproject` command takes care of creating necessary files automatically -- no need for poetry?

`manage.py` contains code to run a development server AND MANY OTHER THINGS IT'S JUST A DJANGO INTERFACE TO USE CL ARGUMENTS (`runserver` command when running the py file)

`startapp` command to create an app inside the project -- there can be several apps with different functionality within one project

### Building

Pages of the app (e.g., `http://localhost:8000/polls/`) are added with `path()` and `include()` functions by appending new paths to the list of `urlpatterns` inside `urls.py`

Django can be used with diifferent databases. The default is SQLite. 

Django can manupulate the databases:
`migrate` creates db tables
`makemigrations` makes changes in schemas

for MODELS `__str__` method has to be defined for interactivity

### Admin stuff

`createsuperuser` VERY EASY to add other users incdredible amazing stuff thank you

allows to see what apps are crated inside if registered in `admin.py`

WHY THO the options for votes are added through shell instead of in the admin interface -- found answer in the end: the options are added and registered through `admin.py` and appear in the interface

### Views

**Views** are web pages (a fucnction or a method of a class)

`http://127.0.0.1:8000/polls/4/results/`
`http://127.0.0.1:8000/polls/4/vote/`
PRETTY urls with just several functions -- every page is a function

**Templates** (basically htmls) separate design stuff from python

HTMLs <-- VIEWS <-- URLs and MODELs + all that hooked up with admin

### Testing

Tests are created as classes inside `tests.py` in the project directory.

Can be run with the command `python manage.py test polls`


