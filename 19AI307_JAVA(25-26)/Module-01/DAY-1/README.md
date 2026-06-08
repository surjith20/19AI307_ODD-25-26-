# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Write a Java program to implement variables and operators using different data types and display user details using input from the keyboard.

---

# AIM:

To study and implement Java programming concepts involving data types, variables, input handling, and operators using the Scanner class.

---

# ALGORITHM :

1. Import the required Java utility package.
2. Create a class containing the main method.
3. Use the Scanner class to accept user inputs.
4. Store the inputs in variables of different data types.
5. Display the entered values using output statements.

---

# PROGRAM:

```java
/*
Program to implement variables and Operators using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

# Sourcecode.java:

```java
import java.util.*;

class prog {
    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        String a = s.next();
        int b = s.nextInt();
        float c = s.nextFloat();

        System.out.println("Hello, " + a);
        System.out.println("You are " + b + " years old");
        System.out.printf("Your favorite number is %.2f", c);

        s.close();
    }
}
```

---

# OUTPUT:

<img width="352" height="143" alt="image" src="https://github.com/user-attachments/assets/96b32bbc-fd67-4423-8a24-ebc494ee5fcb" />


# RESULT:

Thus the Java program to implement variables, data types, and operators using user input was executed successfully and the output was verified.
