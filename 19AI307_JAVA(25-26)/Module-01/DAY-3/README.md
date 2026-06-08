# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program to reverse a number using looping statements.

---

# AIM:

To study and implement looping statements in Java using the `while` loop.

---

# ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class containing the `main()` method.
4. Create a Scanner object to accept input from the user.
5. Read an integer value from the user.
6. Initialize a variable `rev` to store the reversed number.
7. Use a `while` loop until the number becomes 0.
8. Extract the last digit using modulus operator `%`.
9. Add the digit to the reversed number.
10. Remove the last digit from the original number.
11. Display the reversed number.
12. Stop the program.

---

# PROGRAM:

```java id="y8p2fv"
/*
Program to implement a Looping Statement using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

# SOURCE CODE:

```java id="r4m9tz"
import java.util.*;

class prog {
    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        int a = s.nextInt();
        int rev = 0;

        while(a != 0) {
            int b = a % 10;
            rev = rev * 10 + b;
            a /= 10;
        }

        System.out.println("Reversed number: " + rev);

        s.close();
    }
}
```

---

# OUTPUT:

<img width="256" height="82" alt="image" src="https://github.com/user-attachments/assets/94487f03-c866-41a5-91ac-cb1369add781" />


# RESULT:

Thus the Java program to implement looping statements using the `while` loop was executed successfully and the output was verified.
