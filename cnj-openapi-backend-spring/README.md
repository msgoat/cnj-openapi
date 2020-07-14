# cnj-openapi-backend-spring

Cloud native Java backend based on Spring Boot using Spring Docs to document REST APIs with OpenAPI.

## Build this application 

``` 
mvn clean verify -P pre-commit-stage
```

Build results: a Docker image containing a Spring Boot application.


## Exposed REST endpoints

Simply call the OpenAPI REST endpoint at `/openapi` to get an OpenAPI compliant API specification.

## Exposed environment variables

| Name | Required | Description |
| --- | --- | --- |
| SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_JWK_SET_URI | x | OpenID Connect Provider endpoint to retrieve key set to verify JWT token signatures |
| SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_ISSUER_URI | x | Expected JWT Issuer URI |
| CLOUDTRAIN_SERVICES_GRANTEDPERMISSIONS_MP_REST_URL | x | Base URL of the downstream service | 
| CLOUDTRAIN_COMMON_REST_TRACE_ENABLED |  | true, if the REST trace should be enabled; false otherwise (default: false) |

## Exposed Ports

| Port | Protocol | Description |
| --- | --- | --- |
| 8080 | HTTP | HTTP endpoint of this application | 
 
## Version / Tags

| Tag(s) | Remarks |
| --- | --- |
| latest, 4.0.0 | first release |
