# Architecture

The assessment describes an application using:
- Angular frontend
- Spring Boot backend services
- Kafka messaging
- WebSocket integration for real-time updates
- Docker Compose for local stack execution

The exact module names, endpoints, topics, database configuration, and WebSocket
destinations must be documented from the supplied source code rather than guessed.

## High-level view

    Angular
       |
       | HTTP / WebSocket
       v
    Spring Boot
       |
       +---- Persistence
       |
       +---- Kafka
       |
       +---- WebSocket updates

Replace the generic diagram above with the application's actual architecture after
inspecting the supplied source.
