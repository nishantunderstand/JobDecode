JPA is a Interface, It Provides 

| Hibernate                    | JPA                  |
| ---------------------------- | -------------------- |
| SessionFactory               | EntityManagerFactory |
| Session                      | EntityManager        |
| Transaction                  | EntityTransaction    |
| First Level Cache (L1 Cache) | Persistence Context  |

- EntityManagerFactory vs EntityManager
- Persistence Context vs EntityManager 🤔🤔🤔 
- What's the Difference ? It is parent and its subChild  🤔🤔🤔 
- Persistence Context vs L1 Cache
- Persistence Context = L1 Cache +  Dirty Checking + Entity Lifecycle Management
- Does JPA have L1 Cache ?
- Doesn’t it belongs to Hibernate 🤔🤔🤔 


Transaction Types
1. Programmatic Transaction
2. Declarative Transaction

Rollback + Exception
1. Checked  : Rollback does NOT happen.
2. Unchecked : Rollback Happen

RollbackBehaviour
1. Implicit Behaviour :  
2. Explicit Behaviour 

Implicit Behavior : Spring rolls back automatically for: RuntimeException , Error
Transaction + Method
Transaction + Access Modifier
Transaction Called from Current / Different Class
Transaction + Self Invocation Problem

Transaction Propagation Types
1. REQUIRED / REQUIRED_NEW
2. SUPPORTED / NOT_SUPPORTED
3. MANDATORY
4. NEVER
5. NESTED

Will Transaction Work 
@Transactional
public void methodA() {
   methodB();
}

[[Spring AOP Transaction Management]]
