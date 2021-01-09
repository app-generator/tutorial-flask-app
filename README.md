# Flask App Tutorial

> Content provided by experienced developers based on the suggestions/questions from the audience. This initiative aims to provide **Free/Allways up-to-date** programming tutorials - Read the [Manifest](https://github.com/app-generator/learn-to-code).

<br />

## Topics

- [Flask Introduction](#flask-introduction)
- [Set up](#set-up) (aka environment)
- [Edit the code](#edit-the-code)
- [Start the application](#start-the-application)
- [Summary](#summary)

<br />

> Questions/Spot a problem? please open a new [issue](https://github.com/app-generator/tutorial-flask-app/issues/new).

<br />

## Flask Introduction

:point_right: Flask is a lightweight web application framework. It is designed to make getting started quick and easy, with the ability to scale up to complex applications. Compared to Django, Flask provides a lightweight codebase and more freedom to the developer.

Flask is written in [Python](https://www.python.org/) and it does not require particular tools or libraries.

> Useful Flask Resources

- [Flask](https://palletsprojects.com/p/flask/) - the official website
- [Flask Docs](https://flask.palletsprojects.com/en/1.1.x/) - learn what Flask has to offer in detail 
- [Flask Tutorial](https://github.com/app-generator/tutorial-flask) - content provided by experienced developers


<br />

<p align="right"><a href="#topics"> :point_up_2: Return to top</a></p>

<br />

## Set up

:point_right: To code a Flask application we need some tools properly set up in our workstation. Here is the recommended list: 

- [Python v3](https://www.python.org/downloads/) - the language used by Flask
- A (free) editor: [VsCode](https://code.visualstudio.com/), [Sublime](https://www.sublimetext.com/), [Atom](https://atom.io/), [Notepad++](https://notepad-plus-plus.org/)

<br />

To finish this tutorial we will work with the console (aka terminal). In Windows, we can use `Powershell` or the corespondent `xterm` for Linux. The next step is to open a terminal and check the Python installation:

```bash
$ python --version
Python 3.8.4
```

If the above command returns an error please double check the Python installation and get back here after to follow up the next steps.

<br />

**Install Flask**

Flask is basicaly a Python package and we can install it with ease via a tool shipped by Python: [PIP](https://pypi.org/project/pip/).

```bash
$ pip install Flask
```

<br />

<p align="right"><a href="#topics"> :point_up_2: Return to top</a></p>

<br />

## Edit the code

:point_right: Create a new file named **hello.py** in the current directory and add this code:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return f'My first Flask APP!'
```

This simple code snippet ( also saved [here](./hello.py) ) does the following:

- Import `Flask`, the library that we've installed in the previous step
- `app` object is constructed by `Flask`. At this point, we can use all features provided by **Flask**
- define a defaut `route` that will return a simple *Hello* message when someone access our application using the browser

<br />

<p align="right"><a href="#topics"> :point_up_2: Return to top</a></p>

<br />

## Start the application

:point_right: Flask being such a nice framework, comes with a simple server to help us check the code without being forced to install 3rd party tools. To use it and see our minimal app running in the browser, a variable must be exported in the `environment` that informs `Flask` the name of the file:

```bash
$ # Set the FLASK_APP environment variable
$ # Unix/Mac 
$ export FLASK_APP=hello.py
$
$ # Windows OS 
$ set FLASK_APP=hello.py
$ 
$ # Windows OS - Powershell
$ $env:FLASK_APP = ".\hello.py"
```

Once we have this variable we can call `Flask`:

```bash
$ flask run
```

By default `Flask` will start the application on address 'localhost:5000'. If we visit the aplication in the browser, we should see the message:

**My first Flask APP!**

<br />

<p align="right"><a href="#topics"> :point_up_2: Return to top</a></p>

<br />

## Summary

:point_right: During this tutorial we've learned a few basic things:

- What is Flask and how to install it
- We've code a super simple app
- We've seen the application running in the browser

<br />

**Where to go from here?**

- Access the [Flask Tutorial](https://github.com/app-generator/tutorial-flask) and learn more about Flask
- [Learn to code](https://github.com/app-generator/learn-to-code) using other technologies. 

<br />

<p align="right"><a href="#topics"> :point_up_2: Return to top</a></p>

<br />

---
**Flask App Tutorial** - Free/Allways up-to-date Flask-related content | by [AppSeed](https://appseed.us?ref=gh).
