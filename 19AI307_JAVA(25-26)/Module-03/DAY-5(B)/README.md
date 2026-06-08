# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to demonstrate the use of a **Wrapper Class** by checking whether a given number is a palindrome or not.

---

## AIM:

To implement the concept of **Wrapper Class** in Java using string conversion and palindrome checking.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `prog`.
4. In the `main()` method:

* Read an integer input from the user using `Scanner`.
* Convert the integer into a string using the wrapper class method `String.valueOf()`.
* Reverse the string using `StringBuilder`.
* Compare the original string with the reversed string.

5. If both strings are equal:

* Display that the number is a palindrome.

6. Otherwise:

* Display that the number is not a palindrome.
* Display the reversed number.

7. Close the scanner.
8. End the program.

---

## PROGRAM:

```java id="j7n2mr"
/*
Program to implement a Wrapper Class using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="d3gk2s"
import java.util.*;

class prog{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        int a = s.nextInt();

        String b = String.valueOf(a);

        String rev = new StringBuilder(b).reverse().toString();

        if(b.equals(rev)){

            System.out.println(b + " is a palindrome number.");

        }else{

            System.out.println(b + " is not a palindrome number.");
            System.out.println("Reversed Number: " + rev);
        }

        s.close();
    }
}
```

---

## OUTPUT:

<img width="471" height="178" alt="image" src="https://github.com/user-attachments/assets/cfbc4dc7-3d24-496f-bdc9-984e710b1c13" />

---

## RESULT:

Thus, the Java program to demonstrate the concept of **Wrapper Class** was implemented successfully and the output was verified.
