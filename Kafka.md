
1. [[Kafka-Architecuture.excalidraw]]
2. [[Kafka-Failure-1.excalidraw]]

---

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



Why Kafka ? Why not use ActiveMQ or Rabbit MQ ? 
[Apache Kafka Will Finally Makes Sense After This Video](https://www.youtube.com/watch?v=yjqwhr23vCs)

When to use Kafka ?
Why Kafka?
Why do we need Kafka?

Advantages of Kafka
Disadvantage of kafka


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


Message Queue  : 1 Publisher : 1 Subscriber
Pub-Sub  : 1 Publisher : N Subscriber
Kafka : 1 Publisher : N Subscriber + Distributed + Persistent Log 
KAFKA Vs RabbitMQ vs ActiveMQ vs AWS SNS or Similar










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
Cannot we achieve Event Driven Architecture by Active or RabbitMQ ?


How EDA is different from Kafka 🤔🤔🤔 






---

Kafka Architecture

Kafka Cluster
Kafka Broker

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


----


# Kafka Cluster Configuration

1. broker.id  : ZooKeeper-based Kafka    
2. node.id : KRaft-based Kafka

---

# Topic 

How to Decide a Topic ?
Based on Business service + Logical event, We can decide 
Order Service
 ├── OrderCreated
 ├── OrderCancelled
 └── OrderUpdated

Payment Service
 ├── PaymentSuccess
 └── PaymentFailed

Inventory Service
 ├── InventoryReserved
 └── InventoryFailed
 
Based on We have 3 Business Event, 3 Topic 

---

# Partition

Partitions — num.partitions

Partitions determine:
- Parallelism
- Throughput
- Maximum number of consumers processing simultaneously
- Ordering scope

How do we decide partitions?
Incoming traffic = 10,000 messages/sec
One consumer instance can process = 2,000 messages/sec
Partitions >= 10000 / 2000
Partitions >= 5
But we also need growth.
Current requirement = 5 partitions
Expected growth = 2x
You might choose:
10–12 partitions

Important rule
Maximum active consumers ≈ Number of partitions
Partition

PartitionSkew : UnEven Distribution
P0 → 90,000 msg/sec : This is becoming a bottleneck
P1 →  2,000 msg/sec
P2 →  2,000 msg/sec
P3 →  2,000 msg/sec
P4 →  4,000 msg/sec

Hot Partition : One partition receives disproportionately high traffic.
P0 : More Traffic Here
P1 : Less Traffic
P2 : Less Traffic

Sticky Partitioning🤔🤔🤔 

---
---


---

Topic 
logical category/group of messages.




Partition 
A **partition is an ordered log of records** inside a topic.
Physical/logical subdivision of that topic
Ordered append-only log of records

OffSet
Position of the record inside its partition
Offset belongs to a Partition

OffSet : An offset identifies a record's position within a partition.
Topic vs Partition vs Offset




Topic + Partitions + Offset

Can a Broker have multiple Topics?	
Can a Topic have multiple Partitions?	
Can a Partition have multiple Offsets? 🤔🤔🤔 


==One Partition can be assigned to only one Consumer within the same Consumer Group.==
Can two consumers read from the same Topic? (Same or Different Consumer Group)
Can Brokers Be in Different Locations?
Can a Topic Have Multiple Partitions?



---


What is the difference between Kafka key and partition?
Key -> Where Message Goes
Partition : Where Message Stored

---
Message Ordering
Does Kafka guarantee message ordering?
Topic 
Multiple Topic 
Partiton 
Multiple Partition
Offset
Local Ordering 
Global Ordering 


Kafka Ordering + Key + Partition 

Ordering 
Kafka Ordering is Topic wide
Ordering within a partition. 


---

Leader Election
Preferred Replica
Replication Lag
Broker 1 Dies, New Leader Broker 2
What if Broker 1 is back ?
What if Replica falls too far behind ?
Preferred Replica vs ISR 🤔🤔🤔 
Leader Election vs Consumer Rebalance 🤔🤔🤔 



---

Kafka Message Structure 
kafka Message aka Record

![[Kafka-Message-Structure.png]]






---

# Producer

Producer acks + Idempotence + Retries
Producer delivery.timeout.ms
Producer Buffer Memory

request.timeout.ms vs delivery.timeout.ms 
request.timeout.ms : One Request
delivery.timeout.ms  : Whole Delivery Attempt Including retries







---

# Consumer and ConsumerGroup

Topic = 3 partitions
Consumer Group A
Consumer 1
Consumer 2
Consumer 3
Consumer 4

If we have 3 Partition, Then we need 3 Consumer 
Consumers ≤ Partitions

Number of useful consumers ≤ Number of partitions
Consumer 4 will be idle.
P0 → Consumer 1
P1 → Consumer 2
P2 → Consumer 3
Consumer 4 → Idle

So partition count directly affects consumer scalability.

How to decide on a Consumer Group ?
Who needs to independently read to this event.

For Example 
This event Need to be read by Payment, Inventory , Rating 
Then I need 3 groups.
Consumer Group 
5 Consumer  12 partition

How to decide the partition ??
C1
C2
C3
C4
C5 : 
12 / 5
Quotient = 2
Remainder = 2

Then Try to Rebalance itself 
How much parallelism does each group need?
Different Consumer Groups can have different numbers of consumers
Can these Consumer groups have Different Number Partitions ?

Example:

| Consumer Group | Incoming Rate | Capacity per Consumer | Needed Consumers |
| -------------- | ------------- | --------------------- | ---------------- |
| Payment        | 10,000/sec    | 2,000/sec             | 5                |
| Inventory      | 10,000/sec    | 5,000/sec             | 2                |
| Shipping       | 10,000/sec    | 1,000/sec             | 10               |
| Analytics      | 10,000/sec    | 10,000/sec            | 1                |


---


Kafka Consumer Lag
Case 1 — Consumer is slow
Case 2 — Consumer processing is expensive
Case 3 — Consumer is down

How Do We Reduce Consumer Lag?
Option 1 — Add consumers
Option 2 — Increase processing speed
Option 3 — Increase partition count

Consumer Lag vs Offset Commit 🤔🤔🤔 


Consumer Polling Model 



Consumer Group Coordinator

Consumer Rebalancing

When does Rebalancing happen ?
1. Consumer joins
2. Consumer leaves/crashes
3. Partition count changes
4. Consumer is considered dead


`poll()` and `max.poll.interval.ms`

max.poll.interval.ms is about maximum time between poll calls.
session.timeout.ms is about consumer liveness through heartbeats.

Modern Kafka Sends heartbeats 


Eager vs Cooperative Rebalancing

Consumer-group partition assignment strategies
1. RangeAssignor
2. RoundRobinAssignor
3. StickyAssignor
4. CooperativeStickyAssignor






---

  
# Replication Factor 

RF ≥ F+1 to tolerate F broker failures,

This is independent 
replication.factor=3

Example:
Topic: orders
Replication Factor = 3
Partition 0:
Broker 1 → Leader
Broker 2 → Replica | Follower
Broker 3 → Replica

How data will be synced across leaders and Followers  

Explain me the meaning of 3 i.e 1 Leader  + 2 Follower 
If Broker 1 crashes:
Broker 2 → New Leader

Common choice :

| Environment | Replication Factor |
| ----------- | ------------------ |
| Development | 1                  |
| Staging     | 2 or 3             |
| Production  | 3                  |

For a production system, RF = 3 is a very common starting point.

Is there any mathematical formula for determining it ? 🤔🤔🤔 

---

# Min.insync.replicas

min.insync.replicas 
minISR = RF-1
RF ≥ F+1 to tolerate F broker failures,
What does this F represent ?
"How many brokers can crash, and I still want my data/service to survive?"

Broker 1 → Leader
Broker 2 → Replica
Broker 3 → Replica

Broker 1 💥
Broker 2 💥
Broker 3 ✅

You lost 2 brokers, but one copy still exists.
Therefore:
F = 2
RF = 3
This is extremely important.

Suppose:
Replication Factor = 3
Broker 1 → Leader
Broker 2 → Follower
Broker 3 → Follower

Set:
min.insync.replicas=2
It means Kafka requires at least 2 in-sync replicas for a successful durable write when the producer uses:
acks=all

Recommended combination
replication.factor=3
min.insync.replicas=2
acks=all
This gives good durability.


```
Scenario
Initially:
ISR = [Broker1, Broker2, Broker3]
One broker dies:
ISR = [Broker1, Broker2]
Still okay because:
ISR >= min.insync.replicas
2 >= 2
Another broker becomes unavailable:
ISR = [Broker1]
Now:
1 < 2
Kafka rejects writes rather than accepting data with insufficient replication.

```

That is a tradeoff:
Availability ↓
Durability ↑

What if we have only 1 ISR ?  
Think about a different edge case ?
How will they behave around it ?

|     |                    |            |        |      |        |        | ISR >= minISR |
| :-: | :----------------: | :--------: | :----: | :--: | :----: | :----: | :-----------: |
| RF  | Failed Replicas(F) | ISR = RF-F | minISR | Read | acks=0 | acks=1 |   acks=all    |
|  3  |         0          |     3      |   2    |  ✅   |   ✅*   |   ✅    |       ✅       |
|  3  |         1          |     2      |   2    |  ✅   |   ✅*   |   ✅    |       ✅       |
|  3  |         2          |     1      |   2    |  ✅   |   ✅*   |   ✅    |       ❌       |
|  3  |         3          |     0      |   2    |  ❌   |   ❌    |   ❌    |       ❌       |
| RF  | Failed Replicas(F) | ISR = RF-F | minISR | Read | acks=0 | acks=1 |   acks=all    |
|  2  |         0          |     2      |   1    |  ✅   |   ✅*   |   ✅    |       ✅       |
|  2  |         1          |     1      |   1    |  ✅   |   ✅*   |   ✅    |       ✅       |
|  2  |         2          |     0      |   1    |  ❌   |   ❌    |   ❌    |       ❌       |
| RF  | Failed Replicas(F) | ISR = RF-F | minISR | Read | acks=0 | acks=1 |   acks=all    |
|  1  |         0          |     1      |   0    |  ✅   |   ✅*   |   ✅    |       ✅       |
|  1  |         1          |     0      |   0    |  ❌   |   ❌    |   ❌    |       ❌       |
| RF  | Failed Replicas(F) | ISR = RF-F | minISR | Read | acks=0 | acks=1 |   acks=all    |
|  0  |         —          |     0      |   —    |  ❌   |   ❌    |   ❌    |       ❌       |

  
RF = 3
minISR = RF-1
RF >= F+1
ISR = RF-F
==acks=all ACCEPT if ISR >= minISR==
acks=all REJECT if ISR < minISR


---
Producer  Acknowledment 
1. acks 0 : Don't wait for acknowledgment
2. acks 1 : Leader acknowledges
3. acks all : wait for all replicas currently in ISR.

How data will get synced b/w leader and follower ?
Leader + Followers / Replication
What about Replication Lag 🤔🤔🤔 
  
| acks | Producer waits for            |
| ---- | ----------------------------- |
| 0    | Nobody                        |
| 1    | Leader                        |
| all  | All replicas currently in ISR |

---

# Idempotency

Idempotency Kafka Key Use Case
Producer enable.idempotence 
retries
Network failures happen.
Can we producer Idempotent ?  enable.idempotence=true
Can we consumer Idempotent 
Can we consumerGroup Idempotent  : Doesn't Exists

---

Kafka Key  🤔🤔🤔 
Kafka uses the key primarily for partition selection:
Kafka Key + Idempotency

---
Kafka Batch 
Kafka can batch messages.

1. Based on time : linger.ms
2. Based on Size : batch.size

linger.ms 
Batch.size

Maximum approximate batch size before sending.

Example:
batch.size=32768
Conceptually:
Producer Buffer

```
[M1][M2][M3][M4][M5]
──────────────────────
        32 KB

```

When the batch fills, it can be sent without waiting for linger.ms.

High throughput → larger batches
Low latency → smaller batching / lower linger

batch.size  → "How MUCH data should I collect?"
linger.ms   → "How LONG should I wait?"

WHICHEVER HAPPENS FIRST → SEND  

Whoever wins Between batch.size and linger.ms  : Based on that it send.

# Compression

compression.type=zstd

Other options:
1. none
2. gzip
3. snappy
4. lz4
5. zstd

Tradeoff:
Compression
Less network
Less disk usage
More CPU

A common modern choice is often:
lz4 → fast
zstd → better compression, with CPU tradeoffs

---
Messaging Protocols
TCP
HTTP
AMQP

What is difference Between Communication and Message Protcols ? 🤔🤔🤔 

---

Kafka Streams
1. KStream
2. KTable

----

Offset Commit 
1. Auto Commit
2. Manual Commit 


Delivery Semantics  Guarantees
1. At-most-once : No duplicates, but possible loss
2. At-least-once : No loss, but duplicates possible 🤔🤔🤔 
3. Exactly-once


Offset Commit and Delivery Semantics

---

cleanup.policy : whether the topic uses deletion, compaction, or both.

cleanup.policy=delete

Log Compaction  : How Old it is ?
Kafka can delete messages based on **time** or **size**.

Compaction
Suppose a user has Active, Suspended, Waiting , Premium
It will only store the latest One, i.e. Premium.

Retention vs Compaction 
Retention = delete messages based on age/size.
Compaction = keep the latest value for each key.

Retention Policy
Types 
1. Time-Based Retention
2. Size-Based Retention

---


# Reliability & Data Management

Kafka : Bytes
Serialization / Deserialization 🤔🤔🤔 
Where this conversion is happening ?
DownStream System 

Error Handling
Dead Letter Topic 
Retry Topic 
Retry Mechanism
DLT Dead Letter Topic 
DLQ Dead Letter Queue
Poison Pill Problem
Retry : "Try again; this might work later."


DLT vs DLQ 🤔🤔🤔 


Retry Topic  vs  DLT Dead Letter Topic