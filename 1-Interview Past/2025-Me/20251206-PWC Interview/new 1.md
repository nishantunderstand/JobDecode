0 1 1 2

int a = 0;
int b = 1;

fib(a,b);


// Base Case
if(a==0 && b==1) return;  //<--
int c = a+b;
System.out.println(c);
return fib(b,c);