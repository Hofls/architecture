## Microservices/distributed patterns

#### Data/Database
* `Database per service`
    * Data accessible only via API
    * Each service can pick DB that suits its needs (e.g. PostgreSQL, Elasticseach, MongoDB)
    * If 1 DB dies, other services won't even notice it (Loose coupling)
* `Saga` - sequence of local transactions that span multiple services
    * `Choreography` based - local transaction publishes domain events that trigger next local transaction
        * Example:
            * Clients service receives "order event", produces "not enough money" event
            * Inventory service receives "order event", produces "out of stock" event
    * `Orchestration` based - orchestrator tells the participants what local transactions to execute
        * Example - Orchestrator checks is item in inventory, is a client has enough money, then approves/rejects order
    * High complexity, any local transaction can be undone
* `API Composition` - invokes services and joins their results
    * Example - send request to organization service, user service and event service. Then combine responses into one JSON.
* `CQRS` - write operations go to one DB, read operations to another
    * Examples - main and replica; tables and materialized view;
* `Domain event` - something that happened, and other parts of system should know about
    * Example - order created/cancelled/edited/done
* `Event sourcing` - persist state of entity as a sequence of state-changing events
    * Provides audit log and time travel

#### Decomposition

#### Integration
* `API Gateway` - single entry point for all the clients.
    * Frontend shouldn't know about all the microservices. It should know only about API Gateway.
    * Some requests are simply proxied to the appropriate service, others require multiple calls and calculations.
* `Backends for frontends` - each backend has its own API Gateway
    * One for android app, another for web app, another for 3rd party apps


#### Observability

#### Cross-Cutting concerns

#### Etc
* Run in containers
    * To take advantage of fixed and isolated environment, autoscaling, portability.
* Externalized configuration
    * Get DB credentials and service URLs from the environment. So same executable can run anywhere (local, test, prod)
* Communication:
    * Request/Response (REST, GraphQL, gRPC)
    * Messaging (Kafka, RabbitMQ)
* Service Template
    * Project example with Security, Logging, DB, REST, Tests, etc. Speeds up new service development.

