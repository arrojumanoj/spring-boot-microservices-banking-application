# Sequence Generator Service

## Introduction
The Sequence Generator Service is a microservice responsible for generating unique sequences for various entities. It provides APIs for generating and retrieving sequences.

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
    - [Generate Sequence](#generate-sequence)
    - [Get Sequence](#get-sequence)
- [Error Handling](#error-handling)
- [Security](#security)
- [Configuration](#configuration)
- [Monitoring](#monitoring)
- [Logging](#logging)
- [Testing](#testing)
- [Build and Deployment](#build-and-deployment)

## Project Structure
The project structure of the Sequence Generator Service is as follows:
```
Sequence Generator Service
|-- src
|   |-- main
|   |   |-- java
|   |   |   \-- com
|   |   |       \-- example
|   |   |           \-- sequencegenerator
|   |   |               |-- controller
|   |   |               |   \-- SequenceGeneratorController.java
|   |   |               |-- model
|   |   |               |   \-- Sequence.java
|   |   |               |-- repository
|   |   |               |   \-- SequenceRepository.java
|   |   |               |-- service
|   |   |               |   \-- SequenceGeneratorService.java
|   |   |               \-- SequenceGeneratorServiceApplication.java
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

### Generate Sequence
- **URL:** `/sequences`
- **Method:** `POST`
- **Description:** Generates a new sequence.
- **Request Body:**
    ```json
    {
        "entityName": "string"
    }
    ```
- **Response:**
    ```json
    {
        "entityName": "string",
        "sequenceValue": "number"
    }
    ```

### Get Sequence
- **URL:** `/sequences/{entityName}`
- **Method:** `GET`
- **Description:** Retrieves the current sequence value for the specified entity.
- **Response:**
    ```json
    {
        "entityName": "string",
        "sequenceValue": "number"
    }
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
The Sequence Generator Service uses Spring Security to secure the API endpoints. Authentication and authorization are handled using JWT (JSON Web Tokens).

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

## About the Maintainer

This project is actively maintained by Manoj Kumar Arroju. Manoj is a Software Developer with a strong background in Java, Python, and distributed systems, specializing in building scalable microservices and RESTful APIs. He is dedicated to ensuring the continued development and stability of this service.

You can connect with Manoj here:
- GitHub: [arrojumanoj](https://github.com/arrojumanoj)
- LinkedIn: [Manoj Kumar Arroju](https://linkedin.com/in/manoj-kumar-arroju)
- Email: arrojumanoj1483@gmail.com