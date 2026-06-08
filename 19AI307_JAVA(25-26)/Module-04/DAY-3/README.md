# Ex.No:4(C) COMPOSITION IN JAVA

## QUESTION:

Write a Java program to demonstrate the concept of **Composition** by creating a `Car` object that contains an `Engine` object.

---

## AIM:

To implement the concept of **Composition** in Java using one class object inside another class.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Engine`.
4. Create a method `startEngine()` inside the `Engine` class.
5. Create another class named `Car`.
6. Create an object of the `Engine` class inside the `Car` class to demonstrate composition.
7. Create a method `startCar()` inside the `Car` class.
8. Inside `startCar()`, call the `startEngine()` method using the `Engine` object.
9. Create the `main()` method inside class `prog`.
10. Create an object for the `Car` class.
11. Call the `startCar()` method.
12. Display the output.
13. End the program.

---

## PROGRAM:

```java id="f7m2kp"
/*
Program to implement a Composition Concepts in Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="v8q4tz"
import java.util.*;

class Engine {

    void startEngine() {

        System.out.println("Engine Started");
    }
}

class Car {

    private Engine engine;

    Car() {

        engine = new Engine();
    }

    void startCar() {

        System.out.println("Car Starting...");
        engine.startEngine();
    }
}

public class prog {

    public static void main(String[] args) {

        Car c = new Car();

        c.startCar();
    }
}
```

---

## OUTPUT:

```text id="u4x9mn"
Output:
Car Starting...
Engine Started
```

---

## RESULT:

Thus, the Java program to demonstrate the concept of **Composition** was implemented successfully and the output was verified.
