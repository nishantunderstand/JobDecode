
Spring Design Pattern
Loose Coupling 
Dependency Injection
Bean Scope
Singletong Bean Scope
AOP , Proxy, Transaction
FrontController DispatcherServlet
MVC


---
Proxy Design Pattern


https://www.instagram.com/reels/DblPyp6Mwip/

### Spring Design Patterns — Default/Internally Used

1. **Singleton Pattern** → Default Spring Bean scope
2. **Factory Pattern** → `BeanFactory`, `ApplicationContext`
3. **Proxy Pattern** → `@Transactional`, `@Cacheable`, AOP
4. **Template Method Pattern** → `JdbcTemplate`, `RestTemplate`
5. **Strategy Pattern** → `HandlerMapping`, interchangeable implementations
6. **Observer Pattern** → Spring Application Events
7. **Front Controller Pattern** → `DispatcherServlet`
8. **Dependency Injection Pattern** → IoC / `@Autowired`
9. **Adapter Pattern** → Spring MVC adapters
10. **Decorator Pattern** → Servlet Filters / Spring wrappers
11. **Chain of Responsibility Pattern** → Spring Security Filter Chain
12. **Facade Pattern** → `ApplicationContext` providing simplified access to Spring services
13. **Builder Pattern** → APIs such as `UriComponentsBuilder`