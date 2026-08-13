
LoadBalancer vs API GateWay 
	NGINX is good, But People hate it.
	Question is why ???
	
	
AMQP and HTTP Protocols


Black Friday Sale

Thundering Herd
	
=============

🌐 Microservices & Cloud

🔹 Monolith vs Microservices
🔹 Service communication (REST, gRPC, Kafka)
🔹 API Gateway & Service Discovery (Eureka/Consul)
🔹 Circuit Breaker (Resilience4j, Hystrix)
🔹 Saga Pattern for distributed transactions
🔹 Centralized config (Spring Cloud Config)
🔹 Resilience → retry, fallback
🔹 Deployment → Docker & Kubernetes


1. What are microservices?
2. Why are microservices used?
3. Difference between monolithic and microservices architecture.
4. What are the main benefits of microservices?
5. What are the challenges of microservices?
6. What is service-to-service communication?
7. Difference between synchronous and asynchronous communication.
8. What is REST API in microservices?
9. What is an API Gateway?
10. Why is API Gateway required?
11. What is service discovery?
12. Difference between client-side and server-side discovery.
13. What is load balancing in microservices?
14. What is fault tolerance?
15. What is circuit breaker pattern?
16. What is distributed system?
17. What is eventual consistency?
18. What is database per service pattern?
19. Why should microservices not share a database?
20. What is centralized configuration?
21. What is centralized logging?
22. What is monitoring in microservices?
23. What is Docker?
24. What is containerization?
25. What is Kubernetes?
26. Difference between Docker and Kubernetes.
27. How is security handled in microservices?
28. What is JWT?
29. What are common microservices design patterns?
30. When should microservices not be used?	


==============
https://www.linkedin.com/pulse/top-30-microservices-interview-questions-answers-nitin-kumar-qswqc/

https://www.linkedin.com/posts/raghugunasekaran_part-1-java-microservices-interview-question-activity-7340027987355910146-5UIS/

https://www.vinsys.com/blog/microservices-interview-questions


==================
Resilience4j

@CircuitBreaker(name="PaymentService", fallbackMethod="fallback")
public String callPaymentService(){
	return restTemplate.getForObject("http://payment/api",String.class);
}

public String fallback(Exception ex){
	return "Payment Service Unavailable";
}