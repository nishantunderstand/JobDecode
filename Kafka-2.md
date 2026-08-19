
MOM (Message Oriented Middleware)

Pub-Sub

KAFKA Vs RabbitMQ vs ActiveMQ vs AWS SNS or Similar

Producer
Producer Group

Consumer
Consumer Group

Kafka Broker
Kafka Cluster

Can we have multiple Kafka Brokers?
Can we have multiple Kafka Clusters?
Can one Kafka Cluster have multiple Kafka Brokers?
Can one Kafka Broker belong to multiple Kafka Clusters?


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


KRaft
Zookepper


DLQ
DLT
Poision Pill Problem



Idempotent Kafka


---
