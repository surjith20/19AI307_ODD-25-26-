# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Write a Java program to implement Class and Object concepts.

---

## AIM:

To create a class and object in Java and access class members using an object.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Teacher` with data members `name`, `subject`, and `experience`.
4. Define a method `printMessage()` inside the class to display teacher details.
5. Create the main class `prog`.
6. Inside the `main()` method, create an object for the `Teacher` class.
7. Read the teacher details using `Scanner`.
8. Assign the values to the object members.
9. Call the `printMessage()` method using the object.
10. Display the output.
11. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement a Class and Objects using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

## SOURCE CODE:

```java
import java.util.Scanner;

class Teacher {
    String name;
    String subject;
    int experience;

    void printMessage() {
        System.out.println("Mr. " + name + " teaches " + subject +
                           " and has " + experience + " years experience.");
    }
}

class prog {
    public static void main(String[] args) {

        Scanner s = new Scanner(System.in);

        Teacher t = new Teacher();

        t.name = s.next();
        t.subject = s.next();
        t.experience = s.nextInt();

        t.printMessage();

        s.close();
    }
}
```

---

## OUTPUT:


<img width="656" height="143" alt="image" src="https://github.com/user-attachments/assets/388b559a-5a27-455a-b79a-866cadf67e3a" />


---

## RESULT:

Thus, the Java program to implement Class and Object concepts was executed successfully.
