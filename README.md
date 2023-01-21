# Laravel Docker Skeleton
A lightweight Docker container that sets up the basic containers for a local Laravel development.

## Installation
- Make sure you have [Docker installed](https://docs.docker.com/docker-for-mac/install/) on your system, and then clone this repository.
- Navigate in your terminal to the directory you cloned, and spin up the containers for the web server by running `docker-compose up -d --build app`.
- After that completes, Clone or create your laravel project inside the `src` directory.

**Note**: Your MySQL database host name in `.env` should be `mysql` (The database container name in `docker-compose` file), **not** `localhost`. The username, password and database should both be the same in `.env` file and `docker-compose` file. 

**Note**: If you want to use PostgreSql instead of MySql uncomment the `postgres` and `pgadmin` containers in `docker-compose.yml` file.

<br>

## Ports
- **nginx** - `:80`
- **mysql** - `:3306`
- **phpmyadmin** - `:8081`
- **postgres** - `:3000`
- **pgadmin** - `:82`
- **php** - `:9000`
- **redis** - `:6379`
- **mailhog** - `:8025` 

<br> 

### You can use composer, npm and artisan from the container like this:
- `docker-compose run --rm artisan make:controller`
- `docker-compose run --rm composer install`
- `docker-compose run --rm npm install`
