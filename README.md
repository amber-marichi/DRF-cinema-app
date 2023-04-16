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

### To run using Docker
!! Docker with docker compose must be installed and ready

1. Prepare the .env file using .env.sample provided in project main directory. Change following values accordingly to database name, user name and password. Save file with variables as ".env"
```sh
POSTGRES_DB=POSTGRES_DB
POSTGRES_USER=POSTGRES_USER
POSTGRES_PASSWORD=POSTGRES_PASSWORD
```
2. Run docker compose command
```sh
docker compose up
```
Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
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
