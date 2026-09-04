


Due to Evolution of Technology 
Hystrix  → Resilience4j
Ribbon   → Spring Cloud LoadBalancer
Zuul     → Spring Cloud Gateway
  
Hystrix 
Fault Tolerance Library
Cascading Failure
Why Deprecated 
  
Fault-Tolerance / Resilience Mechanisms
  
Circuit Breaker
Retry
Timeout / Time Limiter
Bulkhead / Isolation
Rate Limiter
Fallback
  
Successor of Hystrix
  
Resilence4j
https://resilience4j.readme.io/docs/getting-started
  
Bucket4j (Specially Design For Rate Limiter )
  
Circuit Breaker States
Closed
Open 
Half Open 
  
Fallback Method Invoked From Same or Different Class + AOP Concept + Self Invocation Problem
  
Circuit Breaker Vs Retry vs Bulkhead
  
Circuit Breaker Interview Trap Question
  
Retry vs Circuit Breaker
Can Retry Make the System Worse?
  
Retry = "Try again."
Circuit Breaker = "Stop trying."
  
Is Circuit Breaker Same as Timeout?
  
Why Use Bulkhead?
Bulkhead vs Circuit Breaker
Rate Limiter vs Load Balancer
Where to Apply Rate Limiter?
  
Is Fallback mandatory ?
Fallback Method Signature relation with original Method 
  
Does Circuit Breaker Fix Down Service?
If Circuit Opens, What User Gets?
Can We Use All Together?
  
Which Pattern for Temporary Network Glitch?
Which Pattern for Slow External API?
Which Pattern for Too Many Requests?
Which Pattern for Thread Exhaustion?
Is Fallback Mandatory?
  
Spring Boot Tool Name? resilience4j-spring-boot3
  
Rate Limiter Vs Bloom Filter ?
  
Can Circuit Breaker Recover Automatically ? 
If fallback returns successfully, will the Circuit Breaker become CLOSED?
Can fallback itself throw an exception?
Can fallback have a different return type?
What if the original method has parameters?
Can I have multiple fallback methods?
Does fallback mean retry?
  
Does Circuit Breaker Fix the Downstream Service?
  
[https://medium.com/%40shivanimutke2501/day-43-system-design-concept-circuit-breaker-6063b3b754a6](https://medium.com/%40shivanimutke2501/day-43-system-design-concept-circuit-breaker-6063b3b754a6)
