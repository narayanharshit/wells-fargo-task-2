# Wells Fargo Task 2 Starter Repo

Contains Everything you need to get started on task 2 of Forage's Wells Fargo software engineering program.

## Overview

This project implements the data model for the counselor application using Spring Boot. The following entity classes were created:

- `Client`
- `Portfolio`
- `Security`

## Entity Classes

Each entity class is annotated with `@Entity` and follows these guidelines:
- IDs are auto-generated using `@Id` and `@GeneratedValue`.
- Instance variables are annotated with appropriate JPA annotations (`@Column`, `@ManyToOne`, `@OneToMany`, etc.).
- Each class has a constructor initializing all instance variables.
- Each class has getters and setters for all instance variables except the ID.

## H2 Database Configuration

The H2 in-memory database is configured in `application.properties`. Here are the details:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update
