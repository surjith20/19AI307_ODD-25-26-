# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to find the average of elements in an array.

---

# AIM:

To study and implement array concepts in Java and calculate the average of array elements.

---

# ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class containing the `main()` method.
4. Create a Scanner object to receive input from the user.
5. Read the size of the array.
6. Declare an integer array with the given size.
7. Use a `for` loop to store elements into the array.
8. Use another `for` loop to calculate the sum of array elements.
9. Calculate the average using the formula:
   `Average = Sum / Number of Elements`
10. Display the average value.
11. Stop the program.

---

# PROGRAM:

```java id="q9k2mx"
/*
Program to implement a Array concept using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

---

# SOURCE CODE:

```java id="n8w5ra"
import java.util.*;

class prog {
    public static void main(String[] ar) {

        Scanner s = new Scanner(System.in);

        int b = s.nextInt();

        int[] a = new int[b];

        for(int i = 0; i < b; i++) {
            a[i] = s.nextInt();
        }

        float c = 0;
        float avg = 0;

        for(int i = 0; i < b; i++) {
            c += a[i];
        }

        avg = c / b;

        System.out.printf("The average of elements is %.2f", avg);

        s.close();
    }
}
```

---

# OUTPUT:

<img width="367" height="207" alt="image" src="https://github.com/user-attachments/assets/5f778ea5-fe62-4649-8c48-0f5816abba67" />

# RESULT:

Thus the Java program to implement arrays and calculate the average of elements was executed successfully and the output was verified.
