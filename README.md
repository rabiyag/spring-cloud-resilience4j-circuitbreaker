
# Spring Cloud Resilience4j Circuit Breaker

This project demonstrates how to use **Spring Cloud** with **Resilience4j** to implement a **Circuit Breaker** pattern in a Spring Boot application. The circuit breaker helps manage failures in microservices by preventing calls to a failing service and providing fallback logic.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Running the Application](#running-the-application)
- [Usage](#usage)

## Features
- Circuit Breaker implementation using **Resilience4j**.
- Integration with **Spring Cloud** for microservice resilience.
- Custom fallback methods for handling service failures.
- Monitoring and configuration of circuit breakers via **Spring Boot Actuator**.

## Technologies Used
- **Spring Boot**
- **Spring Cloud**
- **Resilience4j** for Circuit Breaker
- **Spring Boot Actuator** for monitoring

## Project Structure
```
src/main/java
    ├── config          # Resilience4j configuration
    ├── controller      # Controller handling the API requests
    ├── service         # Service with business logic and circuit breaker
src/main/resources
    └── application.yml  # Application configuration including circuit breaker settings
```

## Prerequisites
- **JDK 8** or higher
- **Maven** for dependency management
- **Docker** (optional, for running any microservices)

## Setup
1. **Clone the repository**:
   ```bash
   git clone https://github.com/rabiyag/spring-cloud-resilience4j-circuitbreaker.git
   cd spring-cloud-resilience4j-circuitbreaker
   ```

2. **Build the project with Maven**:
   ```bash
   mvn clean install
   ```

3. **Configure application properties**:
   - Modify `src/main/resources/application.yml` for circuit breaker settings.

## Running the Application
1. **Run the application**:
   ```bash
   mvn spring-boot:run
   ```

2. **Access the application**:
   - The application will run on `http://localhost:8080` by default.

## Usage
- The application will use **Resilience4j Circuit Breaker** to manage calls to services.
- You can test the circuit breaker behavior by simulating failures (e.g., by stopping a dependent service).
- The application will fallback to a predefined method in case of failures, demonstrating the resilience pattern.

