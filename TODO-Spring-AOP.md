AOP 
Before
After
Around 

PointCut



---

├── 4. Web Request Flow
│     ├── Filter
│     ├── DispatcherServlet
│     ├── HandlerInterceptor
│     │     ├── preHandle()
│     │     ├── postHandle()
│     │     └── afterCompletion()
│     ├── Controller
│     └── Response

---

└── 5. Interview Questions
      ├── JDK Proxy vs CGLIB
      ├── Why doesn't @Transactional work inside the same class?
      ├── Filter vs Interceptor
      ├── AOP vs Interceptor
      ├── @Transactional vs AOP
      └── How does Spring create proxies?


---

Transaction Management
@EnableTransactionMangement On MainSpringBoot Class
@Transactional
Transaction Proxy
Propagation
Isolation
Rollback
Self Invocation Problem
Access Modifier : public, protected , private , default
final Method 
Checked Exception Does Not Rollback By Default
Wrong Propagation Usage
Async Method + Transaction
Exception Caught and Swallowed
Wrong Bean Scope / Proxy Disabled
Will it work on protected method? JDKProxy , CGLIB Proxy ?


Critical Code 
Critical Code Segment 
Shared 

ACID 
Class / Method Level

Transaction Manager
Programmatic
Declarative

Transaction Propagation 
When to use what ? Learn Example 
REQUIRED
REQUIRED_NEW
SUPPORTS
MANDATORY
NOT_SUPPORTED
NEVER
Transaction Manager Hierarachy (Just Know, No need to studty)
Method1 - Method2 + Different Combination of @Transactional Annotation



--- 
ASPECT J (Read Later )


---
Proxy

Why Proxy ?

Types 
1. Static Proxy
2. Dymanic Proxy

Problem with Static proxy

Dymanic Proxy Implementation
1. JDK Proxy
2. CGLib Proxy

How Spring Chooses a Proxy
1. Interface Present → JDK Proxy
2. No Interface → CGLIB Proxy

Self Invocation Problem
Current Class Problem
Why Proxy is Bypassed
Solutions


Parent vs Child Method Calls
Super Method Calls
Overridden Methods
Proxy Limitations


Current Class Problem (Self Invocation)
Current Class → Proxy ❌
External Class → Proxy ✅
Why self-invocation bypasses AOP


Proxy Limitations
private methods
final methods
final classes (CGLIB limitation)
static methods			



Interview Questions
Proxy vs Decorator
Static Proxy vs Dynamic Proxy
JDK Proxy vs CGLIB
Why doesn't @Transactional work inside the same class?
Why are final methods/classes not proxied by CGLIB?
Why are private methods not advised by Spring AOP?
Which proxy does Spring Boot use?



