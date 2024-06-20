# JWT Authentication with Spring Boot and Spring Security

This project is a simple demonstration of how to implement JWT (JSON Web Token) authentication using Spring Boot and Spring Security.

## Features

- User Registration
- User Authentication
- Protected Endpoints

## Prerequisites

- Java 21
- Maven or Gradle
- Postman (for testing the API)

## Dependencies

The project uses the following dependencies:

1. **Spring Boot Starter Data JPA**
2. **Spring Boot Starter Security**
3. **Spring Boot Starter Web**
4. **PostgreSQL Driver**
5. **Project Lombok**
6. **JJWT API (version 0.11.5)**
7. **JJWT Implementation (version 0.11.5)**
8. **JJWT Jackson (version 0.11.5)**
9. **Spring Boot Starter Test** (for testing)
10. **Spring Security Test** (for testing)

## Getting Started

### Installation

1. Clone the repository:
    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Build the project using Maven or Gradle:
    ```sh
    mvn clean install
    ```
   or
    ```sh
    ./gradlew build
    ```

### Running the Application

1. Run the application:
    ```sh
    mvn spring-boot:run
    ```
   or
    ```sh
    ./gradlew bootRun
    ```

2. Open Postman and create the following endpoints for testing:

    - **Register a new user:**
        - URL: `http://localhost:8080/api/v1/auth/register`
        - Method: `POST`
        - Body (JSON):
            ```json
            {
                "firstName": "daffa",
                "lastName": "fathoni",
                "email": "daffafathoni@gmail.com",
                "password": "daprut"
            }
            ```

    - **Authenticate the user:**
        - URL: `http://localhost:8080/api/v1/auth/authenticate`
        - Method: `POST`
        - Body (JSON):
            ```json
            {
                "email": "daffafathoni@gmail.com",
                "password": "daprut"
            }
            ```

    - **Access a protected endpoint:**
        - URL: `http://localhost:8080/api/v1/demo-controller`
        - Method: `GET`
        - Authorization: Bearer Token (use the token from the authenticate response)

## Reference

This project is based on the tutorial by [Amigoscode](https://youtu.be/KxqlJblhzfI?si=4WcmR5Zl8TsCNX4q).
