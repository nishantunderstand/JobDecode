Interview LinkedIn 2026


🚀 Most Frequently Asked Scenario-Based Questions for Senior Java Developer Roles

1. Suppose you have 3 microservices: A, B, and C. A posts a message to a Kafka topic of B. How does Microservice B consume the message and post it to the REST API endpoint of Microservice C?
2. How do we post a message to a REST API endpoint, and what is the difference between HttpClient and RestTemplate?
3. What is the difference between CrudRepository and JpaRepository?
4. What is the difference between SessionFactory and EntityManager?
5. In Spring JPA, what does it internally use: SessionFactory or EntityManager?
6. In Hibernate, what do we use: SessionFactory or EntityManager?
7. Suppose you consume a Kafka message in XML, convert it, and publish it to a downstream Kafka topic, but while doing this, the data is persisted in the database and the message is not published to the Kafka topic due to some error. How do you roll back the database data? How do you handle this scenario in a microservice?
8. How does Spring communicate with the database? How does Spring Data JPA do the same?
9. How do you control the number of users who can access your microservice? Suppose there are billions of users, but you want only 10K users to be able to access the service.
10. How do you store user details and passwords in AWS?
11. How does pagination work in Spring Boot? How does Spring Boot and the database know that only 10 records should be fetched and displayed at a time? Explain the internal working and flow from the Controller to the Service and Repository levels.
12. Suppose you have to design a flow where a message has to be put at a place from where 5 different microservices can read those messages asynchronously. Now, what approaches can we take here, and why?
13. How does Spring Boot decide which auto-configuration to apply?
14. What happens internally when you add the spring-boot-starter-web dependency?
15. Why does Spring Boot prefer convention over configuration?
16. What is the exact startup flow of a Spring Boot application?
17. What will happen if you define @Controller, @Service, and @Repository over the same class?
18. How does Spring Boot detect the embedded Tomcat and configure it?
19. How do we configure a health check in a Spring Boot application?
20. How do we make sure no external person can check or hit the health-check URL of your service? How do we secure it?
21. How does Spring Boot reduce XML configuration completely?
22. What is the role of SpringFactoriesLoader?
23. How does Spring Boot handle profile-specific configuration?
24. How does Spring Boot manage dependency versions internally?
25. How does Spring Boot handle externalized configuration?

If anyone is preparing for Java Backend Developer interviews, these questions might be helpful.




I recently attended an interview for a Java Backend Developer role at TCS and Capgemini. 
I wanted to share my experience along with the questions that were asked.

1. Diff between synchronized keyword and Reentrant Lock. What is a trade-off?
2. HirakiCP, what is it?
3. What is a volatile keyword?
4. What is the difference between the volatile keyword and the Atomic class (AtomicInteger & AtomicFloat)
5. What is the Maven life-cycle (in a detailed -Maven package, maven - install, maven - deploy)
6. How did you implement Spring Security in distributed microservices?
7. How to maintain transactions in a distributed database?
8. In pom.xml, we used the tag <DistributionManagement>. What is it? why we use it?
9. Is it possible to write private methods in an interface?
10. How many types of methods can we write in an interface?
11. what is @EnableAutoConfiguration and @Qualifier?
12. What are bean lifecycles? 
13. Java 17 features.
14. What is the Record class, and how do we store data in the Record class if a list of data is coming through a query? How to fetch the first records?
15. What is the var keyword? Can we use it as a generic type?
16. SOLID design principles.
17. What is CQRS?
18. How can we make Kafka Producer Idempotent?
19. Load Balancer Policies scenario - if 3 instances are running, how to check which is available to post messages?
20. Write a query to fetch all employees who have a salary more than the average of all employees' salaries.
21. Find the first unique character, and its index. ex- String input = ‘hackathon’;

If anyone is preparing for Java Backend Developer interviews, these questions might be helpful.



I recently attended an interview for a Senior Java Developer role at Citi Bank.
I wanted to share my experience along with the questions that were asked.
 
1. What is Kafka?
2. What are zookeeper, broker and topic?
3. How to manage the order of messages if a message is posted in two topics and one consumer is reading from both topics?
4. What is the difference between a stream and a parallel stream? Have you used a parallel stream in a real project?
5. What are the new features in Java 17?
6. What is Kafka stream? how you know whether a message is consumed or not by the consumer?
 a -> What happened when the error occurred between phase message get persisted in the table, but after that any error occurred?
 b -> How to manage this so no duplicate message needs to be reprocessed. 
7. What is event sourcing?
8. What happens if we write two identical default methods in two different interfaces and try to implement them in a class? What will happen? How to fix the issue if there any think came?
9. What are the SOLID principles?
10. What are Liskov's substitutional principles? If we can replace the parent class object with a subclass, then why do we need inheritance?
11. What are TDD and BDD?
12. What is canary deployment? What is blue & green deployment?
13. What is orchestration and choreography?
14. Kubernetes vs. OpenShift?
15. Can we keep HashMap keys mutable? Why and why not?
16. What is a checked Exception? advantage & disadvantage.
17. What is an effective final in Java?
18. What is the CQRS design pattern?

If anyone is preparing for Java Backend Developer interviews, these questions might be helpful.



I recently attended an interview for a Java Backend Developer role at Infosys and Barclays. I wanted to share my experience along with the questions that were asked.

Explain the SOLID Design pattern.
What is JWT security, and how have you used it in your project?
Stream vs flat Map.
Explain basic Spring Security.
Reverse a string without using predefined methods.
Spring Container internal working.
What is an Optional class?
What is the difference between @primary and @Qualifier?
Explain Completable Future methods.
Explain Bean Lifecycle.
Explain Maven Lifecycle.
What is the difference between Path Variable and Request Params?
What is JWT security, and how have you used it in your project
What is fetch type (Lazy and Eager Loading)?
Explain and implement the factory design pattern (with some modification)
What do you know about ISO8583?
Diff b/w IOC and Dependency Injection.
What is Dependency Injection and its types?
Find the second-highest salary from the employee table.
Find a file in a subdirectory
How have you used Spring Security in your project?
What is a spring profile, and how did you use it?
What is exception handling, and what is a Controller Advisor?
How does the @Transactional annotation work?

If anyone is preparing for Java Backend Developer interviews, these questions might be helpful.
