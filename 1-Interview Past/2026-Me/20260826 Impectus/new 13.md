class Counter {

    int count = 0;
 
    void increment() {

        count++;

    }

}
 
String str = "NIshant";
str = "Purvi";
 
class Animal {

    void sound() {

        System.out.println("Animal");

    }

}
 
class Dog extends Animal {

    void sound() {

        System.out.println("Dog");

    }

}
 
Animal a = new Dog();

a.sound();
 
Problem: Given a string, find the length of the longest substring that contains no repeated characters.
 
Input: "abcabcbb"

Output: 3
 
Input: "bbbbb"

Output: 1
 
 
Input: "pwwkew"

Output: 3
 
 
final test case : "dvdf", 3
 
Find Employee who are managers as well

EmpId, EmpName, ManagerId, Salary
101, Purvi, 100, x
102, Nishant, 101, y
 