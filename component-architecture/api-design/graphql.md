### Approaches
* `DB first`
    * Use hasura to create tables in postgres, generate graphql endpoints + schema
    * Generate types and request code with [generator](https://graphql-code-generator.com/)
* `Code first`
* `Schema first`

#### Main concepts:
* GraphQL - A Query Language for APIs
* The syntax for writing schemas called Schema Definition Language (SDL).
* Schema stitching allows to combine and connect multiple GraphQL APIs and merge them into a single one. 

#### GraphQL vs Rest
* No more Over - and Underfetching (frontend chooses which fields backend should return)
* Rapid Product Iterations on the Frontend (no need to change backend each time frontend changes)
* Insightful Analytics on the Backend
As each client specifies exactly what information it’s interested in, it is possible to gain a deep understanding of how the available data is being used
* Benefits of a Schema & Type System
Frontend teams can easily test their applications by mocking the required data structures. Once the server is ready, the switch can be flipped for the client apps to load the data from the actual API.
* developers don’t have to manually write API documentation any more — instead it can be auto-generated based on the schema that defines the API. 
