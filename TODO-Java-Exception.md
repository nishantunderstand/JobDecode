Exception


Throwable 
Exception Hierarchy 

Exception
Checked 
Unchecked / RunTime Exception


How to write Exception
Checked Exception
UnChecked Exception
In this case , You are going to extend which one ???


How to handle it ?
Try 
Catch 
Finally


throw vs throws 

try with resource


Pipe Operator 
Unreachable Code Error

Child Exception Followed by Parent Exception



---

Checked Exception Example 

public class AgeNotFound extends Exception{
  
  public AgeNotFound(String msg){
    super(msg);
  }
}

RunTime Exception
public class AgeNotFound extends RuntimeException{
  public AgeNotFound(String msg){
    super(msg);
  }
}



Method Overriding with Exception


Chained Exception
Exception Propagation


Exception with SpringBoot

ExceptionHandler
