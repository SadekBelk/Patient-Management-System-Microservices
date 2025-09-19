# Patient Management System (SpringBoot Microservices)

This project is a **microservices-based healthcare system** designed to demonstrate modern architectural practices such as authentication, service-to-service communication, and event-driven processing. At its core, it provides an **Auth Service** for secure user login and token management, a **Patient Service** for managing patient records, and an **Analytics Service** that consumes patient-related events to generate insights. Communication between services is handled through a combination of **gRPC** (for fast, synchronous calls like billing) and **Kafka** (for asynchronous event streaming such as patient activity tracking). An API Gateway serves as the single entry point, routing client requests securely and simplifying access to the underlying services. Each service manages its own database and runs inside isolated **Docker containers**, enabling independent deployment and scalability. Together, these components simulate a real-world healthcare information platform that balances **security, efficiency, and flexibility** in handling patient data and operations.

## Development Architecture

![Animation](https://github.com/user-attachments/assets/c06d8ecd-fcbf-45f3-be78-7cf016b36d66)

# Patient Service
# Billing Service
# Auth Service
# Analytics Service
# Detailed instructions on how to set up and install the project locally
## patient-service-db
The first step is to create a Docker container using the official Postgres image from Docker Hub (**link:** [postgres image](https://hub.docker.com/_/postgres)). When running the container, we need to define a set of environment variables that configure the database (such as username, password, and database name). Next, we should expose the container’s ports by binding them to ports on the host machine, allowing access from our IDE or other applications. After that, we’ll set up bind mounts so that the container can store a copy of its data on our local development machine, ensuring persistence across container restarts. Finally, we’ll connect this container to a Docker network so that it can communicate with other containers running on the same network.

**Setup steps:**

1. Pull the container image from Docker Hub.

2. Define the required environment variables.

3. Bind the container’s ports to the host machine.

4. Configure bind mounts for persistent storage.

5. Add the container to a Docker network for inter-container communication.

### Environment Variables

```
POSTGRES_DB=db;
POSTGRES_PASSWORD=password;
POSTGRES_USER=admin_user
```
