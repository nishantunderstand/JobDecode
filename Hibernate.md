Hibernate ORM 

Hibernate Lifecycle - GeeksforGeeks
https://www.geeksforgeeks.org/advance-java/hibernate-lifecycle/

Hibernate.cfg.xml  🤔🤔🤔 

Hibernate Provides
1. SessionFactory
2. Session
3. Transaction

Does Hibernate provide PersistentContext ?  🤔🤔🤔 

SessionFactory vs Session
Session vs Connection  🤔🤔🤔 

SessionFactory
1. Heavyweight object
2. Thread-safe
3. Usually created once per application
4. Stores metadata about mappings/tables
5. Creates Session objects

Session
1. Lightweight object
2. Not thread-safe
3. Represents a single unit of work / interaction with DB

Created By using
1. sessionFactory.openSession()
2. sessionFactory.getCurrentSession()

Hibernate vs ConnectionPool vs JDBCConnectionPool vs ThreadPool vs HikariCP

Can Hibernate Work Without JPA?
Can JPA Work Without Hibernate?
Hibernate vs JPA


Hibernate LifeCycle
1. Transient (New) State
2. Persistent State / Managed State
3. Detached State / UnManaged State
4. Removed (Deleted) State

Transient → Persistent → Detached → Removed
New → Managed → Unmanaged → Deleted


C : save(), persist()       
R : get(), load(), find() 
U : update(), merge()       
D : delete(), remove()      

|           |                   |              |
| --------- | ----------------- | ------------ |
| Operation | Hibernate         | JPA Standard |
| Create    | save()            | persist()    |
| Read-One  | get(), load()     | find()       |
| Read-All  | 🤔🤔🤔            |              |
| Update    | update(), merge() | merge()      |
| Delete    | delete()          | remove()     |

Hibernate LifeCycle 

> Hibernate implements the JPA entity lifecycle.

Is JPA LifeCycle different from Hibernate ? 🤔🤔🤔 
JPA has a Cycle, As it is an interface ? 🤔🤔🤔

```
NEW/TRANSIENT
       |
       | persist/save , update / merge
       V
PERSISTENT / MANAGED
       |
       | close/clear/evict , evict/detach
       V
DETACHED / UNMANAGED
       |
       | merge/update
       V
PERSISTENT / MANAGED
       |
       | remove/delete
       V
REMOVED / DELETED
```

![[JDBC Hibernate LifeCycle.png]]

────────────────────────────────────────────────────────────

Hibernate Method :

1. save() vs persist()
2. update() vs merge()
3. evit() vs detach()  vs clear()  🤔🤔🤔 
4. save() vs flush()  🤔🤔🤔 
5. flush() vs commit()  🤔🤔🤔 
6. get() vs load() 
7. clear() vs flush() vs evict()  🤔🤔🤔 
8. save() vs persist() vs merge()


🤔🤔🤔 

First identity which is the Hibernate Method ?
Which is the JPA Method ?

────────────────────────────────────────────────────────────
Query
1. SQL
2. HQL
3. JPQL
4. CriteriaAPI
5. NativeQuery i.e. SQL Query
6. NamedQuery
7. NamedQuery vs NativeQuery
8. CriteriaAPI vs JPQL

HQL works on Table or Entity?

HQL vs JPQL

JPQL       -> Fixed Query
Criteria   -> Dynamic Query
Native SQL -> Complex Query
NamedQuery -> Reusable Query
HQL        -> Hibernate Query

RelationShip
1. One to One
2. One to Many 
3. Many to One
4. Many to Many
	1. Junction Table 

How many tables are created ?
1. @OneToMany     -> LAZY
2. @ManyToMany    -> LAZY
3. @OneToOne      -> EAGER
4. @ManyToOne     -> EAGER


Fetching Strategy 🤔🤔🤔 
1. Eager 
2. Lazy
3. FetchType 🤔🤔🤔 
4. FetchJoin

Fetch Type 
1. FetchType.LAZY
2. FetchType.EAGER

N+1 Problem,

N+1 Problem   🤔🤔🤔
1. One department has many employees.
2. How would you decide on a DB for M:N  ??
3. 2 Table + 1 Common Table  Junction Table 


Occur in which kind of Relationship Why does it happen? How to solve it?
Lazy -> Eager (This will not solve the Problem) 🤔🤔🤔 
Fetch Join
EntityGraph
Batch Fetching 
Write Code as well  🤔🤔🤔 



Locking 
1. Optimistic 
	1. @Version
2. Pessemistic

Hibernate Cache
1. First Level Cache / L1 Cache / (Session cache)
2. Second Level Cache/  L2 Cache / (SessionFactory cache)
3. Query Cache

You can enable this L2 Cache 

L1 vs L2 vs QueryCache
Cache Friendly , Shared , 
Which one is persistent ? Per Session ? 

StoredProcedure 🤔🤔🤔 
How to create it 🤔🤔🤔 

# Cascade 

- Cascade vs Orphan Removal 
- Cascade = "pass the operation to the child."
- Orphan removal = "child no longer belongs to parent, delete it."

Cascade 
Cascade means parent operation automatically applies to child.

Cascade Type  👈👈👈👈👈
JPA Behaviour (Entity Level)
Database Behaviour (Database Level)

Cascade JPA Behaviour
1. CascadeType.ALL
2. CascadeType.PERSIST
3. CascadeType.MERGE
4. CascadeType.REMOVE
5. CascadeType.REFRESH
6. CascadeType.DETACH

PERSIST  -> Save Parent  → Save Child
MERGE    -> Update Parent → Update Child
REMOVE   -> Delete Parent → Delete Child
REFRESH  -> Reload Parent → Reload Child
DETACH   -> Detach Parent → Detach Child
ALL      -> PERSIST + MERGE + REMOVE+ REFRESH + DETACH

orphanRemoval 
![[JDBC Cascade Orphan Removal.png]]

![[JDBC Cascade Classification.png]]



Cascade Database Behaviour  
foreign-key relationship.
Maintains Referential Integrity 
1. Cascade
2. Restrict
3. Set Null
4. No Action



![[JDBC Cascade On Delete Action.png]]


![[JDBC Cascade JPA And Database Classification.png]]





![[JDBC JPA Cascade.png]]


@Temporal vs Modern Java Time 
Modern Approach
private LocalDate joiningDate;
private LocalDateTime createdAt;
private Instant updatedAt;


Auditing 
@CreatedDate
private LocalDateTime createdAt;

@LastModifiedDate
private LocalDateTime updatedAt;

@CreatedBy
private String createdBy;

@LastModifiedBy
private String updatedBy;

@EnableJpaAuditing




