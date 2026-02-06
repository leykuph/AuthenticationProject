# Authentication Project

A secure, full-stack web application featuring Spring Boot for the backend and a modern HTML/CSS/JS frontend. It implements JWT-based authentication with a premium, responsive UI.

## Features

- **Authentication**: Secure user registration and login with JWT (JSON Web Tokens).
- **Validation**: Robust input validation with stackable error toast notifications.
- **Security**: Password encryption using BCrypt, protected API endpoints.
- **UI/UX**: Modern, responsive dark-themed interface with glassmorphism effects.
- **Tech Stack**:
  - **Backend**: Java, Spring Boot, Spring Security, Spring Data JPA, PostgreSQL.
  - **Frontend**: HTML5, Vanilla JS, CSS3 (JetBrains Mono font).

## Prerequisites

- Java 17 or higher
- Maven
- PostgreSQL

## Configuration

1.  **Database**: Ensure PostgreSQL is running and you have a database named `loginapp`.
2.  **Properties**: Update `src/main/resources/application.properties` if your DB credentials differ from the defaults:
    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/loginapp
    spring.datasource.username=postgres
    spring.datasource.password=password
    ```

## Running the Application

1.  **Build the project**:

    ```bash
    mvn clean install
    ```

2.  **Run the application**:

    ```bash
    mvn spring-boot:run
    ```

3.  **Access the App**:
    Open your browser and navigate to: [http://localhost:8080/index.html](http://localhost:8080/index.html)

## API Endpoints

| Method | Endpoint          | Description                     |
| :----- | :---------------- | :------------------------------ |
| `POST` | `/users/register` | Register a new user             |
| `POST` | `/users/login`    | Login and receive JWT           |
| `GET`  | `/users/me`       | Get current user info (Secured) |

## Project Structure

- `src/main/java`: Backend source code.
- `src/main/resources/static`: Frontend assets (HTML, CSS, JS).
