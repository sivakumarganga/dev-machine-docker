# SonarQube & Database (Postgresql) powered by compose
* Quick Setup for SonarQube and Postgresql

## Requirements:
* docker >= 25.0.3+
* docker-compose

## Quick Start
* Run this command `docker-compose up -d`


## Environments
This Compose file contains the following environment variables:

* `SONAR_JDBC_URL` the default value is **jdbc:postgresql://db:5432/sonar**
*  `SONAR_JDBC_USERNAME` the default value is **sonar**
* `SONAR_JDBC_PASSWORD` the default value is **sonar**
 #Postgresql
* `POSTGRES_USER` the default value is **sonar**
* `POSTGRES_PASSWORD` the default value is **sonar**

## Access to sonarqube: 
* `http://localhost:9000`
* **Username:** admin (as a default)
* **Password:** admin (as a default)

## Access to postgres: 
* `http://localhost:5432`
* **Username:** sonar (as a default)
* **Password:** sonar (as a default)


## Logging

There are no easy way to configure pgadmin log verbosity and it can be overwhelming at times. It is possible to disable pgadmin logging on the container level.

Add the following to `pgadmin` service in the `docker-compose.yml`:

```
logging:
  driver: "none"
```