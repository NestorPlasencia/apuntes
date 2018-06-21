# Bravo Survey System

Survey System project for Bravo Consultoría

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development  purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* [Conda](https://conda.io/docs/user-guide/install/index.html) ( Anaconda or Miniconda )
* [Git](https://git-scm.com/)

### Installing

#### Clone the project

```bash
$ git clone git@gitlab.com:softbutterfly/bravo-consultoria/backend.git
$ cd backend/
```

Clone the git submodules

```bash
$ git submodule init
$ git submodule update
```

#### Backend Install

Change to development branch

```bash
$ git checkout develop
```

Create and activate the enviorement

```bash
$ conda create -n bravo-consultoria -c conda-forge --file requirements.conda
$ source activate bravo-consultoria
```

Install the project dependencies

```bash
$ pip install -r requirements.pip
```

Make the migrations to the database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

Test the django project

```bash
$ python manage.py runserver
```

In the browser

````bash
http://127.0.0.1:8000/
````

Cancel the test with `Ctrl`+ `C`

#### Frontend Install

Change to the frontend submodule

```bash
$ cd frontend 
```

Change to development branch

```bash
$ git checkout develop
```

Install package.json dependencies

```bash
$ yarn install
```

Test the vue project

```bash
$ yarn run start:dev
```

In the browser

```bash
http://localhost:1234/
```

Cancel the test with `Ctrl`+ `C`	

## Built With

- [Django](https://www.djangoproject.com/) - The Web framework for perfectionists with deadlines
- [Vuejs](https://vuejs.org/) - The Progressive JavaScript Framework