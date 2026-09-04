class Animal {
    void sound() {
        System.out.println("Animal");
    }
					
} 
class Dog extends Animal {
    
}
 

Animal a = new Dog();
a.sound();


Inheritance+Polymorpihs : Runtime Dispatch


Dog d1 = new Animal()