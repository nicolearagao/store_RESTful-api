# Store simple RESTful API
Simple store CRUD API written on Flask with Sqlite database and SQLAlchemy

## Features

- user registration and JWT authentication
- add, update and delete items from the store
- get information about all the current items or get item info by name 

## Installation

### Virtual environment
```
git clone https://github.com/nicolearagao/store_RESTful-api.git
cd store_RESTful
python3 -m venv venv
source ./venv/bin/activate
pip install -r requirements.txt
python3 ./create_tables.py
python3 ./app.py

```
Press CTRL + C to terminate the server or use ``` deactivate ``` to quit the virtual environment

### Run with Docker

```
docker build -t store-flask:1.0 .
docker run store-flask:1.0

```
Create the tables
```
python3 create_tables.py

```
Start the server

```
python3 app.py

```

## Dependencies

- [Flask] (https://github.com/pallets/flask)
- [SQLAlchemy] (https://github.com/zzzeek/sqlalchemy)
- [Flask-JWT] (https://github.com/mattupstate/flask-jwt)
- [Flask-RESTful] (https://github.com/flask-restful/flask-restful)







