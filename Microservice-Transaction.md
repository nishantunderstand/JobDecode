

Transaction Management 
On Monolithic  : Rollback 
On Microservice 
  
SAGA Design Patten
SAGA : Sequential Approach to General Availability
  
Types 👈👈👈👈👈
1. Choreography Saga
2. Orchestration Saga : BPMN or Camunda
Central Coordinator
  
ACID guarantees.
This provides eventual consistency rather than a single ACID transaction across all services
ACID Vs BASE 



How to Handle Transaction in Microservices ?
1. SAGA
2. Choreography
3. Orchestration
4. Eventual Consistency
5. Compensating Transaction
6. Avoid 2 Phase Commit






2 Phase Commit 
3 Phase Commit


ACID : Use ACID within a single microservice where all operations are on the same database.
BASE : Use BASE between multiple microservices.