# Spring Boot Ticket App

This project is a Spring Boot REST API built with Maven, Spring Web, Spring Data JPA, and MariaDB. It manages help desk tickets with full CRUD endpoints.

## Endpoints

- `GET /tickets`
- `GET /tickets/{id}`
- `POST /tickets`
- `PUT /tickets/{id}`
- `DELETE /tickets/{id}`

## Local Setup

1. Start your local MariaDB server.
2. Create the database:

```sql
CREATE DATABASE IF NOT EXISTS ticketdb;
```

You can also run the script in [database-setup.sql](database-setup.sql).

3. Set database credentials if needed:

```bash
export DB_USERNAME=your_username
export DB_PASSWORD=your_password
```

4. Start the application:

```bash
./mvnw spring-boot:run
```

The API will be available at `http://localhost:8080`.

## Sample Request Body

```json
{
  "title": "Reset employee password",
  "description": "User cannot access the internal portal.",
  "status": "OPEN"
}
```

## Build Verification

This project builds successfully with:

```bash
./mvnw -DskipTests package
```

## Report

Use [POSTMAN-TESTING-REPORT.md](POSTMAN-TESTING-REPORT.md) to add the five required Postman screenshots and the explanation of how JPA simplifies REST development.
