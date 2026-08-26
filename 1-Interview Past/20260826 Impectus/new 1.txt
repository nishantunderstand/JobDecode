class Counter {
    int count = 0;
 
    void increment() {
        count++;
    }
}

int counter = 0;


public class A extends thread{
	private int cnt = 0;
	@Override
	public void run(){
	
	for(int i=0;i<1000;i++){
		cnt++;
	}	
	}
	
}

public class Main{
	public static void main(String[] args){
		A a1 = new A();
		A a2 = new A();
		a1.start(); 
		a2.start();		
	}
}