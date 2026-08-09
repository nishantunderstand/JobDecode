Transaction Management

ACID 

Bank Example 
How to achieve Consistency ?


Enable Transaction Management
@EnableTransactionManagement
Transaction Proxy


Who Creates the Proxy?
Client
   ↓
Proxy
   ↓
PlatformTransactionManager.begin()
   ↓
Business Method
   ↓
PlatformTransactionManager.commit()


@Transactional
Class Level
Method Level



@Transactional Annotation
Access Modifier
private
package-private, protected : CGLIB proxy can intercep (Spring 6+)
public 

Non-Access Modifier
final 

Interview Answer : public 

Rollback
Checked Exception Does Not Rollback By Default
Unchecked Exception Rollback By Default
rollbackFor
noRollbackFor
Exception Caught and Swallowed

Based On Business Requirment : 
Force Rollback For Checked Exception
Prevent Rollback

@Transactional(
    propagation = Propagation.REQUIRED,
    isolation = Isolation.READ_COMMITTED,
    readOnly = false,
    timeout = 30,
    rollbackFor = Exception.class,
    noRollbackFor = RuntimeException.class
)
public void save() throws Exception {
    throw new Exception();
}


Transaction Manager Provide
PlatformTransactionManager
JpaTransactionManager 


Which Transaction Manager is used in Spring Boot with Hibernate?

Types : 
Declarative Transaction Management
Programmatic Transaction Management (Manually)



Transaction Propagation
REQUIRED
REQUIRES_NEW
SUPPORTS
MANDATORY
NOT_SUPPORTED
NEVER
NESTED
When to use what?
Method1 → Method2 Combination
Different @Transactional Combination



Spring's default rule:
Rollback only for RuntimeException and Error.


Exception Caught and Swallowed
Case 1 : Exception Propagates => Rollback
Case 2 : Exception Caught => Commit 





Study Later

| Caller   | Callee        | Result     |
| -------- | ------------- | ---------- |
| REQUIRED | REQUIRED      | Same TX    |
| REQUIRED | REQUIRES_NEW  | New TX     |
| REQUIRED | SUPPORTS      | Join TX    |
| No TX    | SUPPORTS      | No TX      |
| REQUIRED | MANDATORY     | Join TX    |
| No TX    | MANDATORY     | Exception  |
| REQUIRED | NOT_SUPPORTED | Suspend TX |
| REQUIRED | NEVER         | Exception  |


Can inner transaction commit, while outer transaction rolls back?



Isolation Level (Order)
READ_UNCOMMITTED (Less Secure) | Dirty Read ,Non-Repeatable Read, Phantom Read
READ_COMMITTED  -> PostgreSQL | | Non-Repeatable Read, Phantom Read
REPEATABLE_READ -> MySQL | | Phantom Read
SERIALIZABLE (Most Secure) 


Problem of Isolation Level (Order)
Dirty Read (Reading data that is not yet committed.)
Non-Repeatable Read (Same row read twice gives different values.)
Phantom Read (Same query returns extra rows.)


Proxy Related Issues
Self Invocation Problem
JDK Proxy vs CGLIB Proxy
Access Modifier
public
protected
default
private
final Method
Bean Not Managed By Spring



Async + Transaction
@Async + @Transactional


@Async + @Transactional

What is @Async?
@Async executes a method in a different thread.

Scenario 1 : @Transactional → @Async
Does @Async inherit transaction?
Scenario 2 : @Transactional + @Async on Same Method
Scenario 3 : Transaction Calls Async Method
Scenario 4 : Outer Transaction Rollback
Why doesn't @Async share transaction?


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