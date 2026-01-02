# 🎟️ Ticketing System – Microservices with Spring Boot, Kafka, Keycloak and Resilience4j

Personal project developed to study and practice **microservices architecture**, **event-driven systems**, **fault tolerance**, and **secure API design** using modern Spring technologies.

The system simulates a **real-world ticket booking workflow**, using asynchronous processing with Kafka, distributed inventory management, authentication with Keycloak (JWT), and **resilience mechanisms with Resilience4j**.

---

## 📌 Overview

The Ticketing System is composed of **four independent microservices**, each with a clear responsibility, following principles of:

- Low coupling  
- Event-driven architecture  
- Scalability and resilience  
- Separation of concerns  

Communication between services happens through:
- **Synchronous REST (HTTP)** for queries
- **Asynchronous messaging (Kafka)** for order processing

---

## 🧰 Technologies Used

- Java 21
- Spring Boot
- Spring Cloud Gateway (MVC)
- Resilience4j
- Apache Kafka
- Zookeeper
- Keycloak
- MySQL
- Flyway
- Docker & Docker Compose
- Springdoc OpenAPI (Swagger)

---

## ▶️ How to Run the Project

### Prerequisites

- Java 21
- Docker and Docker Compose

---

### Step 1 – Start Infrastructure

From the **inventory-service** directory, where the `docker-compose.yml` file is located, run:

```bash
docker-compose up
```
---

This step will start the following services:

- **MySQL**
- **Kafka and Zookeeper**
- **Kafka UI**
- **Schema Registry**
- **Keycloak**

---

### Step 2 – Run the Microservices

After the infrastructure is running, start the services **locally** (IDE or terminal):

- **inventory-service**
- **order-service**
- **booking-service**
- **api-gateway**

Each service runs as a **Spring Boot application** using **Java 21**.

---

### Step 3 – Access the APIs

You can interact with the system in the following ways:

- **Direct access** using the services’ default REST endpoints
- **Secured access via API Gateway**, authenticating with **Keycloak** and using a **JWT token**
