# Spring Boot Hello API

A small Java web application built to learn the basics of Spring Boot and HTTP request handling. It exposes a greeting endpoint and runs with an embedded Tomcat server.

## Technologies

- Java 21
- Spring Boot
- Spring Web / Spring MVC
- Maven Wrapper
- Embedded Tomcat

## Endpoint

| Method | Path | Response |
| --- | --- | --- |
| GET | `/hello` | `Hello World! Welcome Spring Boot` |

Open `http://localhost:8080/hello` in your browser while the application is running.

The root path `/` has no custom endpoint and returns HTTP 404.

## Run locally

Install JDK 21 and open a terminal in the project root, where `pom.xml` is located. A separate Maven installation is not required because the project includes Maven Wrapper.

**Windows PowerShell**

```powershell
.\mvnw.cmd spring-boot:run
```

**macOS / Linux**

```bash
./mvnw spring-boot:run
```

By default, the application listens on port `8080`. Stop it with `Ctrl+C`. In a Windows terminal, answer `Y` if prompted to terminate the batch job.

After changing Java code, save the file and restart the application to load the changes. Automatic restart is not configured in this project.

## Key files

| File or directory | Purpose |
| --- | --- |
| `src/main/java/com/example/springboot_demo/SpringbootDemoApplication.java` | Application entry point |
| `src/main/java/com/example/springboot_demo/HelloController.java` | Handles the greeting request |
| `src/main/resources/application.properties` | Application configuration |
| `pom.xml` | Maven dependencies and build configuration |
| `mvnw`, `mvnw.cmd`, `.mvn/` | Maven Wrapper |
| `target/` | Generated build output; excluded from version control |

## What I practiced

- Creating and running a Spring Boot project
- Mapping a GET request with `@GetMapping`
- Returning a response using `@RestController`
- Understanding the role of the embedded web server
- Using Maven Wrapper and restarting the application after code changes

## Scope

This is a learning project with one greeting endpoint. It does not currently include a database, authentication, or a separate frontend.
