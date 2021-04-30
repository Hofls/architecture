# Microservices architecture

* `Microservices` - defines application that consist of a set of loosely coupled, collaborating services
* Advantages. Each service is:
	* Loosely coupled with other services (enables independent work, scope of problem is small and simple)
	* Highly maintainable and testable (fast development and deployment)
	* Easily scalabale
* Drawbacks:
	* Development complexity (inter-service communication, testing interactions between services)
	* Deployment complexity 
* Example:
    * News site page with weather broadcast, exchange rates, most popular news articles, feedback form. 
    * Each of those is independent backend service
* Solves all the problems described in monolith.md
* App as a whole is more durable. Even if one service falls down - another one quickly jumps on its place
