# Ex.No:3(C) ABSTRACTION

## QUESTION:

Write a Java program to demonstrate **Abstraction** using an abstract class and subclasses to process maze data and generate outputs based on different conditions.

---

## AIM:

To implement **Abstraction** in Java using abstract classes and method overriding.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an abstract class `MA`.
4. Declare an abstract method `GNC(String[] m)` inside the abstract class.
5. Create a subclass `Sc` that extends `MA`.
6. Override the `GNC()` method to identify the positions of `'@'` symbols in the maze and generate a code.
7. Create another subclass `HA` that extends `MA`.
8. Override the `GNC()` method to count the number of `'#'` symbols in the maze.
9. If the count is greater than or equal to 10, return `"TRAPPED"`; otherwise return `"ESCAPE"`.
10. In the `main()` method:

    * Read the maze size and maze data from the user.
    * Read the type value.
    * Create the appropriate subclass object dynamically using abstraction.
    * Call the `GNC()` method and display the result.
11. Close the scanner.
12. End the program.

---

## PROGRAM:

```java id="yb3b3k"
/*
Program to implement a Abstraction using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="7o4wl9"
import java.util.*;

abstract class MA{
    abstract String GNC(String[] m);
}

class Sc extends MA{

    String GNC(String[] m){

        StringBuilder code = new StringBuilder();

        for(int i = 0; i < m.length; i++){

            for(int j = 0; j < m[i].length(); j++){

                if(m[i].charAt(j) == '@')
                    code.append(i + 1);
            }
        }

        return code.toString();
    }
}

class HA extends MA{

    String GNC(String[] m){

        int c = 0;

        for(String row : m)

            for(char d : row.toCharArray())

                if(d == '#')
                    c++;

        return c >= 10 ? "TRAPPED" : "ESCAPE";
    }
}

public class Main{

    public static void main(String[] ar){

        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());

        String[] maze = new String[n];

        for(int i = 0; i < n; i++)
            maze[i] = sc.nextLine();

        int type = Integer.parseInt(sc.nextLine());

        MA a = (type == 1) ? new Sc() : new HA();

        System.out.println(a.GNC(maze));

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="152" height="357" alt="image" src="https://github.com/user-attachments/assets/2552fa64-eaef-4331-9917-cf2129ebb219" />


---

## RESULT:

Thus, the Java program to demonstrate **Abstraction** using abstract classes and method overriding was implemented successfully and the output was verified.
