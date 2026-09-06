Interview TechMahindra


1] Suppose you have added @Transactional, but still data is partially saved when an exception happens. How will you debug and fix it?
2] when your Spring Boot application is working fine in normal traffic, but during high traffic the response time becomes very slow. How will you find the root cause?
3] In your project, one microservice is calling another microservice using REST, but sometimes the second service is slow or down. How will you handle timeout, retry, and fallback?
4] If your JWT token is valid, but the user role has changed in the database. How will you make sure old permissions are not misused?
5] Suppose cached data is showing old values even after the database is updated. How will you fix this issue?
6] In your project, database queries are increasing suddenly because of the N+1 query problem. How will you detect and solve it?
7] If one API is throwing LazyInitializationException in production. How will you identify and fix it?
8] In your project, messages are processed from Kafka or RabbitMQ, but the same message is processed twice. How will you handle duplicate processing?
9] Let say if one microservice publishes an event, but the consumer service is down at that time. How will you make sure the event is not lost?
10] Suppose your application secret keys and database passwords should not be kept in application.properties. How will you manage them securely?
11] In your microservices project, authentication is handled by one service, but other services also need to know whether the user is valid or not. How will you design security?
12] Suppose your application is calling three external APIs, and one of them has rate limits. How will you avoid crossing the limit and still keep your application stable?
13] In your project, one API is fetching the same master data again and again from the database. How will you use caching to improve performance?
14] In your project, one API returns thousands of records and the frontend becomes slow. How will you implement pagination and sorting?
15] In your project, you need to send a welcome email after user registration, but email sending should not slow down the registration API. How will you design this?