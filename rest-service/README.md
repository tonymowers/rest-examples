# REST Service Example

Simple REST hello world greeting implemented with Spring Boot.


## Run application using

```
./mvnw spring-boot:run
```

## Accessing Swagger API documentation

```
http://localhost:8080/swagger-ui.html
```

## Using Application via curl 

### __Greetings__ API Examples

```
curl -i \
    -u username:password \
    -H "Accept-Language: fr" \
    -H "Accept: application/xml" \
    http://localhost:8080/greeting?name=Bob
``` 

```
curl http://localhost:8080/greeting/Bob
``` 

### __Users__ API Examples

Get list of all users
```
curl -u username:password http://localhost:8080/users
```

Get a single user
```
curl -u username:password http://localhost:8080/users/2
```

Create a single user
```
curl -i -u username:password \
-d '{"name" : "Lex Mowers", "birthDate":"2019-10-29T19:58:36.290+0000"}' \
-H "Content-Type: application/json" -X POST http://localhost:8080/users
```

## Actuator Examples

```
http://localhost:8080/browser/index.html#/actuator
http://localhost:8080/browser/index.html#/users/1
```