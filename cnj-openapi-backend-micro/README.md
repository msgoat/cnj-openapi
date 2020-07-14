# cnj-openapi-backend-micro

Cloud native JavaEE backend based on Eclipse MicroProfile using MP OpenAPI feature to document REST APIs.

## Build this application 

``` 
mvn clean verify -P pre-commit-stage
```

Build results: a Docker image containing an Payara MicroProfile application.

## Exposed REST endpoints

Simply call the OpenAPI REST endpoint at `/openapi` to get an OpenAPI compliant API specification.

## Exposed environment variables

| Name | Required | Description |
| --- | --- | --- |
| MP_JWT_VERIFY_PUBLICKEY_LOCATION | x | REST endpoint of an OpenID Connect authentication provider returning the JWT key set |
| MP_JWT_VERIFY_ISSUER | x | ID of the JWT's issuer |
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
