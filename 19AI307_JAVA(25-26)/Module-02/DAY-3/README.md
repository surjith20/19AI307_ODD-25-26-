# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to implement access specifiers.

---

## AIM:

To create a Java program using access specifiers with private data members and public getter and setter methods.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `prog`.
4. Declare private data members `length` and `width`.
5. Create public getter and setter methods for both variables.
6. Define a method `calculateArea()` to calculate the area of a rectangle.
7. In the `main()` method, create a `Scanner` object to get input values.
8. Read the length and width values from the user.
9. Create an object for the class `prog`.
10. Set the values using setter methods.
11. Access and display the values using getter methods.
12. Close the scanner.
13. Stop the program.

---

## PROGRAM:

```java id="acs01"
/*
Program to implement a Access Specifiers using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

## SOURCE CODE:

```java id="acs02"
import java.util.Scanner;

class prog {

    private double length;
    private double width;

    public double getLength() {
        return length;
    }

    public void setLength(double length) {
        this.length = length;
    }

    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    public double calculateArea() {
        return length * width;
    }

    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        double a = s.nextDouble();
        double b = s.nextDouble();

        prog p = new prog();

        p.setLength(a);
        p.setWidth(b);

        System.out.println("Length: " + p.getLength());
        System.out.println("Width: " + p.getWidth());

        s.close();
    }
}
```

---

## OUTPUT:

<img width="505" height="313" alt="image" src="https://github.com/user-attachments/assets/da8f0b2f-12f7-42c8-90f2-5c69c3d687e7" />


## RESULT:

Thus, the Java program to implement access specifiers was executed successfully.
