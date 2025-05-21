# 🛒 eshop-moduler – Modular Monolith Backend in .NET 8

**eshop-moduler** is a modern backend project showcasing how to build a **Modular Monolith** using **.NET 8**, combining principles like **DDD**, **CQRS**, **Vertical Slice Architecture**, and **Outbox Pattern** with cloud-native backing services.

<img src="https://sdmntprsouthcentralus.oaiusercontent.com/files/00000000-cf14-61f7-b19c-4f374fe3496d/raw?se=2025-05-21T11%3A11%3A18Z&sp=r&sv=2024-08-04&sr=b&scid=24a95671-bc21-5e1b-8c56-103be464cc7d&skoid=bbd22fc4-f881-4ea4-b2f3-c12033cf6a8b&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-05-20T22%3A32%3A44Z&ske=2025-05-21T22%3A32%3A44Z&sks=b&skv=2024-08-04&sig=tAk48GrOcY461GDpK5Co198uZcoln/bHt9CyEHoYLDY%3D" alt="Sample Image" width="900"/>
 
 
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
