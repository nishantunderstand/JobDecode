# Transaction Management
Transaction Management
  
ACID 
  
Bank Example 
How to achieve Consistency ?
  
How to Enable Transaction Management ?
@EnableTransactionManagement
Transaction Proxy
  
Who Creates the Proxy?
```
Client
   ↓
Proxy
   ↓
PlatformTransactionManager.begin()
   ↓
Business Method
   ↓
PlatformTransactionManager.commit()

```  
  
  
@Transactional Used at which Level ? 
Class Level
Method Level
  
Best Practice to use at which Layer ?
Controller Layer
Service Layer (Best Practice)
Repository Layer
  
  
@Transactional Annotation
Access Modifier
private
package-private, protected : CGLIB proxy can intercept (Spring 6+)
public 
  
Non-Access Modifier
final 
  
Interview Answer : public 
  
Rollback :
Rollback + Exception 
1. Checked Exception Does Not Rollback By Default    
2. Unchecked Exception Rollback By Default    
  
rollbackFor
noRollbackFor
Exception Caught and Swallowed
  
Based On Business Requirement : 
Force Rollback For Checked Exception
Prevent Rollback
  
```
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

```  
  
Transaction Manager Provide 
1. PlatformTransactionManager (Interface)    
2. JpaTransactionManager     
3. DataSourceTransactionManager     
4. JtaTransactionManager     
  
Which Transaction Manager is used in Spring Boot with Hibernate?
  
Types : 
1. Declarative Transaction Management
2. Programmatic Transaction Management (Manually)
  
  
Transaction Propagation
1. REQUIRED / REQUIRES_NEW    
2. SUPPORTS / NOT_SUPPORTED    
3. MANDATORY / NEVER    
4. NESTED    
  
When to use what?
Method1 → Method2 Combination
Different @Transactional Combination
  
  
Spring's default rule:
Rollback only for RuntimeException and Error.
  
Exception Caught and Swallowed
Case 1 : Exception Propagates => Rollback
Case 2 : Exception Caught => Commit 
  
|   |   |   |
|---|---|---|
|Caller|Callee|Result|
|REQUIRED|REQUIRED|Same TX|
|REQUIRED|REQUIRES_NEW|New TX|
|REQUIRED|SUPPORTS|Join TX|
|No TX|SUPPORTS|No TX|
|REQUIRED|MANDATORY|Join TX|
|No TX|MANDATORY|Exception|
|REQUIRED|NOT_SUPPORTED|Suspend TX|
|REQUIRED|NEVER|Exception|
  
  
  
Can inner transaction commit, while outer transaction rolls back?
  

Problem of Isolation Level (Order)
1. Dirty Read (Reading data that is not yet committed.)    
2. Non-Repeatable Read (Same row read twice gives different values.)    
3. Phantom Read (Same query returns extra rows.)    
  


Isolation Level (Order)
1. READ_UNCOMMITTED (Less Secure) | Dirty Read ,Non-Repeatable Read, Phantom Read    
2. READ_COMMITTED  -> PostgreSQL | | Non-Repeatable Read, Phantom Read    
3. REPEATABLE_READ -> MySQL | | Phantom Read    
4. SERIALIZABLE (Most Secure)     
  

Try to remember by example
  
DIRTY READ  🤔🤔🤔  TODO
A: UPDATE → 5000 (No COMMIT)
B: SELECT → 5000
A: ROLLBACK → 10000
→ B read UNCOMMITTED data
Which data we will see 5000 or 10000 
  
NON-REPEATABLE READ
A: SELECT → 10000
B: UPDATE → 7000 + COMMIT
A: SELECT → 7000
→ Same ROW, different VALUE
  
PHANTOM READ
A: SELECT → 3 rows
B: INSERT → new matching row + COMMIT
A: SELECT → 4 rows
→ Same QUERY, different ROW COUNT
Remember:
Dirty          → Uncommitted
Non-Repeatable → Same row changed
Phantom        → New row appeared
  
UnexpectedRollbackException 
  
  



