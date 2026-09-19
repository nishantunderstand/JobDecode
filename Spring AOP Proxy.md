# Proxy 
Why do we need Proxy ?
  
Types 
1. Static Proxy | CompileTime
2. Dynamic Proxy | RunTime
  
Problem with Static proxy
  
Dynamic Proxy Implementation
1. JDK Proxy
2. CGLib Proxy (Code Generation Library)
  
How Spring Chooses a Proxy
1. Interface Present → JDK Proxy
2. No Interface → CGLIB Proxy
  
JDK Proxy vs CGLIB Proxy
  
Spring Boot/Spring generally uses CGLIB proxies by default.
  
 Do I need to Enable it ?  Is it Enabled by Default ?
  
How to Enable JDK Proxy  ?
@EnableAspectJAutoProxy(proxyTargetClass = false) → JDK proxy when possible.
🤔🤔🤔  Can we force springboot to use JDK or CGLIB ? Or is it enabled by Default.
  
Proxy Limitations 👈👈👈👈👈
1. private methods    
2. final methods    
3. final classes (CGLIB limitation)    
4. static methods       
  
Spring 6 : New Modification

| Method          | Spring AOP                          |
| --------------- | ----------------------------------- |
| public          | ✅                                   |
| protected       | ✅ with class-based proxying         |
| package-private | ✅ with class-based proxying         |
| private         | ❌                                   |
| final           | ❌ for proxy-based method overriding |
| static          | ❌                                   |
  
  
CGLIB Limitation
1. Needs Inheritance
2. Cannot Override final/private
  
  
Self Invocation Problem (Current Class Problem)
Why does self-invocation bypass AOP ?
1. Current Class → Proxy ❌
2. External Class → Proxy ✅ 
  
Method Call Behaviour Related to Proxy 
3. Parent vs Child Method Calls    
4. Super Method Calls    
5. Overridden Methods    
6. Call From Current Class Method    
7. Call From External Class Method

![[Spring AOP Method Call.png]]
  
  
Proxy 
The proxy is what allows Spring to intercept things such as:  👈👈👈👈👈
@Transactional
@CircuitBreaker
@Retryable
@Cacheable
@Async
  
  
  
![[Spring Bean Proxy.png]]

Interview Questions
1. Proxy vs Decorator 🤔🤔🤔     
2. How does Spring create proxies?  
3. Static Proxy vs Dynamic Proxy  
4. JDK Proxy vs CGLIB             
5. Why doesn't @Transactional work inside the same class? 🤔🤔🤔 
6. Why are final methods/classes not proxied by CGLIB?            
7. Why are private methods not advised by Spring AOP?             
8. Which proxy does Spring Boot use?                              
9. Filter vs Interceptor                                          
10. AOP vs Interceptor                                            
11. @Transactional vs AOP