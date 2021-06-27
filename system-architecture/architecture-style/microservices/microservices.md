# Microservices architecture

* `Microservices` - collection of small, autonomous services
* `Advantages`. Each service is:
    * Focused (implements single business capability)
	* Self-contained, independent, Loosely coupled with other services (enables independent work, scope of problem is small and simple)
	* Highly maintainable and testable (fast development and deployment)
	* Scalable - if one service experience high load - automatically deploy more instances
	* Durable (fault isolation) - if one service fails and unable to start - others continue working (without features of fallen service)
	* Communicates with others via API (implementation details hidden)
* `Drawbacks`:
	* Each service is simple, but overall app is complex (inter-service communication, testing interactions between services)
	* Network congestion and latency (all communications done via network)
	* Data integrity (each service is responsible for its own data persistence). Embrace eventual consistency
	* Versioning. Changes in one service shouldn't break others
* `Example`:
    * News site page with weather broadcast, exchange rates, most popular news articles, feedback form. 
    * Each of those is independent backend service
* `Archtecture`
    * ![](microservices.png)
    * ![](microservices-logical.png)
* `Components`
    * `Management/orchestration` - placing services on nodes, identifying failures, rebalancing (e.g. Kubernetes)
    * `API Gateway` - entry point for clients (auth, load balancing, logging, caching etc)
* `Links`
    * [Macroservices](https://www.reddit.com/r/programming/comments/nzemqn/disasters_ive_seen_in_a_microservices_world/)
        * Less complexity, almost same benefits
    