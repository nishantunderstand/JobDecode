Spring Security Flow

Client -> ServletAPI


ServletAPI --> DelegateFilterProxy -->FilterChainProxy --> 
SecurityFilterChain--> 

AuthenticationManager --> 
ProviderMangaer -->
AuthenticationProvider -->

SpringApplication









====================
@SpringBootApplication
@SpringBootConfiguration : 
@SpringBootConfiguration is a special version of @Configuration created specifically for Spring Boot.

	@Configuration can exist in many modules, but @SpringBootConfiguration marks a single 	entry-point configuration — the class that starts Spring Boot

	Registers beans defined in the application
	Enables Java-based configuration
	Acts as the root configuration for ApplicationContext

@EnableAutoConfiguration  : @EnableAutoConfiguration (auto setup based on classpath)

@ComponentScan : Scan Current Package + sub-package for Sterotype Annotation








---

How @Primary is different From @Qualifier 

@Lazy
How to convert to eager

@Lazy(value=false) : Now it is eager


@Import vs @ImportResource


# JDBC 

What about Unstructured ?
CSV?
Raw File?
Excel Sheet ?
Text File 
File ?
How to fetch or establish Connection with them ???

Is JDBC only related to RDBMS ? Will it be used to fetch Non-Relational Database as well ?

Spring 
JDBC
ORM
OXM
JMS 
Transaction




# APIResponse 

status
httpStatus
message
msID : Microservice Identifier / Request ID / Trace ID
data


BuilderDesignPattern

GenericResponseWrapper

Factory + Builder Hybrid Design Pattern


APIResponse
APIResponseFactory
	success
	failure
	error
	You can merge them as well.


# Pagination
REST API Design: Filtering, Sorting, and Pagination



Types
OffSet Based
PageBased
Keyset Pagination or Seek Pagination
TimeBased
Cursor Based 

https://www.merge.dev/blog/rest-api-pagination
https://apisyouwonthate.com/blog/api-design-basics-pagination/ 

https://restfulapi.net/api-pagination-sorting-filtering/

Payload 
	Header
	Body
	
	
APIResponse  : Generic
PageApiResponse : Generica (Backward Compatiablity)
ApiPageableResponse : List	



---

✔ Versioning (/api/v1/...)
✔ Global Exception Handler (@RestControllerAdvice)
✔ API Response Wrapper
✔ Request Validation
✔ Logging + MDC
✔ Security (Spring Security or API keys)
✔ Swagger (OpenAPI)
✔ Pagination
✔ Tests