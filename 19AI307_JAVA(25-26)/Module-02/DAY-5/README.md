# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Write a Java program to implement access modifiers.

---

## AIM:

To create a Java program that demonstrates the use of access modifiers in Java.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Student`.
4. Declare private data members `name` and `mark`.
5. Create public setter methods to assign values to the variables.
6. Create public getter methods to access the variable values.
7. Create a method to display the student details.
8. Create the main class `prog`.
9. In the `main()` method, create a `Scanner` object to get input.
10. Read the student name and mark from the user.
11. Create an object for the `Student` class.
12. Set the values using setter methods.
13. Display the details using getter methods.
14. Close the scanner.
15. Stop the program.

---

## PROGRAM:

```java id="am01"
/*
Program to implement a Access Modifiers using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

## SOURCE CODE:

```java id="am02"
import java.util.*;

class Student {

    private String name;
    private int mark;

    public void setName(String name) {
        this.name = name;
    }

    public void setMark(int mark) {
        this.mark = mark;
    }

    public String getName() {
        return name;
    }

    public int getMark() {
        return mark;
    }
}

class prog {

    public static void main(String[] args) {

        Scanner s = new Scanner(System.in);

        String name = s.next();
        int mark = s.nextInt();

        Student st = new Student();

        st.setName(name);
        st.setMark(mark);

        System.out.println("Student Name: " + st.getName());
        System.out.println("Student Mark: " + st.getMark());

        s.close();
    }
}
```

---

## OUTPUT:

<img width="270" height="121" alt="image" src="https://github.com/user-attachments/assets/19b8c7ef-c859-4160-9e70-bfbcd29ae9a8" />


---

## RESULT:

Thus, the Java program to implement access modifiers was executed successfully.
