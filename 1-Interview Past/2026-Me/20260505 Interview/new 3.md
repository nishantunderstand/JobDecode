try {
    int x = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Exception");
} finally {
    System.out.println("Finally");
}

O/P
Exception
Finally