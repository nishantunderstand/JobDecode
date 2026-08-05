Constructor
Constructor vs Method 
Constructor Chaining (this + super)
Constructor + Access Modifier
Constructor + Non Access Modifier

Type of Constructor
Default Constructor
No-Argument Constructor
Parameterized Constructor
Private Constructor
Copy Constructor 

Constructor Overloading 
Constructor Overriding 
Constructor Hiding
Constructor Calling 


Instance Initializer Block vs Constructor
Static Block vs Constructor
Object Initialization Sequence

Constructor + Inheritance


Constructor + Serialization
Constructor + Reflection
Constructor + Cloning 

Types of Copy 
Shallow Copy
Deep Copy

Clone vs Copy Constructor


---

Method 
Method Signature

Types of Method 
Instance Method
Static Method
Abstract Method
Final Method
Native Method
Synchronized Method
Default Method (Interface)
Private Method (Java 9+ Interface)
Static Method (Interface)

Method Overloading 
Method Overiding
Method Hiding



Method + Access Modifiers
Method + Non-Access Modifiers

Argument vs Parameter
Pass By Value

Method Return Type


Method & Exception Handling
Exception Rules in Method Overriding
Checked vs Unchecked Exceptions in Overriding


String[] args vs String... args

Varargs vs Array Parameter

---

Modifiers
Access Modifier
private
package-private | default
protected
public

Non-Access Modifiers
abstract
static
final
volatile
transient
synchronized
sealed (Java 17+)
non-sealed (Java 17+)


---

Blocks

Instance vs Static Block vs Construtor


Student s1 = new Student();
Student s2 = new Student();
Static Block
Instance Block 1
Construtor 1
Instance Block 2
Construtor 2

Complete Order of Execution
Class Loading
      ↓
Static Blocks (Top → Bottom)
      ↓
main() Starts
      ↓
new Student()
      ↓
Instance Blocks (Top → Bottom)
      ↓
Constructor


Can a static block create an object?

Multiple Static Blocks    → Top → Bottom
Multiple Instance Blocks  → Top → Bottom
Object Creation           → Static → Instance → Constructor
Static Block              → Once per Class
Instance Block            → Every Object
Constructor               → Every Object (after instance blocks)


---

Static And Final Keyword

Static 
Static Class
Static Nested Class
Static Method 
static Variable
Static Block

Final 
Final + Inheritance
Final Class
Final Method
Final Variable

final vs finally vs finliaze

---

this and super keyword

this 
current class

super 
parent class

Interview Question :
Can we use this() and super() together?
Does every constructor call super()?
What happens if the parent has only a parameterized constructor?
Can we use this inside a static method?
Can we use super inside a static method?
Can we write super.super?
Can this be assigned to another variable?


---
Inner Class

Outer Class
Static Nested Class
Non-Static Nested Class
Member Inner Class
Local Inner Class
Anonymous Inner Class

Nested Interface
Nested Enum
Nested Record Class (Java 16+)
Nested Abstract class
Nested Method  (Not Allowed)

Interview 
Difference between Inner Class and Static Nested Class?
Can a static nested class access instance variables?
Can an inner class have static members? 
Before Java 16 & After Java 16
Can a class be both static and abstract?
Anonymous Class vs Lambda