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


---
Differene B/W Them :: 
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
Circit Breaker Interview Trap Question
Retry vs Circuit Breaker
Can Retry Make System Worse?
Is Circuit Breaker Same as Timeout?
Why Use Bulkhead?
Bulkhead vs Circuit Breaker
Rate Limiter vs Load Balancer
Where to Apply Rate Limiter?
Does Circuit Breaker Fix Down Service?
If Circuit Opens, What User Gets?
Can We Use All Together?
Which Pattern for Temporary Network Glitch?
Which Pattern for Slow External API?
Which Pattern for Too Many Requests?
Which Pattern for Thread Exhaustion?
Is Fallback Mandatory?
Spring Boot Tool Name?
Rate Limiter Vs Bloom Filter ?


Can circuit Breaker Recover Automatically ? Yes via HALF_OPEN state

---


SAGA Design Patten
SAGA 
Fallback On Monlithic vs Micorservice Payment

Types
1. Choreography Saga
2. Orchestration Saga

You need to learn an example.

How to Handle Transaction in Microservices ?


---

Deployment
Blue Green Deployment
Canary Deployment


---

Event Sourcing
Event Sourcing vs Event-Driven Architecture
Event Sourcing vs CQRS


---
EDA

---


Schema per Service Design Pattern  
Schema level Isolation

Database per Service Design Pattern

