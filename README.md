# Hello FLask

## set variables

```bat
set FLASK_APP=hello
set FLASK_ENV=development 
```

> This will run hello.py file as app, by default it runs app.py, there are two environments, development and production.

## run 

`python -m flask run`

`-p for port`

## using HTML templates

Flask uses jinja template engine.


## How to create a virtual environment

### install virtualenv

`pip install virtualenv`

### create a virtual environment

`python3 -m venv venv`

### activate virtual environment

`venv\Scripts\activate`

then install required libraries(eg flask) and create a package file.

`pip freeze > requirements.txt`

## To Deploy at vercel

1. create a vercel.json file with following content

```json
{
    "version": 2,
    "builds": [{
        "src": "./hello.py",
        "use": "@vercel/python"
    }],
    "routes": [{
        "src": "/(.*)",
        "dest": "/hello.py"
    }]
}
```

then install required libraries(eg flask) and create a package file.

`pip freeze > requirements.txt`