Architectural Style 
1. Monolithic : Method Call
2. Microservice : 

Communication / Protocols 
1. Sync (REST API) 
2. Async (RabbitMQ, KAFKA)

Sync : REST API ,HTTP / HTTPS, Feign Client, WebClient 

AMQP and HTTP Protocols    
HTTP vs HTTPs
AMQP : Advanced Message Queuing Protocol
Famosuly Used for RabbitMQ

![[Microservice-Communication-Ways.png]]


How this is service communication ? 🤔🤔🤔 
Here communication is between user or system ? 🤔🤔🤔 

```
COMMUNICATION
│
├── A. Client ↔ Service
│      │
│      ├── Browser / Mobile App
│      └── API Gateway / External System
│
│      Usually:
│      └── HTTP / HTTPS
│
└── B. Service ↔ Service
       │
       ├── Synchronous
       │    ├── REST API
       │    ├── Feign Client
       │    └── WebClient
       │
       └── Asynchronous
            ├── Kafka
            └── RabbitMQ
```

```
MICROSERVICE ARCHITECTURE
│
├── Communication
│   │
│   ├── 1. Client → Service
│   │      │
│   │      └── HTTP / HTTPS
│   │
│   └── 2. Service → Service
│          │
│          ├── Synchronous
│          │    │
│          │    ├── REST API
│          │    ├── Feign Client
│          │    └── WebClient
│          │
│          └── Asynchronous
│               │
│               ├── Kafka
│               └── RabbitMQ
│
└── Protocols
    │
    ├── HTTP / HTTPS
    │
    └── AMQP
         └── Advanced Message Queuing Protocol
              └── Commonly used with RabbitMQ
```


```
CLIENT–SERVER COMMUNICATION
│
├── Client
│    ├── Browser
│    ├── Postman
│    ├── Mobile App
│    └── Another Backend Service
│
└── Server
     └── Spring Boot Application
          │
          └── REST API
```