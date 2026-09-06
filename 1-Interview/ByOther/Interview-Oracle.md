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
