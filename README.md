# Jira Software with PostgreSQL - Docker Compose

## Overview
This repository provides a Docker Compose setup to run Atlassian Jira Software with a PostgreSQL database.

## Prerequisites
- Docker
- Docker Compose

## Services
This setup includes two services:
- **Jira**: Runs Atlassian Jira Software 9.17.5.
- **PostgreSQL**: Runs PostgreSQL 15.8 as the database backend.

## Configuration
### Volumes
- `./jira-var`: Stores Jira application data.
- `./jira-opt/server.xml`: Contains Jira's Tomcat server configuration.
- `./postgresqldata`: Stores PostgreSQL database data.

### Environment Variables
- **Jira**:
  - `CATALINA_OPTS`: Configures JVM settings, including heap size and enabling plugin uploads.
- **PostgreSQL**:
  - `POSTGRES_USER`: Database user for Jira.
  - `POSTGRES_PASSWORD`: Password for the Jira database user.
  - `POSTGRES_DB`: Name of the Jira database.
  - `POSTGRES_ENCODING`: Sets the database encoding to UTF-8.

## Ports
- Jira: `8080:8080`
- PostgreSQL: `5432:5432`

## Usage
1. Clone this repository:
   ```sh
   git clone https://github.com/nkuranov/docker-atlassian-jira
   cd docker-atlassian-jira

## Connect
   ```sh
   http://127.0.0.1.8080