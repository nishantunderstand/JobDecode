JDK 
JRE
JVM

JDK = JRE + JVM

JVM 
ClassLoader

Runtime Area / JVM Memory
A. Shared Memory (Shared By Each Thread)
B. Thread Memeory (Each thread gets its own)

1. Method Area (Shared) | MetaSpace | Class MetaData
2. Heap (Shared)  | Object 
3. Stack 
4. PCRegister
5. Native Method Stack

Execution Engine 
1. Interpreter
2. Compiler
3. Garbage Collector

Native Method Interface
Native Method Libraries

Why is Java called both interpreted and compiled?



---

Class Loader Responsbility 
1. Loading 
   1. Read .class File
   2. Generate binary Data
   3. Save info in method area
      1. Fully Qualified Name 
      2. Whether .class is realted to class or Enum
      3. Modifier variables and Method Information
2. Linking 
   1. Verification
      1. Enusure correctess of .class file
      2. Check for format
      3. java.lang.VerfiyError if Verification fails
   2. Preparation
      1. Allocates memory for static members
      2. Intialize memory to default values
   3. Resolution
      1. Transform symbolic reference to direct references
3. Initliazation
   1. Static variables are assigned with values
   2. Executed from top to bottom

ClassLoader Types
1. BootStrap ClassLoader : JAVA_HOME/lib : Load Core Java Classes
2. Extension/Platform ClassLoader : JAVA_HOME/lib/ext
3. System/Application ClassLaoder : (Your Project Classes, External library)
   1. Child of Extension Class Loader
   2. Load Class From applicaiton path
   3. Enviroment Variable mapped to java.class path

ClassLoader Delegation-Hierarchy
Application ClassLoader
Platform ClassLoader
BootStrap ClassLoader

Why Parent Delegation?
Security
Prevent duplicate class loading
Better performance through caching

Can Parent Delegation Be Broken?

---

Heap Memory

Heap Java7
1. Young Generation
2. Old Generation
3. Permanent Generation(PermGen)

Heap Java8
1. Young Generation  
2. Old Generation
3. MetaSpace

Young Generation
1. Eden
2. Surviour S0
3. Surviour S1
  
Object Aging  
Promotion Threshold

Every Object has a property called age counter.
After a threshould i.e. 15 Move From Next Step

Difference between Minor GC, Major GC and Full GC?

Student s1 = new Student();
s1 = Stack 
new : Heap -> Eden


---

Garbage Collection 

Stop the world Scenario

GC Roots
1. Local Variables
2. Static Variables
3. Active Thread
4. JNI References

Types of Garbage Collectors
1. Serial
2. Parallel
3. CMS Conucurrent Mark & Sweep
4. G1 GC
5. Z GC
6. Shenandoah GC 

CMS 
1. Live Object
2. Dead Object

Rules of GC 
1. UnReferenced Object
2. Object Referred to Null
3. Island of Isolation

Does GC immediately delete an eligible object?

What is Memory Leak ? How to identify it ?

Types of Error
1. OutOfMemoryError 
2. StackOverflowError 

Difference between OutOfMemoryError and StackOverflowError?

finalize() Method

JVM TroubleShoooting 
1. Heap Dump
2. Thread Dump
3. jstack
4. jmap
5. jcmd
6. VisualVM

Heap Dump & Thread Dump Analysis
Why CMS was removed?
Why Metaspace introduced?
How JVM decides object promotion from Young to Old Generation?

Reference Types
1. Strong Reference
2. Weak Reference
3. Soft Reference
4. Phantom Reference

JVM Tunning


Class.forName("Student"); vs ClassLoader.loadClass("Student");


During which phase are static variables assigned their actual values?

---
Study Later
Tiered Compilation
Modern Java now has 2Compiler
C1, C2
Code Cache
How to run Java With Compile ? Java 11+
Java Test.java 