[Spring Boot + Kafka Course | Learn Apache Kafka in One Shot!](https://www.youtube.com/watch?v=gpx7smdUkgU&t=667s)  : Only Theory 

MessageOriented Middleware (MOM)
It is software that allows applications to communicate through messages instead of direct calls.

Message Broker
Loosely Coupling

Producer → Message Broker → Consumer
ActiveMQ 
RabbitMQ
Kafka
Redis Pub-Sub

---

Parameter of Judgement : 
Message Storage 
Consumer OFF / ON 
Message Replay 
Consumer Groups 
Scalability 
Pull vs Push Model 
Ordering 
Kafka does NOT guarantee global ordering across all partitions.
Ordering is guaranteed only inside each partition.



Message Queue  : 1 Publisher : 1 Subscriber
Pub-Sub  : 1 Publisher : N Subscriber
Kafka : 1 Publisher : N Subscriber + Distributed + Persistent Log 
KAFKA Vs RabbitMQ vs ActiveMQ vs AWS SNS or Similar


Why Kafka ? Why not use ActiveMQ or Rabbit MQ ? 
[Apache Kafka Will Finally Makes Sense After This Video](https://www.youtube.com/watch?v=yjqwhr23vCs)

When to use Kafka ?
Why Kafka?
Why do we need Kafka?

Advantages of Kafka
Disadvantage of kafka

Architecture
Monolithic Architecture
Microservice Architecture

Communication
Sync (REST API)
Async (Kafka)

EventDriven Architecture
What is EventDriven Architecture?
Event
Event Producer
Event Consumer
Cannot we achieve Event Driven Architecture by Active or RabbitMQ ? 🤔🤔🤔 

---


Depend Upon Nature of Business  : 

When to Pick Rabbit MQ 
If system has:
- moderate traffic
- straightforward work queues
- task distribution
- relatively short-lived messages
- no significant replay requirement
I'd seriously consider RabbitMQ.

RabbitMQ / ActiveMQ
task processing
work queues
request distribution
routing
low-latency messaging

Kafka
event streaming
high throughput
distributed systems
event-driven microservices
analytics
log/data pipelines
replaying events
multiple independent consumers

[https://www.instagram.com/reels/Db5v8fxPvUS/](https://www.instagram.com/reels/Db5v8fxPvUS/)

---

Kafka Architecture

Kafka Cluster
Broker

Producer
Producer Group : Doesn't Exisits
Consumer
Consumer Group
Topic
Partition
Offset
Key in Kafka
Serialization

Leader
Follower
MasterSlave Architecture

Replication Factor
Zookeeper / KRaft

Can we have multiple Kafka Clusters?
Can we have multiple Kafka Brokers?
Can one Kafka Cluster have multiple Kafka Brokers?
Can one Kafka Broker belong to multiple Kafka Clusters? 🤔🤔🤔  
One Kafka cluster → can have multiple brokers.
One broker → can host partitions belonging to multiple topics.
One topic → can have multiple partitions.
One partition → belongs to exactly one topic.

---


Topic 
Logical category/stream

Partition 
Physical/logical subdivision of that topic
Ordered append-only log of records

OffSet
Position of the record inside its partition
Topic + Partitions + Offset

Can a Broker have multiple Topics?	
Can a Topic have multiple Partitions?	
Can a Partition have multiple Offsets?


One Partition can be assigned to only one Consumer within the same Consumer Group.
Can two consumers read from the same Topic? (Same or Different Consumer Group)
Can Brokers Be in Different Locations?
Can a Topic Have Multiple Partitions?
Consumer Rebalancing
Message Ordering
Does Kafka guarantee message ordering?



---

Delivery Guarantees
At Most Once
At Least Once
Exactly Once


---
Messaging Protocols
TCP
HTTP
AMQP

What is difference Between Communication and Message Protcols ? 🤔🤔🤔 

---
  ---
Error Handling
Retry Mechanism
DLT Dead Letter Topic 
DLQ Dead Letter Queue
Poison Pill Problem

---
Kafka Streams
KStream
KTable

---

How would you determine how much partition and Replica lag ?
How do you decide ?
What is the parameter of judgment ?
How do you decide on Configuration ?

---




---

🤔🤔🤔 

Reliability & Data Management
Retention Policy
Log Compaction

Idempotence Kafka 
Idempotent Producer
Idempotent Consumer
Idempotent Consumer Group 

---
