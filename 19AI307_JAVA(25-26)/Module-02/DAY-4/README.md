# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a Java program to implement variable scope and constructor.

---

## AIM:

To create a Java program that demonstrates variable scope and the use of constructors.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `St` with instance variables `name` and `a`.
4. Define a constructor `St(String name, int a)` to initialize the instance variables using `this` keyword.
5. Create a method `det()` to display the student details and result status.
6. In the `main()` method, create a `Scanner` object to get input from the user.
7. Read the student name and marks.
8. Create an object of class `St` and pass the values to the constructor.
9. Call the `det()` method using the object.
10. Display the student details and pass/fail status.
11. Close the scanner.
12. Stop the program.

---

## PROGRAM:

```java id="vsc01"
/*
Program to implement a Variable scope and Constructor using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

## SOURCE CODE:

```java id="vsc02"
import java.util.*;

class St {

    String name;
    int a;

    public St(String name, int a) {
        this.name = name;
        this.a = a;
    }

    public void det() {

        System.out.println("Student Name: " + name);
        System.out.println("Marks Scored: " + a);

        if (a > 50) {
            System.out.println("Status: Pass");
        }
        else {
            System.out.println("Status: Fail");
        }
    }
}

class prog {

    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        String a = s.next();
        int b = s.nextInt();

        St st = new St(a, b);

        st.det();

        s.close();
    }
}
```

---

## OUTPUT:

<img width="255" height="147" alt="image" src="https://github.com/user-attachments/assets/30ace345-92e7-4bfd-b409-c10c81bc4ca8" />


---

## RESULT:

Thus, the Java program to implement variable scope and constructor was executed successfully.
