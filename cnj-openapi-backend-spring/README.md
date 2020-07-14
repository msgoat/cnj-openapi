# cnj-openapi-backend-spring

Cloud native Java backend based on Spring Boot using Spring WEB MVC to expose and consume REST endpoints.

## Build this application 

``` 
mvn clean verify -P pre-commit-stage
```

Build results: a Docker image containing a Spring Boot application.

## Exposed REST endpoints

### /api/v1/tasks

Manages Task entities.

Method
: GET

URI
: /api/v1/tasks

Parameter(s)
: none

Response
: all existing Task entities

Authentication type
: Bearer Token

Role(s) required
: CLOUDTRAIN_USER

Method
: GET

URI
: /api/v1/tasks/{taskId}

Parameter(s)
: task ID as last path component

Response
: (200) Task identified by the given task ID or (404) if no Task with the given task ID can be found

Authentication type
: Bearer Token

Role(s) required
: CLOUDTRAIN_USER

Method
: POST

URI
: /api/v1/tasks

Parameter(s)
: Task as request body

Response
: (201) Location of newly created Task

Authentication type
: Bearer Token

Role(s) required
: CLOUDTRAIN_USER

Method
: PUT

URI
: /api/v1/tasks/{taskId}

Parameter(s)
: task ID of task to save as last path component plus Task to save as request body

Response
: (204) if Task could be saved successfully

Authentication type
: Bearer Token

Role(s) required
: CLOUDTRAIN_USER

Method
: DELETE

URI
: /api/v1/tasks/{taskId}

Parameter(s)
: task ID of Task to delete as last path component

Response
: (204) if Task could be deleted successfully

Authentication type
: Bearer Token

Role(s) required
: CLOUDTRAIN_USER

## Exposed environment variables

| Name | Required | Description |
| --- | --- | --- |
| SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_JWK_SET_URI | x | OpenID Connect Provider endpoint to retrieve key set to verify JWT token signatures |
| SPRING_SECURITY_OAUTH2_RESOURCESERVER_JWT_ISSUER_URI | x | Expected JWT Issuer URI |


## Exposed Ports

| Port | Protocol | Description |
| --- | --- | --- |
| 8080 | HTTP | HTTP endpoint of this application | 
 
## Version / Tags

| Tag(s) | Remarks |
| --- | --- |
| latest, 4.0.0 | first release |