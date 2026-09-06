Interview CJD WhatsApp Group Question 

interview with Oracle for a Java Backend Developer role.
It covered DSA, Java, Spring Boot, Kafka, and System Design. Sharing a few questions that asked to me:

1. DSA – Number of Islands
Started with a variation of Number of Islands.
Follow-ups:

* What if diagonal cells are also connected?
* BFS vs DFS – which would you choose and why?

2. Java Streams
Given a list of employees, group them by department and find the top 3 highest-paid employees from each department.
Follow-up: Would parallelStream() actually improve performance here?

3. Java & Spring Boot

* How does @Transactional work internally?
* Two threads update the same resource simultaneously — how would you prevent race conditions?
* How would you reduce latency when an API makes multiple independent downstream calls?

4. Kafka
A consumer processes a message but crashes before committing the offset.

* What happens next?
* How would you prevent duplicate processing?

5. System Design
We discussed designing a scalable backend service using Kafka, Redis, caching, retries, and horizontal scaling.

An interesting follow-up:
“What would start breaking if traffic suddenly increased 100x?”

This led to discussions around DB bottlenecks, connection pools, Kafka lag, caching, and scaling.

Hope this helps anyone preparing for Java Backend interviews.

#Oracle #Java #SpringBoot #BackendEngineer
#Kafka #Microservices #SystemDesign
#InterviewExperience



---



Java Backend Developer
Client -Flipkart (Third party payroll)
1. Tell me about your project and your contribution in it
2. Why did you migrate to microservices
3. Follow-up if testing is difficult in microservices why you choose it
4. How microservices communicate with each other
 5. why you choose kafka for async operations .
 6. Doesn’t your synchronous service handles               
7. notification service? if ti can handle what’s the need of kafka
8. What rest method did you use
9 Why we use patch and put
10. While using, post method, where it is created.
11. How did you handle global exception
12. What is a topic in kafka
13 Kafka partitioning
14. What is the cluster metadata in kafka
15 How does Kafka supports scalability
16. What happens when a kafka broker goes down
17. There are some microservices A, B and C. Service C becomes unavailable. What will happen?
18. How does  Kafka ensure data consistency?
19. How does kafka handles data retention
20. Public void test(){
 Int x=10;
Employee e=new Employee ();
}
 What will happen inside JVM? Stack, heap? Will they stay inside the stack/ heap or where will they go after execution? 
What will happen to the object inside the heap after execution?
21. {1, 0, 1, 0, 0, 1, 0, 1 } push all zero to end22.  Find middle node - LinkedList problem