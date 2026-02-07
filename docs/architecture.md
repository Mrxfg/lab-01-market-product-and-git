## Product Choice

**Product:** Telegram  
**Website:** https://telegram.org  
**Description:** Telegram is a cloud-based instant messaging platform focused on speed, security, and scalability.

## Main components

![Telegram Component Diagram](../docs/diagrams/out/telegram/component-diagram/Component%20Diagram.svg)

[Component Diagram Code](../docs/diagrams/src/telegram/component-diagram.puml)

**Selected components:**

1. **Client Applications** – Mobile and desktop apps that allow users to send messages and media.
2. **API Gateway** – Entry point for client requests, routing them to backend services.
3. **Authentication Service** – Handles user login, sessions, and authorization.
4. **Message Service** – Processes, stores, and delivers messages between users.
5. **Media Storage** – Stores images, videos, and other shared files.

## Data flow

![Telegram Sequence Diagram](../docs/diagrams/out/telegram/sequence-diagram/Sequence%20Diagram.svg)

[Sequence Diagram Code](../docs/diagrams/src/telegram/sequence-diagram.puml)

When a user sends a message, the client application sends the request to the API Gateway.
The request is authenticated, processed by the Message Service, stored if needed, and delivered to the recipient.

## Deployment

![Telegram Deployment Diagram](../docs/diagrams/out/telegram/deployment-diagram/Deployment%20Diagram.svg)

[Deployment Diagram Code](../docs/diagrams/src/telegram/deployment-diagram.puml)

Telegram services are deployed across distributed cloud infrastructure with load balancers, application servers, and storage systems.

## Assumptions

- I assume Telegram uses horizontal scaling to handle millions of concurrent users.
- I assume media files are stored in distributed storage with redundancy.
