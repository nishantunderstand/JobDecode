String a = "abc";
String b = "ab";
final b = b + "c"; 

System.out.println(a == b); // Reference  => FALSE 

SCP 
abc // 1
ab // 2
c // 3

Heap 
abc


System.out.println(a.equals(b));   // Value  => TRUE 
