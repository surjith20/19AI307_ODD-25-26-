# Ex.No:2(B) METHODS

## QUESTION:

Write a Java program to implement methods.

---

## AIM:

To create and use methods in Java for checking whether a number is even or odd.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `prog`.
4. Define a static method `isEven(int num)` to check whether the number is even.
5. In the `main()` method, create a `Scanner` object to get input from the user.
6. Read an integer value.
7. Call the `isEven()` method by passing the input number.
8. If the method returns `true`, display `"true"`.
9. Otherwise, display `"false"`.
10. Close the scanner.
11. Stop the program.

---

## PROGRAM:

```java id="mtds01"
/*
Program to implement a Methods using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

## SOURCE CODE:

```java id="mtds02"
import java.util.*;

class prog {

    public static boolean isEven(int num) {
        return (num & 1) == 0;
    }

    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        int a = s.nextInt();

        boolean p = isEven(a);

        if (p) {
            System.out.println("true");
        }
        else {
            System.out.println("false");
        }

        s.close();
    }
}
```

---

## OUTPUT:

<img width="141" height="90" alt="image" src="https://github.com/user-attachments/assets/b2772cb6-ad44-44d2-b783-b5a3f8053dcd" />


---

## RESULT:

Thus, the Java program to implement methods was executed successfully.
