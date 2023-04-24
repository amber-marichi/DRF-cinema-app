# DRF-cinema-app
Cinema API with Django REST Framework, JWT authentication, and PostgreSQL

## Features
- Authenticate with JWT
- Create cinema halls
- Create movies with genres and actors
- Manage orders and tickets
- Filter movies and movie sessions
- Access documentation at ../api/doc/swagger/
- Access admin panel at ../admin/

## Setting up project and getting started
Install using GitHUB
```sh
git clone https://github.com/amber-marichi/DRF-cinema-app.git
cd DRF-cinema-app
```

Prepare the .env file using .env.sample provided in project main directory. Change following values accordingly to Django SECRET_KEY, hostname, database name, user name and password. Save file with variables as ".env"
```sh
SECRET_KEY=SECRET_KEY
POSTGRES_HOST=POSTGRES_HOST
POSTGRES_DB=POSTGRES_DB
POSTGRES_USER=POSTGRES_USER
POSTGRES_PASSWORD=POSTGRES_PASSWORD
```

### To run using Docker
!! Docker with docker compose must be installed and ready

Run docker compose commands and wait till containers are built and started
```sh
docker compose build
docker compose up
```
Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

### To run locally
!! Python3.8+ with pip should be installed and ready.
PostgreSQL database should be running locally or in Docker with creds corresponding to ones stated in .env file.

1. Create and activate venv:
```sh
python -m venv venv
```

2. Activate environment:

On Mac and Linux:
```sh
source venv/bin/activate
```
On Windows
```sh
venv/Scripts/activate
```

3. Install requirements:

```sh
pip install -r requirements.txt
```

4. Apply migrations

```sh
python manage.py migrate
```

5. Start the app:

```sh
python manage.py runserver
```

### To get access to the app
1. Go to registration page and enter email with password to use for access
```sh
http://127.0.0.1:8000/api/user/register/
```
2. After registration proceed to token page. Enter email and password to obtain access token. Save it to use later
```sh
http://127.0.0.1:8000/api/user/token/
```
3. Now you are ready to proceed with using service by submitting access token in http request header
```sh
http://127.0.0.1:8000/api/doc/swagger/
```
