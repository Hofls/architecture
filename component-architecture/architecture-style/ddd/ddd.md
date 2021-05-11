* DDD
    * Structure and language of software should match business domain
    * Iterative, ongoing process (e.g. if service grows too much - break it apart)
* Concepts
    * Context - setting in which a statement appears that determines its meaning
    * Domain - subject area of a project
    * Model - describes parts of a domain. If model becomes too complex - fragment into multiple models.
    * Ubiquitous Language - shared by all team members
    * Bounded context - boundary within a domain where a particular domain model applies
    * Context map
* Steps
    * Analyze domain
        * Organize business knowledge, create business model, provide common language
    * Define bounded contexts
    * Define entities, aggregates, services (within each subdomain)
    * Identify microservices
* Phases
    * Strategic - define large-scale structure of the system
    * Tactical - design patterns that help to create domain model
* Building blocks
    * Entity - object with ID, persists over time (e.g. customer, account)
    * Value object - no ID, only attributes, immutable
    * Aggregate - group of objects
    * Domain Event - notify parts of system when something happens (e.g. delivery cancelled)
    * Service - implements logic, doesn't have state
    * Repository
    * Factory
* Examples
    * https://docs.microsoft.com/en-us/azure/architecture/microservices/model/domain-analysis
    * 
    * 