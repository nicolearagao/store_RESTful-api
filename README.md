# store_RESTful-api
Simple store CRUD API written on Flask with Sqlite database and SQLAlchemy

## Features

- user registration and JWT authentication
- add, update and delete items from the store
- get information about all the current items or get item info by name 

## Installation

´´´
git clone https://github.com/nicolearagao/store_RESTful-api.git
cd store_RESTful
python3 -m venv venv
source ./venv/bin/activate
pip install -r requirements.txt
python3 ./create_tables.py
python3 ./app.py

´´´
Press CTRL + C to terminate the server
use ´´´ deactivate ´´´ to quit the virtual environment







