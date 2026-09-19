[[JDBC]]

Connection
ConnectionPooling 
JDBC Connection Pooling
Are they the same or different thing ?

Why Connection Pooling ?
Internal Working of ThreadPool ?  🤔🤔🤔 
How to create ThreadPool ?  
You just need to configure it. Are you good to go ??


HikariCP 
Why is HikariCP so fast ?
HikariCP is a high-performance, lightweight Java JDBC connection pooling library
HikariCP is — Fast, simple, and reliable. 
HikariCP is a “zero-overhead” production-ready JDBC connection pool. 
Does HikariCP make SQL queries faster. ?

ThreadPool vs ConnectionPool

Who manages the Connection Pool in Spring Boot?

```
Spring Boot
    ↓
DataSource
    ↓
HikariCP
    ↓
JDBC Driver
    ↓
Database
```


Does Hibernate maintain the Connection Pool?

```
Hibernate
    ↓
DataSource
    ↓
HikariCP
    ↓
Database
```



Hibernate + HikariCP

SessionFactory → Session management
Session        → Entity/persistence management
Transaction    → Commit/Rollback
HikariCP       → Connection management


What happens when we call connection.close()?

```
spring.datasource.hikari.maximum-pool-size=10
spring.datasource.hikari.minimum-idle=5
spring.datasource.hikari.connection-timeout=30000
spring.datasource.hikari.idle-timeout=600000
spring.datasource.hikari.max-lifetime=1800000

```

Pool size = 10 but 100 requests arrive. What happens?
- What happens if a connection is leaked?
- What happens if maximumPoolSize is too small?
- What happens if maximumPoolSize is too large?

If I have 5 application instances and pool size = 20, how many possible DB connections?

Pool size does not limit HTTP requests. 
It limits simultaneous database connections.

How to determine count of connection ?
- CPU Based 
- IO Based

HDD : Pool Size ≈ CPU Cores × 2 + Effective Spindle Count
Spindle : The Handle Present on Harddisk for writing.
SDD : Pool Size ≈ CPU Cores × 2 
