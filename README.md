# Docker Compose WordPress Setup

Welcome to the **wordpress-with-docker-compose** repository! This repository contains a Docker Compose setup that allows you to easily run a WordPress website, along with a MariaDB database and an Nginx reverse proxy. This setup is perfect for local development and testing purposes.

## Prerequisites

Before you begin, make sure you have the following installed on your system:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Clone this repository to your local machine:
     
     git clone https://github.com/islam286/wordpress-with-docker-compose.git

### 2. Navigate to the cloned directory:

  
     cd wordpress-with-docker-compose
### 3. Create a .env file based on the provided .env.template:

     cp .env.template .env
### 4. Edit the .env file and replace the placeholders with your actual secret values.

### 5. Start the services using Docker Compose:


    docker-compose up -d

This will launch the WordPress, MariaDB, and Nginx containers in the background.

Access the WordPress site in your web browser:

- WordPress Site: http://localhost
- Admin Dashboard: http://localhost/wp-admin

When you're done, you can stop the services:


    docker-compose down

## Files

- docker-compose.yaml: Defines services, environment variables, and volumes for the containers.
- nginx.conf: Configuration file for Nginx reverse proxy, directing requests to the WordPress backend.
- .env.template: Template for environment variables. Copy this to .env and replace placeholders with actual secret values.

## Notes

This setup is intended for local development and testing, not for production use.
Always prioritize security by keeping your secrets and sensitive information safe. Do not commit actual secrets to version control.
