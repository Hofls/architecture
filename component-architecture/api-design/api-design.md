### Api design
* Pretend you are API user, what would be simplest and most convenient API?
    * Write pseudocode for client-side to test different ideas
* How easy is it to start using API?
    * Time to first hello world (TTFHW) is a key metric
    * Great starting experience: swagger-ui, GraphQL
* Each endpoint should have small amount of parameters
    * Good examples - get dictionary (no parameters), search by id (1 parameter)
* Expose atomic operations (client can combine them to build complex ones)
* Create use cases and design API with them in mind
* Pick GraphQL or REST
    * GraphQL prevents over-fetching/under-fetching, allows quick front-end development
* The product needs to be easily accessible
    * Quick and easy auth mechanism (or none at all), examples, great documentation
* Reduce cognitive load for your users
    * Consistent naming and code patterns
    * Introduce as few new concepts as possible (mental models)
    * Automate what can be automated
* Provide helpful feedback to your users
    * Catch user errors early and anticipate common mistakes
    * Provide detailed feedback messages upon user error, possibly with hints now to fix error
    * Have a place where users can ask questions
