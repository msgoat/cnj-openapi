# cnj-openapi-backend-javaee

Cloud native JavaEE backend based on JavaEE Full Profile Application Server using MP OpenAPI feature to document REST APIs.

Since the JavaEE showcase does not differ from the MicroProfile showcase, 
this JavaEE showcase demonstrates the usage of a static OpenAPI YAML file located at `/META-INF/openapi.yaml`.

## Build this application 

``` 
mvn clean verify -P pre-commit-stage
```

Build results: a Docker image containing an Payara Full Profile application server plus the deployed application.

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
