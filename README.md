# Patient Management System (SpringBoot Microservices)

This project is a **microservices-based healthcare system** designed to demonstrate modern architectural practices such as authentication, service-to-service communication, and event-driven processing. At its core, it provides an **Auth Service** for secure user login and token management, a **Patient Service** for managing patient records, and an **Analytics Service** that consumes patient-related events to generate insights. Communication between services is handled through a combination of **gRPC** (for fast, synchronous calls like billing) and **Kafka** (for asynchronous event streaming such as patient activity tracking). An API Gateway serves as the single entry point, routing client requests securely and simplifying access to the underlying services. Each service manages its own database and runs inside isolated **Docker containers**, enabling independent deployment and scalability. Together, these components simulate a real-world healthcare information platform that balances **security, efficiency, and flexibility** in handling patient data and operations.

## Development Architecture

![Animation](https://github.com/user-attachments/assets/c06d8ecd-fcbf-45f3-be78-7cf016b36d66)

# Patient Service
# Billing Service
# Auth Service
# Analytics Service
