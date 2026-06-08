# Ex.No:4(D) DESIGN PATTERN – BEHAVIOUR PATTERN

## QUESTION:

Write a Java program to demonstrate a **Behaviour Pattern** by storing and retrieving different versions of an article.

---

## AIM:

To implement a **Behaviour Pattern** in Java for managing article versions using objects and collections.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Article`.
4. Declare a string variable `text` inside the class.
5. Create a method `set()` to store article content.
6. Create a method `get()` to return article content.
7. Create the `main()` method inside class `AM`.
8. Create:

* An `Article` object.
* An `ArrayList` to store versions of the article.

9. Read the number of versions from the user.
10. Use a loop to:

    * Read article content.
    * Store the content using the `set()` method.
    * Add the content to the version list.
11. Read the version number to retrieve.
12. If the version number is:

    * `0` → display the first version.
    * Between `1` and total versions → display the latest version.
    * Otherwise → display `"Invalid version"`.
13. End the program.

---

## PROGRAM:

```java id="q7n5bx"
/*
Program to implement a Behaviour Pattern using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="d4k8rv"
import java.util.*;

class Article{

    String text;

    void set(String t){

        text = t;
    }

    String get(){

        return text;
    }
}

public class AM{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        Article a = new Article();

        ArrayList<String> v = new ArrayList<>();

        int n = s.nextInt();

        s.nextLine();

        for(int i = 0; i < n; i++){

            a.set(s.nextLine());

            v.add(a.get());
        }

        int x = s.nextInt();

        if(x == 0)

            System.out.println(v.get(0));

        else if(x >= 1 && x <= v.size())

            System.out.println(v.get(v.size() - 1));

        else

            System.out.println("Invalid version");

        s.close();
    }
}
```

---

## OUTPUT:

<img width="420" height="195" alt="image" src="https://github.com/user-attachments/assets/59f8fcc5-7733-4812-bd39-e44e8866c3f1" />


---

## RESULT:

Thus, the Java program to demonstrate the **Behaviour Pattern** for managing article versions was implemented successfully and the output was verified.
