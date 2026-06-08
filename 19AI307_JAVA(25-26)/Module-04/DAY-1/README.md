# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a Java program to demonstrate **Exception Handling** by checking for null values and safely handling user input.

---

## AIM:

To implement **Exception Handling** in Java for handling null values and preventing runtime errors.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Main`.
4. In the `main()` method:

* Create a `Scanner` object to read input from the user.
* Create a string array of size 1.

5. Check whether input is available using `hasNextLine()`.
6. If input is available:

* Store the input in the array element.

7. Check whether the array element is:

* `null`
* or equal to the string `"null"`

8. If true:

* Display `"Null element"`.

9. Otherwise:

* Convert the string to uppercase using `toUpperCase()`.
* Display the uppercase string.

10. Close the scanner.
11. End the program.

---

## PROGRAM:

```java id="8t7x2v"
/*
Program to implement a Exception Handling using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="n6v2wd"
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String[] arr = new String[1];

        // Read input safely
        if (sc.hasNextLine()) {

            arr[0] = sc.nextLine();
        }

        // Check for null or "null"
        if (arr[0] == null || arr[0].equals("null")) {

            System.out.println("Null element");

        } else {

            System.out.println(arr[0].toUpperCase());
        }

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="472" height="177" alt="image" src="https://github.com/user-attachments/assets/61c37b06-68c6-4bf8-95af-e6d9b57bbbee" />


---

## RESULT:

Thus, the Java program to demonstrate **Exception Handling** by handling null values safely was implemented successfully and the output was verified.
