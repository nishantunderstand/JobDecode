Exception Handling 
Throwable
Throwable Hierarchy

1. Object
2. Throwable
3. Exception (Application Level Problem)
4. Checked Exception
5. UnChecked Exception
6. Error (JVM / System-Level Problem)
7. VirtualMachineError
8. OutOfMemoryError
9. StackOverFlow
10. NoClassDefFoundError

Exception
Exception Constructor
When we called an Exception Constructor ? What Actually Happened? Explain to me ? 
Exception Constructor vs throw 


Exception Methods

Types of Exception :
1. Predefined Exception
2. CustomException

Types
1. Checked Exception : FileNotFoundException, ClassNotFoundException , SQLException
2. UnChecked Exception : NullPointerException, ArrayIndexOutOfBound , ArithmeticException

Exception
1. Implicit
2. Explict

Handle Exception
1. try-catch
2. try-catch-finally
3. try-with-resource
4. throw vs throws
5. Final, Finally, Finalize

When finally block will not execute  
1. System.exit(0)
2. Exception 

return keyword in try , catch , finally block scenario Tricky Interview Question

[Return Statement in Try Catch Finally Block in Java - Scientech Easy](https://www.scientecheasy.com/2020/09/return-statement-in-try-catch-finally-block.html/)  
(You must practice it | This is Gold standard)

Shutdown Types
1. Normal 
2. Abnormal 
3. Graceful 

Graceful Shutdown
1. System.exit(0); 
2. System.exit(1); 
3. System.exit(2); 
Is it a naming/convention  ?

Java 7
Rethrowing of an Exception
Multi-Catch / Pipe Operator  ( | )

Autoclosable Interface  
Closeable and AutoCloseable  Interface 
Is it Associated with I/O resources ?

ChainedException
UnReachable Code Error
Can we write code after throw?
Child Exception Followed by Parent Exception
Method Overriding with Exception | Refer Method Notes

CustomExceptionClass , Which Class extends what Exception?
1. Checked
2. UnChecked

Checked Exception 
```
class AgeNotFoundException extends Exception {
    public AgeNotFoundException(String message) {
        super(message);
    }
}
```

Error vs Exception
Can we catch errors?
Can we catch Throwable?
StackOverflowError vs OutOfMemoryError
JVMFailure

### Java Exception Hierarchy    
![[image1.png]]