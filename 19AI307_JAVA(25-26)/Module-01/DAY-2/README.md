# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

Write a Java program to implement conditional statements using if-else conditions.

---

# AIM:

To study and implement conditional statements in Java using if, else if, and else constructs.

---

# ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class containing the `main()` method.
4. Create a Scanner object to receive input from the user.
5. Read an integer value from the user.
6. Check the conditions using `if`, `else if`, and `else` statements.
7. Display the corresponding output based on the condition satisfied.
8. Stop the program.

---

# PROGRAM:

```java id="7t2qna"
/*
Program to implement a conditional statement using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

# SOURCE CODE:

```java id="f7o4ke"
import java.util.*;

class prog {
    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        int a = s.nextInt();

        if(a >= 2 && a <= 6) {
            System.out.println("Lights flicker");
        }
        else if(a % 2 == 1 && a >= 7 && a <= 11) {
            System.out.println("Lights off");
        }
        else if(a == 12) {
            System.out.println("Lights red");
        }
        else {
            System.out.println("Dark house");
        }

        s.close();
    }
}
```

---

# OUTPUT:

<img width="205" height="83" alt="image" src="https://github.com/user-attachments/assets/74196e6f-4db2-49d0-9de6-b4f190ab68f6" />


# RESULT:

Thus the Java program to implement conditional statements using if-else conditions was executed successfully and the output was verified.
