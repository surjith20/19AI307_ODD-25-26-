# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## QUESTION:

Write a Java program to demonstrate the implementation of **SOLID Principles** using a Radar Control Tower system that manages flight registrations.

---

## AIM:

To implement **SOLID Principles** in Java using classes, object-oriented design, and the Singleton design pattern.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `RadarControlTower`.
4. Declare:

* A static object `instance` for Singleton implementation.
* A list to store flight names.

5. Create a private constructor to restrict object creation from outside the class.
6. Create a static method `getInstance()`:

* If the instance is null, create a new object.
* Return the same object every time.

7. Create a method `registerFlight()`:

* Add the flight name to the list.
* Return the total number of flights registered.

8. Create the `main()` method inside class `prog`.
9. Read the number of flights from the user.
10. Use a loop to:

    * Read each flight name.
    * Access the Singleton object using `getInstance()`.
    * Register the flight.
    * Display the registration details and total flights.
11. End the program.

---

## PROGRAM:

```java id="k5v8qx"
/*
Program to implement a SOLID Principles in Java Program
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="x2q7nv"
import java.util.*;

class RadarControlTower {

   private static RadarControlTower instance = null;

   private List<String> flights;

   private RadarControlTower(){

       flights = new ArrayList<>();
   }

   public static RadarControlTower getInstance(){

       if(instance == null){

           instance = new RadarControlTower();
       }

       return instance;
   }

   public int registerFlight(String flightName){

      flights.add(flightName);

      return flights.size();
   }
}

public class prog {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        sc.nextLine();

        for (int i = 0; i < n; i++) {

            String flight = sc.nextLine();

            RadarControlTower tower =
                    RadarControlTower.getInstance();

            int total = tower.registerFlight(flight);

            System.out.println(flight +
            " registered with Radar Control Tower. Total Flights: "
            + total);
        }

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="622" height="167" alt="image" src="https://github.com/user-attachments/assets/ba901252-cfbd-49ec-a881-a3bdcaa03c2d" />


---

## RESULT:

Thus, the Java program to implement **SOLID Principles** using the Singleton design pattern was implemented successfully and the output was verified.
