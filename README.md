# Set up an Odoo 17 instance using Docker and Docker Compose

This repository contains the configuration to set up an Odoo 17 instance with PostgreSQL using Docker and Docker Compose.

## Prerequisites

- Docker installed on your machine.
- Docker Compose installed on your machine.

## Project Structure

```
.
├── Dockerfile
├── docker-compose.yml
├── customs/
└── odoo.conf
```

- `Dockerfile`: The Dockerfile to build the Odoo web service.
- `docker-compose.yml`: The Docker Compose file to define and run the multi-container Docker application.
- `customs/`: A directory for custom modules and addons.
- `odoo.conf`: The configuration file for Odoo.

## Configuration

### docker-compose.yml

- Defines two services: db (PostgreSQL) and odoo_web (Odoo).
- Specifies ports for each service.
- Defines environment variables for database configuration.
- Mounts volumes for persistent storage.

### odoo.conf

Ensure that your `odoo.conf` file contains the correct database settings

## Setup Instructions

### Clone the Repository

Clone this repository to your local machine using:
```bash
git clone https://github.com/AhmedHoussamBouzine/odoo-17-docker-compose.git
```

### Build the Containers

Build and start the services defined in the `docker-compose.yml` file:

```bash
docker compose up -d
```
This will pull the required images, build the Odoo image from the Dockerfile.

### Start the Containers

```bash
docker compose up
```
### Access Odoo

Open your web browser and go to `http://localhost:8069`. You should see the Odoo setup page.
