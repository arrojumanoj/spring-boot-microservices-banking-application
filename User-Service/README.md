# User Service

## Introduction
The User Service is a microservice responsible for managing user information. It provides APIs for creating, retrieving, updating, and deleting user details.

## Table of Contents
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
    - [Spring Boot](#spring-boot)
    - [Spring Data JPA](#spring-data-jpa)
    - [MySQL](#mysql)
    - [Spring Cloud](#spring-cloud)
    - [Eureka Server](#eureka-server)
    - [Feign Client](#feign-client)
    - [Lombok](#lombok)
- [API Endpoints](#api-endpoints)
    - [Create User](#create-user)
    - [Get User Details](#get-user-details)
    - [Delete User](#delete-user)
    - [Update User](#update-user)
    - [List Users](#list-users)
- [Error Handling](#error-handling)
- [Security](#security)
- [Configuration](#configuration)
- [Monitoring](#monitoring)
- [Logging](#logging)
- [Testing](#testing)
- [Build and Deployment](#build-and-deployment)

## Project Structure
The project structure of the User Service is as follows:
```
User Service
|-- src
|   |-- main
|   |   |-- java
|   |   |   \-- com
|   |   |       \-- example
|   |   |           \-- userservice
|   |   |               |-- controller
|   |   |               |   \-- UserController.java
|   |   |               |-- model
|   |   |               |   \-- User.java
|   |   |               |-- repository
|   |   |               |   \-- UserRepository.java
|   |   |               |-- service
|   |   |               |   \-- UserService.java
|   |   |               \-- UserServiceApplication.java
|   |   \-- resources
|   |       |-- application.properties
|   |       \-- static
|   |           \-- index.html
|-- .gitignore
|-- Dockerfile
|-- mvnw
|-- mvnw.cmd
|-- pom.xml
\-- README.md
```

## Technologies Used

### Spring Boot
Spring Boot is used to create stand-alone, production-grade Spring-based applications. It simplifies the configuration and deployment process by providing a set of default configurations and a wide range of features such as embedded servers, security, and monitoring.

### Spring Data JPA
Spring Data JPA is used for data access and manipulation. It provides a repository abstraction over the JPA (Java Persistence API) and simplifies the implementation of data access layers by reducing boilerplate code.

### MySQL
MySQL is a popular open-source relational database management system. It is widely used for storing and managing data in web applications. When used with Spring Data JPA, MySQL serves as the database where the application's data is persisted. Spring Boot provides easy integration with MySQL through auto-configuration and properties settings, allowing developers to quickly set up and use MySQL in their applications.

### Spring Cloud
Spring Cloud is used for building microservices architectures. It provides tools for configuration management, service discovery, circuit breakers, intelligent routing, and more.

### Eureka Server
Eureka Server is a service registry used for service discovery. It allows microservices to register themselves at runtime and discover other registered services.

### Feign Client
Feign is a declarative web service client. It simplifies the process of making HTTP requests to other microservices by providing a simple and intuitive API.

### Lombok
Lombok is a Java library that helps to reduce boilerplate code by generating common methods like getters, setters, equals, hashCode, and toString at compile time.

## API Endpoints

### Create User
- **URL:** `/users`
- **Method:** `POST`
- **Description:** Creates a new user.
- **Request Body:**
    ```json
    {
        "username": "string",
        "password": "string",
        "email": "string"
    }
    ```
- **Response:**
    ```json
    {
        "userId": "string",
        "username": "string",
        "email": "string",
        "createdDate": "string"
    }
    ```

### Get User Details
- **URL:** `/users/{userId}`
- **Method:** `GET`
- **Description:** Retrieves user details by user ID.
- **Response:**
    ```json
    {
        "userId": "string",
        "username": "string",
        "email": "string",
        "createdDate": "string"
    }
    ```

### Delete User
- **URL:** `/users/{userId}`
- **Method:** `DELETE`
- **Description:** Deletes a user by user ID.
- **Response:** `204 No Content`

### Update User
- **URL:** `/users/{userId}`
- **Method:** `PUT`
- **Description:** Updates user details.
- **Request Body:**
    ```json
    {
        "username": "string",
        "email": "string"
    }
    ```
- **Response:**
    ```json
    {
        "userId": "string",
        "username": "string",
        "email": "string",
        "updatedDate": "string"
    }
    ```

### List Users
- **URL:** `/users`
- **Method:** `GET`
- **Description:** Retrieves a list of all users.
- **Response:**
    ```json
    [
        {
            "userId": "string",
            "username": "string",
            "email": "string",
            "createdDate": "string"
        }
    ]
    ```

## Error Handling
The API uses standard HTTP status codes to indicate the success or failure of an API request. Common status codes include:
- `200 OK` - The request was successful.
- `201 Created` - The resource was successfully created.
- `204 No Content` - The resource was successfully deleted.
- `400 Bad Request` - The request was invalid or cannot be served.
- `404 Not Found` - The requested resource was not found.
- `500 Internal Server Error` - An error occurred on the server.

## Security
The User Service uses Spring Security to secure the API endpoints. Authentication and authorization are handled using JWT (JSON Web Tokens).

## Configuration
The service configuration is managed using Spring Cloud Config, which allows for centralized and externalized configuration management across all microservices.

## Monitoring
Spring Boot Actuator is used for monitoring and managing the application. It provides various endpoints to check the health, metrics, and other operational information of the service.

## Logging
Logging is configured using Logback, which is the default logging framework in Spring Boot. It provides powerful and flexible logging capabilities.

## Testing
JUnit and Mockito are used for unit and integration testing. These frameworks provide a comprehensive set of tools for writing and running tests.

## Build and Deployment
The project uses Maven for build automation and dependency management. The service can be packaged as a Docker container for deployment in a containerized environment.

## Maintainer

This project is actively maintained by Manoj Kumar Arroju.

- **GitHub:** [arrojumanoj](https://github.com/arrojumanoj)
- **LinkedIn:** [Manoj Kumar Arroju](https://linkedin.com/in/manoj-kumar-arroju)
- **Email:** arrojumanoj1483@gmail.com

Manoj is a Software Engineer with a strong foundation in Java, Python, and distributed systems. Experienced in building scalable microservices, RESTful APIs, and backend systems, with skills in cloud infrastructure, containerization, and modern software development practices.