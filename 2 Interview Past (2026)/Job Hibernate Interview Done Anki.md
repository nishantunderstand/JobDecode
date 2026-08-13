Hibernate
JPA
Spring JPA
Spring Data JPA


Topic Interviewer Favourite List

N+1 Query
@Transient

@OneToMany
@ManyToMany
@ManeToMany

L1Cache
L2Cache

Redis Cache 

Write me similar Topic

StoredProcedure, How to call it 

NamedQuery
Query


---

https://substack.com/home/post/p-184113452

---
25 Must-Know JPA + Hibernate Interview Questions

What is JPA, and how does it differ from Hibernate? (JPA is a specification; Hibernate is its implementation.)

What is an Entity in JPA? (Maps Java objects to database tables — the essence of ORM.)

Difference between POJO, DTO, and Entity? (POJOs are simple, DTOs transfer data, Entities persist data.)

What do Student and Long represent in CrudRepository<Student, Long>? (Entity type and primary key type.)

Purpose of @Id annotation? (Defines the primary key for persistence.)
What is a Named Query and where is it defined? (Reusable JPQL queries within entity classes.)
Named Query vs Native Named Query? (JPQL vs SQL — portability vs flexibility.)
Fetch Types in JPA? (LAZY for on-demand, EAGER for immediate fetching.)
Why is FetchType.LAZY default for @OneToMany? (Prevents unnecessary data fetching.)

What is the N+1 Select Problem? (Lazy loading triggers multiple DB calls.)
How does JOIN FETCH solve it? (Fetches associations in a single query.)
What are Cascade Types in JPA? (Propagate operations like persist or delete.)
CascadeType.REMOVE vs OrphanRemoval? (REMOVE cascades deletes; OrphanRemoval removes detached children.)

What happens to child entities if the parent is deleted? (Depends on cascade configuration.)
What is Level-1 Cache? (Session-level, managed by Hibernate.)
What is Level-2 Cache? (Shared across sessions — reduces DB calls.)
What shouldn’t be cached in Level-2 cache? (Frequently changing or sensitive data.)

What is SessionFactory? (Thread-safe, immutable factory for Sessions.)

Why isn’t Session thread-safe? (Scoped per transaction.)

Lifecycle of a Hibernate Session? (Transient → Persistent → Detached.)

@GeneratedValue strategies? (AUTO, IDENTITY, SEQUENCE, TABLE — default: AUTO.)

get() vs load() in Hibernate? (get() fetches now; load() returns proxy.)

Entity states in Hibernate? (Transient, Persistent, Detached.)

What is dirty checking? (Detects and updates changed entities automatically.)

Purpose of @Version annotation? (Enables optimistic locking for concurrency control.)


https://www.linkedin.com/posts/ramesh-fadatare_top-hibernate-interview-questions-and-answers-activity-7421954867050504192-RB1i/

Here is a list of all the interview questions asked in the video:
What is ORM? (0:13)
What is Java Persistence API or JPA? (0:49)
What is the Hibernate framework? (1:27)
How does Hibernate relate to JDBC? (2:01)
Explain the Hibernate architecture. (2:42)
What is Hibernate SessionFactory and how do you configure it? (3:41)
Is Hibernate SessionFactory thread-safe? (4:21)
What is Hibernate Session and how do you get it? (4:41)
Is Hibernate Session thread-safe? (5:22)
What is the difference between openSession and getCurrentSession? (5:42)
Explain the Hibernate transaction interface. (6:18)
What are the possible ways to configure object-to-table mapping? (6:53)
What is required for a Java object to become a Hibernate entity? (7:37)
Why should we not make an entity class final? (8:15)
What are the different states of a Hibernate entity? (8:40)
Explain Hibernate and JPA primary key generation strategies. (9:17)
What is HQL and what are its benefits? (9:54)
What is a named query in Hibernate? (10:36)
What are the benefits of named SQL query? (11:03)
What is cascading and what are the different types? (11:34)
Which types of relationships are available in Hibernate mapping? (12:09)
What are the different types of caches available in Hibernate? (12:41)
What design patterns are used in Hibernate? (13:19)
What is the difference between JPA and Hibernate? (13:52)


https://www.youtube.com/watch?v=SQ0Zw8rDQ1A


https://www.linkedin.com/posts/saikarthik2002_hibernate-interviews-questions-activity-7404346630105444352-0HJ9/


https://medium.com/@aymenfarhani28/jpa-hibernate-transactions-interview-questions-b91bf16b6560

https://www.linkedin.com/posts/shamdal-khokad-70277816a_here-are-the-top-10-most-asked-hibernate-activity-7320270613678358528-qEp4/


Here are the Top 10 Most Asked Hibernate Interview Questions:
What is Hibernate?

Answer:
Hibernate is an Object-Relational Mapping (ORM) framework for Java that maps Java classes to database tables and simplifies database interactions by handling CRUD operations, caching, lazy loading, etc.


---

are the advantages of using Hibernate?

Answer:

Simplifies database interactions

Eliminates boilerplate JDBC code

Provides automatic table creation

Supports HQL (Hibernate Query Language)

Caching support (first & second level)

Lazy loading & fetching strategies



---

What is the difference between get() and load() in Hibernate?

Answer:

get(): Returns null if the object is not found; hits the DB immediately

load(): Throws ObjectNotFoundException if not found; returns a proxy object and hits DB lazily



---

What is the difference between first-level and second-level cache in Hibernate?

Answer:

First-level cache: Enabled by default, scoped to a session

Second-level cache: Scoped to SessionFactory; needs explicit configuration (like Ehcache, Infinispan)



---

What is the use of the @Entity and @Table annotations?

Answer:

@Entity: Marks a class as a Hibernate entity

@Table: Specifies the table name mapped to the entity class



---

What is the difference between HQL and SQL?

Answer:

HQL (Hibernate Query Language): Object-oriented and works with entity objects

SQL: Table-oriented and works with database columns



---

What are the different states of an object in Hibernate?

Answer:

Transient: Not associated with any session

Persistent: Associated with an open session

Detached: Once associated but currently not in a session



---

What is cascading in Hibernate?

Answer:
Cascade types (PERSIST, MERGE, REMOVE, REFRESH, ALL) tell Hibernate what to do with related entities when the parent entity is affected.


---
What are the fetching strategies in Hibernate?

Answer:

Eager: Loads the associated entities immediately

Lazy: Loads associated entities only when accessed (default)



---

What is the difference between save(), persist(), and merge()?

Answer:

save(): Returns generated ID, works outside transactions

persist(): Doesn't return ID, needs active transaction

merge(): Used to update a detached object


============

@JoinColumn
mappedBy
Owning Side vs Inverse Side
FetchType.LAZY vs EAGER
CascadeType
orphanRemoval
Bidirectional vs Unidirectional
N+1 Query problem

==========


Query
NamedQuery
NaiveQuery


SQL
HQL
JPQL


Parameter
Position Parameter

What else are related to Query


============

@Entity
@Table
@Id
@GeneratedValue
@Column
@Transient


=============
@OneToOne
@OneToMany
@ManyToOne
@ManyToMany


-----------------


EntityManagerFactory
ThreadSafe
Heavy
Singleton
EntityManagerFactory factory = new EntityManagerFactory.builSessionFactory();

EntityManager
NotThreadSafe
Light 
Interact With DB

	EntityManager em = EntityManagerFactory

PerisitenceContext
Same as L1 Cache Equivalent


Transaction
You need to Create it manually
	Types 
	Programmatic
	EntityTransaction tx = em.getTransaction();
	tx.begin();
	e.perisit();
	tx.commit();
	
	Declartic 
	
=======================	


Hibernate 

SessionFactory : ThreadSafe
	Resource Heavy
	1 Application = 1 SessionFactory
	It had the Meta Data
	Table Properties, Schema
		SessionFactory factory = new Configuration.configure("hibernate.cfg.xml").buildSessionFactory();
		Shared Accross Session
		Long Lived
	Singleton 
	
Session : Not ThreadSafe
	1 SessionFactory  = N Session
	Session session = sesssionFactory.openSession();
	Session session = sesssionFactory.getSession();
	Short Lived
	Not ThreadSafe
	Used per session / per transaction
		
Transaction : No Concept Of ThreadSafe , Single Thread Application
	1 Session  = N Transaction, But 1 Active Transaction
	Transaction tx = session.beignTransaction();
	session.save();
	tx.commit();
	
	
	
	
Can we create multiple SessionFactory ?	