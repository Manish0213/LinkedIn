# LinkedIn Clone – Microservices Architecture

## Tech Stack

- **Java 17**
- **Spring Boot**
- **Spring Cloud Gateway** – Centralized API routing
- **Spring Eureka Discovery Server** – Service registry and discovery
- **Kafka** – Real-time communication and event streaming
- **Neo4j** – Graph database for managing user connections
- **PostgreSQL / MySQL** – For relational data (User, Post, etc.)
- **JWT** – Authentication and authorization

---

## Modules

### 1. USER-SERVICE
- Handles user **signup** and **login**
- Stores user credentials and profile information

### 2. POST-SERVICE
- Allows users to **create posts**
- Supports **like/unlike** functionality

### 3. CONNECTION-SERVICE
- **Send, accept, and reject** connection requests
- Uses **Neo4j** to manage and query **first-degree connections**

### 4. NOTIFICATION-SERVICE
- Listens to **Kafka events**:
  - Post creation
  - Post like
  - Connection request sent/accepted
- Sends **real-time notifications**

### 5. API-GATEWAY
- Acts as **central entry point** for all services
- Performs **authentication using JWT**
- Routes requests to appropriate microservice

### 6. DISCOVERY-SERVICE
- **Registers all microservices**
- Provides **dynamic service discovery**

---

## Features

- Secure JWT-based authentication
- Create and like posts
- Send, accept, and reject connection requests
- Use Neo4j to get first-degree connections
- Real-time notifications via Kafka
- Centralized routing with Spring Cloud Gateway
- Modular and scalable microservices architecture

---
