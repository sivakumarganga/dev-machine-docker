# Postgresql & PgAdmin powered by compose
* Quick Setup for Postgresql and PgAdmin

## Requirements:
* docker >= 25.0.3+
* docker-compose

## Quick Start
* Clone or download this repository
* Go inside of directory,  `cd compose-postgres`
* Run this command `docker-compose up -d`


## Environments
This Compose file contains the following environment variables:

* `POSTGRES_USER` the default value is **techdev**
* `POSTGRES_PASSWORD` the default value is **techdev123**
* `PGADMIN_DEFAULT_EMAIL` the default value is **techdev@gmail.com**
* `PGADMIN_DEFAULT_PASSWORD` the default value is **techdev123**

## Access to postgres: 
* `localhost:5432`
* **Username:** techdev (as a default)
* **Password:** techdev123 (as a default)

## Access to PgAdmin: 
* **URL:** `http://localhost:8888`
* **Username:** techdev@gmail.com (as a default)
* **Password:** techdev123 (as a default)

## Add a new server in PgAdmin:
* **Host name/address** `postgresdb_docker` as named in service 
* **Port** `5432`
* **Username** as `POSTGRES_USER`, by default: `techdev`
* **Password** as `POSTGRES_PASSWORD`, by default `techdev123`

## Logging

There are no easy way to configure pgadmin log verbosity and it can be overwhelming at times. It is possible to disable pgadmin logging on the container level.

Add the following to `pgadmin` service in the `docker-compose.yml`:

```
logging:
  driver: "none"
```