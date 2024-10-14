# Food Ordering System

## Overview

The **Food Ordering System** is a microservice-based application designed using Hexagonal Architecture and Domain-Driven Design (DDD) principles. It leverages Spring Boot, Kafka, and PostgreSQL for scalability and reliability, with Docker and Kubernetes for containerization and orchestration. The system handles food orders from customers, processing them through different services and ensuring data consistency through Saga and Outbox patterns.

## Table of Contents
- [Features](#features)
- [System Architecture](#system-architecture)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)

## Features

- **Microservice Architecture**: Independent services for order, payment, restaurant, and customer.
- **Hexagonal Architecture (Ports & Adapters)**: Ensures loose coupling between services.
- **Domain-Driven Design (DDD)**: Organizes code into clearly defined domains, enhancing maintainability.
- **Saga Pattern**: Handles long-running transactions across services using distributed coordination.
- **Outbox Pattern**: Ensures reliable message delivery between microservices using Kafka.
- **Event-Driven Architecture**: Services communicate asynchronously using Kafka.
- **PostgreSQL**: Centralized database for persisting order and customer information.
- **Docker**: Containerization of each microservice.
- **Kubernetes**: Orchestration of containers for scaling and management.

## System Architecture

The Food Ordering System consists of the following microservices:

1. **Order Service**: Manages customer orders, including creation, status updates, and completion.
2. **Payment Service**: Handles payment processing and integration with external payment providers.
3. **Restaurant Service**: Manages restaurant information, menu items, and their availability.
4. **Customer Service**: Manages customer profiles, preferences, and history.

Each service communicates with others asynchronously via **Kafka** to maintain loose coupling and scalability.

## Tech Stack

- **Java 17** and **Spring Boot**
- **Kafka**: For event-driven communication.
- **PostgreSQL**: As the database system.
- **Docker**: For containerization.
- **Kubernetes (K8s)**: For orchestration and deployment.
- **Hexagonal Architecture**: Separation of concerns between domain, application, and infrastructure.
- **Saga and Outbox Pattern**: Ensures transaction consistency across services.

## Project Structure

The project follows a **Hexagonal Architecture**, organized into distinct layers:

1. **Domain Layer**: Contains core business logic and domain models.
2. **Application Layer**: Contains service classes and interfaces for application functionality.
3. **Infrastructure Layer**: Contains adapters, repositories, and configuration (e.g., Kafka, PostgreSQL, etc.).
4. **Ports & Adapters**: Interfaces and implementations for communication with external systems (databases, message brokers, etc.).

