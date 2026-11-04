# Library API

IN3101 Lab Sheet 01 and Lab Sheet 02 Spring Boot REST API using Java 21,
Spring Boot 4, Spring Data JPA, MySQL, and Swagger UI.

## Requirements

- Java 21
- MySQL Server on port 3306
- Maven Wrapper

## Database setup

```sql
DROP DATABASE IF EXISTS library_db;
CREATE DATABASE library_db;
SHOW DATABASES;
```

Set the root password in the terminal without putting it in source control:

```powershell
$env:DB_PASSWORD = "your-local-mysql-password"
```

## Run

```powershell
.\mvnw.cmd clean compile
.\mvnw.cmd spring-boot:run
```

The API is available at `http://localhost:8085`.

Swagger UI: `http://localhost:8085/swagger-ui.html`  
OpenAPI JSON: `http://localhost:8085/v3/api-docs`

## API examples

Create a book with `POST http://localhost:8085/api/books`:

```json
{
  "title": "Enterprise Applications 234109F",
  "author": "Lab Author",
  "isbn": "1234567890",
  "price": 100.0
}
```
