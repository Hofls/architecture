#### Components
* `Message Queue (MQ)`
    * Advantages: 
        * Guaranteed delivery (if system is down - messages just sit and wait) 
        * Limits load (systems can process messages at their own tempo)
    * Disadvantages:
        * Complexity
* `Database`
    * `Relational`
    * `NoSQL`
* `In-memory data store`
* `Content delivery network (CDN)`
* `Reverse proxy`
    * Functions: caching, filtering, load balancing, authentication, logging
    * Almost the same thing: `Load balancer`, `API Gateway`
* `Web Application Firewall`

#### Comparison
* `Managed > Your own`
    * Your own = high complexity, time-consuming (e.g. install, support, update)
    * Examples: managed grafana/k8s/prometheus/docker/elk...
