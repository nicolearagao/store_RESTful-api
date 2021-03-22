# Store API

## Summary
Simple RESTful Flask application created with Sqlite and SQLAlchemy.

## Features

- user registration and JWT authentication
- add, update and delete items from the store
- get information about all the current items or get item info by name 

## Endpoints and Request/Response

- ### Request
POST  /register  username and password registration 
  ### Response 
201 user was created successfully<br/>
400 username already exists

- ### Request 
POST /auth generates JWT token for registered users
  ### Response
401 invalid credentials 
200 returns the generated access token 

- ### Request 
GET /item/<string:name> get item by name, requires a JWT token 
  ### Response
404 Item not found
200 returns the item
401 invalid credentials - request does not have an access token 

- ### Request 
POST /<string:name> post a new item, requires a name and a price 
  ### Response
400 Item with that name already exists
201 return the item, post successful
402 price can't be left blank 
500 an error occurred inserting the item into the database

- ### Request 
DELETE /item/<string:name> delete an item 
  ### Response
404 item not found 
200 item deleted successfully

- ### Request 
PUT /item/<string:name> update an item if it already exists, if not creates it 
  ### Response
200 returns item created or updated 
400 price field cannot be left blank 

- ### Request 
GET /items return a list of all the items of the store 
  ### Response
200 returns all the items of the store or a blank list 


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

- [Flask](https://github.com/pallets/flask)
- [SQLAlchemy](https://github.com/zzzeek/sqlalchemy)
- [Flask-JWT](https://github.com/mattupstate/flask-jwt)
- [Flask-RESTful](https://github.com/flask-restful/flask-restful)







