class Test {
    static int x = 10;
    Test() {
        x++;
    }
}
Test t1 = new Test();  //  11
Test t2 = new Test();   // 12
System.out.println(Test.x); // 12

O/P : 12