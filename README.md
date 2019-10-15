# retail-store-api

## Description
This project is implemented with Python using Flask, and is a secure REST API designed for the retail sector.

The API enables stakeholders to efficiently store multiple items to a database, where the items are allocated to a specified store branch.

## Features
* Users can use the API endpoints to register and login, to post, update, get or delete items and stores.

* Each item requires a name, price and its associated store name to be successfully posted/updated to the database.

* Stores can be posted, updated and deleted from the database, but require a name to be saved. It is possible to retrieve all the stores in the database and their associated items.

* Obtaining access to stores and items requires users to be logged in with JWT tokens.

## Technologies Used
* **[Python3](https://www.python.org/downloads/)** - A programming language that lets you work more quickly (The universe loves speed!).
* **[Flask-RESTFUL](https://flask-restful.readthedocs.io/en/latest/)** - An extension for Flask that adds support for quickly building REST APIs.
* **[Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/)** - It adds support for SQLAlchemy ORM.
* **[Virtualenv](https://virtualenv.pypa.io/en/stable/)** - A tool to create isolated virtual environments.
* **[PostgreSQL](https://www.postgresql.org/download/)** – Postgres database offers many [advantages](https://www.postgresql.org/about/advantages/) over others.
* Minor dependencies can be found in the requirements.txt file on the root folder.


## REST endpoints
Authorized user can view/add/update/delete stores and items in them using the REST endpoints. Below is an overview of REST end points:

### Retail Stores
*  GET /stores - fetches list of all stores data
*  GET /store/<name> - fetches a specific store
*  POST /store/<name> - creates a new store based on request JSON
*  PUT /store/<name> - updates store data based on request JSON
*  DELETE /store/<name> - delete an existing with the given name


### Items
*  GET /items - fetches all item data
*  GET /item/<name> - fetches item of a particular name
*  POST /item/<name> - creates a item name
*  PUT /item/<name> - updates item data
*  DELETE /item/<name> - deletes item from the system

 These REST end points are secured using basic authentication mechanism. 

## Installation

```
pip install Flask
pip install Flask-RESTful
pip install Flask-JWT
pip install Flask-SQLAlchemy

python app.py
```