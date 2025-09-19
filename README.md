# Patient Management System (SpringBoot Microservices)

This project is a **microservices-based healthcare system** designed to demonstrate modern architectural practices such as authentication, service-to-service communication, and event-driven processing. At its core, it provides an **Auth Service** for secure user login and token management, a **Patient Service** for managing patient records, and an **Analytics Service** that consumes patient-related events to generate insights. Communication between services is handled through a combination of **gRPC** (for fast, synchronous calls like billing) and **Kafka** (for asynchronous event streaming such as patient activity tracking). An API Gateway serves as the single entry point, routing client requests securely and simplifying access to the underlying services. Each service manages its own database and runs inside isolated **Docker containers**, enabling independent deployment and scalability. Together, these components simulate a real-world healthcare information platform that balances **security, efficiency, and flexibility** in handling patient data and operations.

## Development Architecture

![Dev Architecture_01 drawio](https://github.com/user-attachments/assets/4e95732f-f265-4622-9f7f-bdf717e3e915)
