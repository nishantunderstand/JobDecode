Constructor()
Constructor1(a,b)
Constructor2(a,b,c)
Constructor3(a,b,c,d)
Constructor4(a,b,c,d,e)

public class Constructor{
	int a = 10;
	int b = 20;
	
	public Constructor(){
		this.a = a;
		this.b = b;
		Constructor1(a,b);
	}
	
	public Constructor(){
		Constructor1(a,b);
	}
	
	
}