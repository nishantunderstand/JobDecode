public static int test() {
    try {
        return 1;
    } finally {
        return 2;
    }
}
 
System.out.println(test());
O/P : 2