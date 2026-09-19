
Async
  
  
Async + Transaction
@Async + @Transactional
  

@Async + @Transactional
  
What is @Async?
@Async executes a method in a different thread.
  
Scenario 1 : @Transactional → @Async
	Does @Async inherit transactions?
Scenario 2 : @Transactional + @Async on Same Method
Scenario 3 : Transaction Calls Async Method
Scenario 4 : Outer Transaction Rollback
	Why doesn't @Async share transactions?

| Scenario                            | Result                |
| ----------------------------------- | --------------------- |
| @Transactional → Normal Method      | Same TX               |
| @Transactional → @Async             | Different TX          |
| @Async + @Transactional             | Works                 |
| Outer TX Rollback                   | Async TX Not Affected |
| Async Method Without @Transactional | No Transaction        |
  
  
  
Critical Concepts
Critical Code
Critical Code Segment
Shared Resource

Async / FutureAPI or CompletableFuture / Virtual Thread
How are they related to each other ?
