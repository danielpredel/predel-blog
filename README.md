# PreDel Blogging Platform

## Overview

Personal project (Jun 2024 - Sep 2024) consisting of a full-stack blogging platform composed of a REST API and an Angular client application.

This repository provides a Docker Compose setup to orchestrate the full system, including:

* Backend API (Node.js / Express)
* Frontend client (Angular)
* MongoDB database

The services are built from their respective repositories and configured to run together in a local environment.

## Related Repositories

* API: [https://github.com/danielpredel/predel-blog-api.git](https://github.com/danielpredel/predel-blog-api.git)
* Client: [https://github.com/danielpredel/predel-blog-client.git](https://github.com/danielpredel/predel-blog-client.git)

## Features

* Containerized full-stack application
* Service orchestration via Docker Compose
* Integrated frontend and backend communication
* Persistent data storage with MongoDB
* Environment-based configuration

## Project Structure

```
.
├── docker-compose.yml     # Service orchestration
└── README.md
```

## Environment Variables

This project requires a `.env` file in the root directory with the following variables:

```
# App Configs
ENV=
PORT=
SECRET_KEY=

# Mail service (optional / not implemented)
EMAIL_ADDRESS=
EMAIL_PASSWORD=

# Database
MONGO_USER=
MONGO_PASSWORD=
MONGO_DB=
```

### Notes on configuration

* Mail service variables are defined for future integration but are not currently used
* Database credentials are consumed by the MongoDB container and API service
* Application variables are shared across services where required

## Usage

From the root directory:

```
docker compose up --build
```

This will:

* Build the API and client images from their respective repositories
* Start all services
* Expose the application locally

The application will be available at:

```
http://localhost:8080
```

## Notes

* This repository is the intended entry point for running the full application
* Individual services (API and client) are not designed to run independently
* Configuration is environment-driven via `.env`
* Partial implementation: some backend features and integrations (email service, profile page) are not completed

## Project Status

Archived – no active development.
Maintained as a portfolio project.
