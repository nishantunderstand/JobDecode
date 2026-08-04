Spring Security

Spring Security Architecture
Incoming Request
FilterChain 
  UsernameAndPasswordFilterChain
AuthenticationProvider
AuthenticationManager
  LDAP
  OAuth
  DAO
PasswordEncoder BCryptPasswordEncoder
UserDetailService
  InMemory
  Database


ContextFacotry as Principal Oject Save ho jata hai


---

filter
Interceptor
PreHandle 
Posthandle 
afterCompletion


filter vs Interceptor

Transaction
Interface : JDKProxy
Not-Interface : CGLIBProxy

---
SpringBoot 2x
SpringBoot 3x
@Secured


@HasRole vs @HasAuthority
ROLE_ADMIN
ADMIN
Role vs Permission
Authentication vs Authorization 
Bearer Token
CSRF 
Stateful and Stateless

