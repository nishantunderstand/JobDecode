Q:What is the difference between System.out, System.err, and System.in?
A:System.out, System.err 
	Similarity : 
		Used to printOut
		PrintStream
	Difference : 
		In Log -> 
		System.out => output.log
		System.err => error.log
	System.in	
		For Input to System
		InputStream
		To Use, we need to create Scanner class for taking input with the system.in.
	 
Q:Difference in the use of print, println, and printf.
A:Similarity : Used for Printing
	Difference in Cursor 
		print, : cursor remains in the same line
		println : cursor shifts to next line
		printf : used for formatting

Q:What are the different ways to create objects in Java?	
A:https://www.geeksforgeeks.org/java/different-ways-create-objects-java
	Using Class.forName().newInstance()
	Using clone() method
	Using Constructor.newInstance() from Reflection API
	Using Deserialization
	Using new instance
	Using new keyword
	Using the newInstance() method of the Constructor class