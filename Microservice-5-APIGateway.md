
API Gateway
  
It handles routing, authentication, logging, monitoring, rate limiting, API versioning, and load balancing

Why API Gateway

API Gateway vs Direct client-to-service communication
Centralized Entry Point
Example :  Spring Cloud Gateway, Kong, NGINX


Cross-Cutting Concern : 
1. Routing
2. Authentication
3. Authorization
4. Rate Limiting
5. Load Balancing
6. SSL/TLS termination
7. CORS
8. Request transformation
9. Response transformation
10. Logging
11. Metrics
12. Tracing
13. Circuit breaking
14. API versioning
15. Caching


Single Point of Failure
Can API Gateway and Load Balancer be used together?
API Gateway vs Load Balancer
LoadBalancer + Scaling 

  

Why not put authentication inside every microservice?
Gateway authentication does not mean downstream services should blindly trust every request.
For sensitive operations, services can independently validate identity/authorization.


401 vs 403 Trap

Should Authentication at APIGateway or before Service ?
Same about Authorization 

Routing
```
/api/users/** 
/api/orders/** 
/api/payments/**


/api/users/**     → User Service
/api/orders/**    → Order Service
/api/payments/**  → Payment Service

```

Why Rate Limit at Gateway?

API Gateway ≠ Load Balancer
API Gateway vs Reverse Proxy
API Gateway vs Service Mesh
API Gateway vs Reverse Proxy
API Gateway vs Service Discovery

North-South = traffic entering/leaving your system.
East-West = traffic between services inside your system.
