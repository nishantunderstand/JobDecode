Micorservice 
Monilithic vs Microservice
Micorservice Principle 

Protocols / Communication
Communication
Example 
Sync 
Async 

Strangler Fig (Migration)

---

API Gateway
API Gateway vs direct client-to-service communication
Why API Gateway
Centralized Entry Point
API Gateway vs Reverse Proxy
API Gateway vs Load Balancer
API Gateway vs Service Discovery
Single Point of Failure
LoadBalancer + Scaling 
Example :  Spring Cloud Gateway, Kong, NGINX
Can API Gateway and Load Balancer be used together?
Gateway Filters
Rate Limiting
API Versioning

---


---

Service Discorvery 
Why Service Discorvery 
Client Side Service Discorvery
Server Side Service Discorvery 

Kubernetes is a very common example of server-side service discovery.
Server Side → API Gateway + Load Balancer
Service Registry
How does Eureka work? 
Service Discovery vs API Gateway
Service Discovery vs Load Balancer


---
Resilence4j
Bucket4j
Do we any other One ?
What else does it support ?

Circuit Breaker
Rate Limiting
API Limiting
BulkHead
Retry
Time Litter 

---




---

Circuit Breaker 
Closed
Open 
Half Open 

fallbackMethod 
Same or Different Class



Circuit Breaker Vs Retry vs BulkHead
---


SAGA Design Patten