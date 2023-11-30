# iQRAdb (Instrument Quick Reference Application Database)
This is iQRA db, a web application for instrumentation and control engineer. It is running on very minimum web server requirements (deploy in shared hosting server) due to limited budget.  

This dev environment includes the latest versions of the following software:

- `php:8.2-apache`
- `mysql:latest`
- `phpmyadmin`

## Prerequisites

 - Docker - https://www.docker.com/products/docker-desktop
 - Tested and confirmed working on:	 
	 - Windows 11 Version 22H2 build 22621.2715

## Running the Container

1. Run `docker compose up` from the project directory
    - Note: the above command will only work on versions newer than 3.6. If you are using Docker 3.6 or older, use `docker-compose up`
2. Visit `localhost:8000` in your browser

## Additional Notes
- Docker setup tutorial follow guide from this blog post: https://www.section.io/engineering-education/dockerized-php-apache-and-mysql-container-development-environment/
