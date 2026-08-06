Transaction Management

├── ACID
│
├── Enable Transaction Management
│   ├── @EnableTransactionManagement
│   └── Transaction Proxy
│
├── @Transactional
│   ├── Class Level
│   └── Method Level
│
├── Transaction Manager
│   ├── PlatformTransactionManager
│   ├── Declarative Transaction Management
│   └── Programmatic Transaction Management
│
├── Transaction Propagation
│   ├── REQUIRED
│   ├── REQUIRES_NEW
│   ├── SUPPORTS
│   ├── MANDATORY
│   ├── NOT_SUPPORTED
│   ├── NEVER
│   ├── NESTED
│   ├── When to use what?
│   ├── Method1 → Method2 Combination
│   └── Different @Transactional Combination
│
├── Isolation Level
│   ├── READ_UNCOMMITTED
│   ├── READ_COMMITTED
│   ├── REPEATABLE_READ
│   ├── SERIALIZABLE
│   ├── Dirty Read
│   ├── Non-Repeatable Read
│   └── Phantom Read
│
├── Rollback
│   ├── Checked Exception Does Not Rollback By Default
│   ├── Unchecked Exception Rollback By Default
│   ├── rollbackFor
│   ├── noRollbackFor
│   └── Exception Caught and Swallowed
│
├── Proxy Related Issues
│   ├── Self Invocation Problem
│   ├── JDK Proxy vs CGLIB Proxy
│   ├── Access Modifier
│   │   ├── public
│   │   ├── protected
│   │   ├── default
│   │   └── private
│   ├── final Method
│   └── Bean Not Managed By Spring
│
├── Async + Transaction
│   └── @Async + @Transactional
│
└── Critical Concepts
    ├── Critical Code
    ├── Critical Code Segment
    └── Shared Resource