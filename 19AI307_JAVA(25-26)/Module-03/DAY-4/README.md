# Ex.No:3(D) INTERFACE

## QUESTION:

Write a Java program to demonstrate the use of an **Interface** by implementing different gaming controller classes with common actions such as jump, shoot, and pause.

---

## AIM:

To implement **Interface** concepts in Java using multiple classes that provide different implementations for common methods.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an interface named `Gc`.
4. Declare abstract methods:

* `j()` for Jump
* `s()` for Shoot
* `p()` for Pause

5. Create a class `Pbc` that implements the `Gc` interface.
6. Provide method definitions for jump, shoot, and pause actions for PlayBox controller.
7. Create another class `Xcc` that implements the `Gc` interface.
8. Provide method definitions for X-Cube controller actions.
9. Create another class `Rcf` that implements the `Gc` interface.
10. Provide method definitions for RetroFun controller actions.
11. In the `main()` method:

    * Read controller type and action from the user.
    * Create the corresponding controller object using switch case.
    * Invoke the required method based on the action entered.
12. Display appropriate messages for unsupported controllers or unknown actions.
13. End the program.

---

## PROGRAM:

```java id="6z4fwb"
/*
Program to implement a Interface using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="8g5hmq"
import java.util.*;

interface Gc{

    void j();
    void s();
    void p();
}

class Pbc implements Gc{

    public void j(){
        System.out.println("PlayBox: Press X to Jump!");
    }

    public void s(){
        System.out.println("PlayBox: Press R2 to Shoot!");
    }

    public void p(){
        System.out.println("PlayBox: Press Start to Pause.");
    }
}

class Xcc implements Gc{

    public void j(){
        System.out.println("X-Cube: Press A to Jump!");
    }

    public void s(){
        System.out.println("X-Cube: Press RT to Shoot!");
    }

    public void p(){
        System.out.println("X-Cube: Press Menu to Pause.");
    }
}

class Rcf implements Gc{

    public void j(){
        System.out.println("RetroFun: Use Up Arrow to Jump!");
    }

    public void s(){
        System.out.println("RetroFun: Press B to Shoot!");
    }

    public void p(){
        System.out.println("RetroFun: Press P to Pause.");
    }
}

class prog{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        String ct = s.nextLine().toLowerCase();
        String a = s.nextLine().toLowerCase();

        Gc g = null;

        switch(ct){

            case "playbox":
                g = new Pbc();
                break;

            case "xcube":
                g = new Xcc();
                break;

            case "retro":
                g = new Rcf();
                break;

            default:
                System.out.println("Unsupported controller!");
                return;
        }

        switch(a){

            case "jump":
                g.j();
                break;

            case "shoot":
                g.s();
                break;

            case "pause":
                g.p();
                break;

            default:
                System.out.println("Unknown action!");
        }

        s.close();
    }
}
```

---

## OUTPUT:
<img width="322" height="108" alt="image" src="https://github.com/user-attachments/assets/e10545fa-4479-41b6-90f7-d04ab94c96cc" />


---

## RESULT:

Thus, the Java program to demonstrate **Interface** concepts using multiple implementing classes was implemented successfully and the output was verified.
