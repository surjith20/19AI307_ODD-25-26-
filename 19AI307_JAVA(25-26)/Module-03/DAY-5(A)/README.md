# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to demonstrate the use of an **Inner Class** by displaying a greeting message using a method inside the inner class.

---

## AIM:

To implement the concept of **Inner Class** in Java and access its methods using an outer class object.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an outer class named `Outer`.
4. Inside the outer class, create an inner class named `Inner`.
5. Create a method `disp()` inside the inner class to display a greeting message.
6. In the `main()` method:

* Read the user name using `Scanner`.
* Create an object for the outer class.
* Create an object for the inner class using the outer class object.
* Call the `disp()` method using the inner class object.

7. Display the greeting message.
8. End the program.

---

## PROGRAM:

```java id="rf9q1q"
/*
Program to implement a InnerClass using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="8ahvkr"
import java.util.*;

class Outer{

    class Inner{

        void disp(String name){

            System.out.println("Hello, " + name +
            "! This message is from the Inner Class.");
        }
    }
}

public class prog{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        String n = s.nextLine();

        Outer o = new Outer();

        Outer.Inner in = o.new Inner();

        in.disp(n);

        s.close();
    }
}
```

---

## OUTPUT:


<img width="545" height="108" alt="image" src="https://github.com/user-attachments/assets/8e8d80af-1946-4d8b-99ad-7d6e8a856655" />

---

## RESULT:

Thus, the Java program to demonstrate the concept of **Inner Class** was implemented successfully and the output was verified.
