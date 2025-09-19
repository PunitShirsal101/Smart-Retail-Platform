# Smart Retail Platform

A cloud-native microservices-based retail system built with Spring Boot, Kafka, Consul, and PostgresSQL. This platform demonstrates enterprise-grade architecture with API Gateway, centralized configuration, service discovery, and real-time messaging.

---

## Architecture Overview

[Client] → [API Gateway] → [Microservices] ↘ [Consul Discovery] ↘ [Config Server (Consul KV)]


### Microservices

| Service                | Description                      | DB          | Messaging | Caching |
|------------------------|----------------------------------|-------------|-----------|---------|
| `user-service`         | Authentication & user management | PostgresSQL | —         | Redis   |
| `product-service`      | Product catalog & inventory      | PostgresSQL | Kafka     | Redis   |
| `order-service`        | Order placement & tracking       | PostgresSQL | Kafka     | Redis   |
| `payment-service`      | Payment gateway integration      | —           | Kafka     | Redis   |
| `notification-service` | Kafka-based alerts & logging     | MongoDB     | Kafka     | —       |

---

## Technologies Used

- **Backend**: Java 21, Spring Boot, Spring Security, Spring Data JPA
- **Architecture**: Microservices, REST APIs, Kafka, Consul
- **Databases**: PostgresSQL, MongoDB, Redis
- **Messaging**: Apache Kafka
- **DevOps**: Docker, Maven, Jenkins
- **Testing**: JUnit, Mockito
- **Version Control**: GitHub

---

## Prerequisites

- Docker & Docker Compose
- Java 21
- Maven
- Git

---

## Setup Instructions

### 1. Clone the Repository

```bash
    git clone https://github.com/PunitShirsal101/smart-retail-platform.git
    cd smart-retail-platform
```

### 2. Start Infrastructure
```bash
    docker-compose up -d
```


