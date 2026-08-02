JDK 
JRE
JVM


JDK = JRE + JVM

JVM 
ClassLoader

Runtime Area
MethodArea
PCRegister
Stack

Execution Engine @@
Interpreter
Compiler


Native Method Stack
Native Method Interface


---
ClassLoader
BootStrapClassLoader : JAVA_HOME/lib
SystemClassLoader : JAVA_HOME/lib/ext
ApplicationClassLaoder : 

Delegation-Hierary

Role of ClassLoader
1. Linking 
2. Verfiying
3. Preparing 



---

Heap Java7
Young Generation
Old Generation
Permanent Generation


Heap Java7
Young Generation
  Eden
  Surviour S0
  Surviour S1
Old Generation


Student s1 = new Student();
s1 = Stack 
new : Heap -> Eden

Every Object has a property called age counter.
After a threshould i.e. 15 Move From Next Step

---

Garbage Collector 

Stop the world Scenario

1. Serial
2. Parallel
3. CMS Conucurrent Mark & Sweep
4. G1 GC
5. Z GC
6. Shendaho GC 

CMS 
1. Live Object
2. Dead Object

Rules of GC 
1. UnReferenced Object
2. Object Referred to Null
3. Island of Isolation