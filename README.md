# py-dockerize-cinema-api

API service for cinema management written on Django REST Framework

## Installing using GitHub:
Install PostgresSQL and create db.
```
git clone https://github.com/OleksandrYanchuk/py-dockerize-cinema-api.git
cd py-dockerize-cinema-api
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
mv .env.sample .env
```
Place expected values of all variables into .env.sample:
```
SECRET_KEY=SECRET_KEY
POSTGRES_NAME=POSTGRES_NAME
POSTGRES_USER=POSTGRES_USER
POSTGRES_PASSWORD=POSTGRES_PASSWORD
```
## Run with Docker:
```
docker-compose build
docker-compose up
```

## Outside the Docker network, you can access it using http://127.0.0.1:8000 on the host machine.

## Getting access:
- create user via /api/user/register/
- get a JWT token via /api/user/token/

## Features:
- JWT authenticated
- Admin panel /admin/
- SWAGGER documentation /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
