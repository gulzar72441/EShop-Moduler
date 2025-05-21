# 🛒 eshop-moduler – Modular Monolith Backend in .NET 8

**eshop-moduler** is a modern backend project showcasing how to build a **Modular Monolith** using **.NET 8**, combining principles like **DDD**, **CQRS**, **Vertical Slice Architecture**, and **Outbox Pattern** with cloud-native backing services.

---

## 📦 Modules

- **Catalog**: Minimal APIs, EF Core, CQRS, FluentValidation, Carter
- **Basket**: Redis caching, Proxy & Decorator patterns, MassTransit, Outbox Messaging
- **Identity**: Keycloak for OAuth2 & OIDC, JWT Authentication
- **Ordering**: Clean Architecture, DDD, CQRS, Outbox Pattern

---

## 🧱 Architectural Highlights

- Modular Monolith (Modulith) Structure
- Vertical Slice Architecture (VSA)
- Domain-Driven Design (DDD)
- CQRS with MediatR
- Outbox Pattern for Reliable Event Messaging
- RabbitMQ for asynchronous inter-module communication
- Redis as Distributed Cache
- PostgreSQL with schema-per-module isolation
- Keycloak for centralized identity management

---

## 🔁 Communication Flow

- **Catalog ↔ Basket**: Sync via in-process APIs
- **Catalog ↔ Basket**: Async events via RabbitMQ
- **Basket → Ordering**: Event-driven ordering flow

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Visual Studio 2022
- .NET 8 SDK
- Docker Desktop

### ⚙️ Setup Instructions

1. Clone the repository:
   git clone https://github.com/gulzar72441/EShop-Moduler.git
   cd eshop-moduler
Start Docker Desktop and ensure:

Memory: 4 GB

CPUs: 2

Run the solution:

Set docker-compose as the startup project in Visual Studio

Or run via CLI:

docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
Wait for all containers to initialize.

🔍 API Testing
Base URL: https://localhost:6060

Use the provided Postman collection to test all internal module APIs.

🔄 Migration Ready
This project is structured to support smooth transition from Modular Monolith to Microservices using the Strangler Fig Pattern.

👨‍💻 Author
Gulzar Ahmad Bilal