
# eShop

The **eShop** project is a modern, modular solution designed to support scalable and maintainable e-commerce platforms. Built using **Clean Architecture** principles and **Domain-Driven Design** **(DDD)**, eShop leverages the Aspire framework to provide enhanced orchestration, discovery, and distributed systems support across the platform’s microservices.


## Key Concepts

- **Clean Architecture:** The eShop solution separates the concerns of the application into different layers (Domain, Application, Infrastructure, API) to ensure high maintainability and scalability. Each layer has clear responsibilities and communicates with other layers via well-defined contracts, reducing coupling and increasing testability.

- **Domain-Driven Design (DDD):** At its core, eShop follows DDD principles, ensuring that the business logic is tightly coupled to the actual domain. Each microservice encapsulates its own bounded context, making the solution modular and easy to extend. The business logic resides in the Domain layer, where entities, value objects, and aggregates are the main building blocks.

- **Aspire Integration:** Aspire enables eShop’s microservices to communicate in a distributed manner with service discovery and fault-tolerance mechanisms. Aspire’s lightweight framework provides tools for distributed application management, with support for scalability, resilience, and modular development. Aspire also enables features like service discovery, enabling services to dynamically find and connect to each other without hardcoded references.
## Architecture Overview

The project structure adheres to **Clean Architecture**, with each microservice following the same layered structure. This ensures a high level of consistency across the solution and provides benefits like separation of concerns, testability, and flexibility.

### Layers:

- **API:** The API layer serves as the entry point for each microservice, exposing RESTful endpoints to the outside world. The WebFrontend also interacts with the APIs of each microservice.

- **Application:** The Application layer contains the use cases, orchestrating commands and queries. It acts as a mediator between the Domain layer and the outside world, including external services, APIs, and infrastructure.

- **Domain:** This layer contains the heart of the business logic. It holds entities, aggregates, value objects, domain events, and repositories. This is where the business rules are enforced.

- **Infrastructure:** The Infrastructure layer deals with external dependencies such as databases, message brokers (like RabbitMQ), and caches (like Redis). It implements interfaces from the Domain layer to provide actual data persistence.
## Aspire-Enabled Features

- **Service Discovery:** With Aspire, microservices within eShop can dynamically discover each other, ensuring smooth communication across different services in a distributed system.

- **Fault-Tolerant Messaging:** Aspire, combined with RabbitMQ, enables reliable messaging between services, supporting retry mechanisms and fault-tolerant communication patterns.

- **Resilience and Scalability:** The solution is built to scale horizontally with support for distributed workloads. Aspire’s orchestration features allow for easy scaling and service resilience.
## Benefits of the Architecture

- **Modular Design:** Each microservice operates independently, and new services can be added or modified without impacting the rest of the system.

- **Maintainability:** The separation of concerns between layers ensures that each layer has well-defined responsibilities, making the system easier to maintain and extend.

- **Testability:** Clean Architecture naturally promotes unit testing as the dependencies are clearly structured, with business logic decoupled from the infrastructure.

- **Flexibility:** Since the Domain layer is decoupled from the infrastructure, switching technologies (e.g., changing databases) becomes much easier.

- **Resilience:** Aspire’s service discovery and distributed system management ensures the eShop remains resilient under high loads or during failures.
## Conclusion

The **eShop** project is a highly modular, scalable, and maintainable e-commerce platform designed using **Clean Architecture**, **DDD**, and enhanced by **Aspire** for distributed microservices management. It is flexible enough to grow as business requirements evolve and is robust in its design for high traffic and complex transactional systems.
## Authors

- [Juan Pavas](https://www.github.com/juanpavasgarzon)


## License

[MIT](https://choosealicense.com/licenses/mit/). This project is licensed under the MIT license. See the LICENSE file for more details