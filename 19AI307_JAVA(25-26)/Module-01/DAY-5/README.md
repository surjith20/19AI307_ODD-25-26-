# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to reverse a string using String functions.

---

# AIM:

To study and implement String handling and built-in functions in Java.

---

# ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class containing the `main()` method.
4. Create a Scanner object to accept input from the user.
5. Read a string from the user.
6. Use `StringBuilder` to reverse the string.
7. Convert the reversed object back to string format.
8. Display the reversed string.
9. Stop the program.

---

# PROGRAM:

```java id="d3n8qx"
/*
Program to implement a Strings and Math Function using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

# SOURCE CODE:

```java id="x7p1vr"
import java.util.*;

class prog {
    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        String a = s.next();

        String rev = new StringBuilder(a).reverse().toString();

        System.out.println("Reversed string: " + rev);

        s.close();
    }
}
```

---

# OUTPUT:


<img width="367" height="207" alt="image" src="https://github.com/user-attachments/assets/6b90e564-600c-47fb-a32d-9aff81350873" />


# RESULT:

Thus the Java program to implement String handling functions and reverse a string was executed successfully and the output was verified.
