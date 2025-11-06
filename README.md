<div align="center">
<h1>Task Manager</h1>

<p>
    A simple and flexible task management web application.
</p>

<p>
<a href="#about">About</a> •
<a href="#installation">Installation</a> •
<a href="#usage">Usage</a> 
</p>

<p align="center">

  <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=fff" alt="Python 3.10+">
  <img src="https://img.shields.io/badge/Django-5.0-092E20?style=for-the-badge&logo=django&logoColor=fff" alt="Django">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=fff" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Bootstrap-5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=fff" alt="Bootstrap 5">
  <img src="https://img.shields.io/badge/Gunicorn-Server-499848?style=for-the-badge&logo=gunicorn&logoColor=fff" alt="Gunicorn">

  <img src="https://img.shields.io/badge/Poetry-Dependency%20Manager-60A5FA?style=for-the-badge&logo=poetry&logoColor=fff" alt="Poetry">
  <img src="https://img.shields.io/badge/pytest-Testing-0A9EDC?style=for-the-badge&logo=pytest&logoColor=fff" alt="pytest">
  <img src="https://img.shields.io/badge/flake8-Linting-F05032?style=for-the-badge&logo=python&logoColor=fff" alt="Flake8">

  <a href="https://python-project-lvl4-k898.onrender.com">
    <img src="https://img.shields.io/badge/Deployed%20on-Render-46E3B7?style=for-the-badge&logo=render&logoColor=fff" alt="Deployed on Render">
  </a>

</p>

</div>

<details><summary style="font-size:larger;"><b>Table of Contents</b></summary>

- [TASK MANAGER](#task-manager)
  - [About:](#about)
  - [Requirements:](#requirements)
    - [Makefile commands:](#makefile-commands)
  - [Installation:](#installation)
      - [Python](#python)
      - [Poetry](#poetry)
      - [PostgreSQL](#postgresql)
    - [Application](#application)
  - [Usage](#usage)
  - [How to use this App:](#how-to-use-this-app)

</details>

# TASK MANAGER
## About:
[Task Manager](https://python-project-lvl4-k898.onrender.com) is a web application tweb application built with Python and [Django](https://www.djangoproject.com/) framework. The application allows a registered user to create, edit and delete tasks, as well as add an executor, status and labels to them.

## Requirements:
App developed with:
* [Python](https://www.python.org/)
* [Django](https://www.djangoproject.com/)
* [Bootstrap 5](https://getbootstrap.com/)
* [PostgreSQL](https://www.postgresql.org/)
* [Beautiful Soup 4](https://www.crummy.com/software/BeautifulSoup/)
* [Psycopg 2](https://www.psycopg.org/)
* [Gunicorn](https://gunicorn.org/)
* [Rollbar](https://rollbar.com/)
* [Poetry](https://python-poetry.org/)
* [pytest](https://docs.pytest.org/en/7.2.x/)
* [Flake8](https://flake8.pycqa.org/en/latest/)

### Makefile commands:
Install all dependencies of the package: ```make install```

Install poetry project and start postgresql server: ```make build```

Generate and apply database migrations:  ```make migrate```

Run Django development server at http://127.0.0.1:8000/: ```make dev```

Start gunicorn server: ```make start```

## Installation:

#### Python

Before installing the package make sure you have Python version 3.10 or higher installed:

```bash
>> python --version
Python 3.10.12
```

#### Poetry

The project uses the Poetry dependency manager. To install Poetry use its [official instruction](https://python-poetry.org/docs/#installation).

#### PostgreSQL

As a database, the PostgreSQL database system is being used. You need to install it first. You can download the ready-to-use package from [official website](https://www.postgresql.org/download/) or use Homebrew.

```bash
>> psql --version
PostgreSQL 14.12
```

### Application

To use the application, you need to clone the repository to your computer. This is done using the `git clone` command. Clone the project:

```bash
>> git clone https://github.com/shizomanya/python-project-lvl4.git && cd python-project-lvl4
```

Then you have to install all necessary dependencies:

```bash
>> make install
```

Create .env file in the root folder and add following variables:
```
DATABASE_URL = postgresql://{provider}://{user}:{password}@{host}:{port}/{db}
SECRET_KEY = '{your secret key}'
DEBUG = True
ALLOWED_HOSTS = webserver
```
To create the necessary tables in the database, start the migration process:

```bash
>> make migrate
```
---
## Usage

Start the gunicorn Web-server by running:
```bash
make start
```
By default, the server will be available at http://0.0.0.0:8000. 

_It is also possible to start it local in development mode with debugger active using:_
```bash
make dev
```
_The dev server will be at http://127.0.0.1:8000._

## How to use this App:

| Tool               | Description                                             
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Registration       | First, you need to register in the application using the registration form provided.                                                                                    |
| Log in             | To view the list of tasks and create new ones, you need to log in using the information from the registration form.                                                     |
| User               | You can see all users on the relevant page. You can change the information only about yourself. If the user is an author or an executor of the task he cannot be deleted|
| Statuses           | You can add, update, delete statuses of the tasks, if you are logged in. The statuses which correspond with any tasks cannot be deleted.                                |
| Labels             | You can add, update, delete labels of the tasks, if you are logged in. The label which correspond with any tasks cannot be deleted.                                     |
| Tasks              | You can add, update, delete tasks, if you are logged in. You can also filter tasks on the relevant page with given statuses, exetutors and labels.                      |


