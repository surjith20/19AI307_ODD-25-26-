# Ex.No:3(B) POLYMORPHISM

## QUESTION:

Write a Java program to demonstrate **Polymorphism** using method overloading to find the maximum value among integers and double values.

---

## AIM:

To implement **Polymorphism** in Java using method overloading.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `MaxFinder`.
4. Create an overloaded method `max(int a, int b)` to find the maximum of two integers.
5. Create another overloaded method `max(double a, double b)` to find the maximum of two double values.
6. Create another overloaded method `max(int a, int b, int c)` to find the maximum of three integers.
7. Create the `main()` method inside the `Main` class.
8. Read integer and double inputs from the user using `Scanner`.
9. Create an object for the `MaxFinder` class.
10. Call the overloaded `max()` methods using different arguments.
11. Display the maximum values.
12. Close the scanner and end the program.

---

## PROGRAM:

```java
/*
Program to implement a Polymorphism using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class MaxFinder {

    int max(int a, int b) {

        if(a > b)
            return a;
        else
            return b;
    }

    double max(double a, double b) {

        if(a > b)
            return a;
        else
            return b;
    }

    int max(int a, int b, int c) {

        int largest = a;

        if(b > largest)
            largest = b;

        if(c > largest)
            largest = c;

        return largest;
    }
}

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        double x = sc.nextDouble();
        double y = sc.nextDouble();

        int p = sc.nextInt();
        int q = sc.nextInt();
        int r = sc.nextInt();

        MaxFinder m = new MaxFinder();

        System.out.println("Max(" + a + ", " + b + "): " +
                           m.max(a, b));

        System.out.println("Max(" + x + ", " + y + "): " +
                           m.max(x, y));

        System.out.println("Max(" + p + ", " + q + ", " + r + "): " +
                           m.max(p, q, r));

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="263" height="138" alt="image" src="https://github.com/user-attachments/assets/baa24dcf-abad-433c-845a-0d6d79af243d" />

---

## RESULT:

Thus, the Java program to demonstrate **Polymorphism** using method overloading was implemented successfully and the output was verified.
