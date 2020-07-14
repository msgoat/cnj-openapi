# cnj-openapi

Showcase of a simple cloud native Java application documenting REST APIs with [OpenAPI](https://swagger.io/specification/).

The actual documentation of REST APIs with OpenAPI is demonstrated with different Java backend technologies:

* Java EE (see: [cnj-openapi-backend-javaee](cnj-openapi-backend-javaee/README.md))
* Eclipse MicroProfile (see: [cnj-openapi-backend-micro](cnj-openapi-backend-micro/README.md))
* Spring Boot (see: [cnj-openapi-backend-spring](cnj-openapi-backend-spring/README.md))
* Quarkus (see: [cnj-openapi-backend-quarkus](cnj-openapi-backend-quarkus/README.md))

All applications are using a common downstream service [cnj-openapi-downstream-spring](cnj-openapi-downstream-spring/README.md)

## Status
![Build status](https://drone.at.automotive.msg.team/api/badges/msgoat/cnj-openapi/status.svg)

## Build this showcase 

### Prerequisites

In order to run the build, you have to install the following tools locally:
* Docker
* Docker Compose 
* Maven
* Java JDK 11   

### Run Maven

You can build all showcase applications by running Maven:
```
mvn clean install -P pre-commit-stage
```

The Maven build will create Docker images for all showcase applications and run system tests on them.