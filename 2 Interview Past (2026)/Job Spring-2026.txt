SpringBoot Exception Handling 
Checked or Unchecked Exception 


@Controller 
@ResponseBody 
@ResponseEntity 
@RequestBody
@RequestEntity



----

@ResponseStatus	Simple exception
@ExceptionHandler	Custom response body banana ho
@RestControllerAdvice	Global handling

Who will get more priority ?



Synchronized Improvemnt Timeline

synchronized 
1 Thread at a Time  : Lock aka Reentrackt 
N Thread at a Time  : Seamphore
AtomicInteger 



How to solve Synchronization Problem ?
Mutex i.e. Locks or RetrantLocks
Synchronized Method or Block or Keyword
Seamphores 

Other Java Specific Solution



Difference Between Fork/Join Framework and ExecutorService in Java

ExecutorService : Java5
Fork/Join Framework : Java 8 
	Advanced Version of Thread Pool
	Work Steal Algorithm
		Whomever is free, Take the resource from occupied that how they work
------------------------------------


@Bean vs @Component in Spring Boot