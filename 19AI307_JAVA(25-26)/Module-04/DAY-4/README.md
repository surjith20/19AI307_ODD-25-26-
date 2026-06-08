# Ex.No:4(D) DESIGN PATTERN – ABSTRACT FACTORY

## QUESTION:

Write a Java program to demonstrate a **Design Pattern** using a music player application that changes behavior based on different player states such as Play, Pause, and Stop.

---

## AIM:

To implement a **Design Pattern** in Java using interfaces, classes, and state-based behavior management.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an interface named `PlayerState`.
4. Declare abstract methods:

* `play()`
* `pause()`
* `stop()`

5. Create a class `StoppedState` implementing `PlayerState`.
6. Implement behavior for:

* Play operation to change state to PlayingState.
* Ignore pause and stop operations.

7. Create a class `PlayingState` implementing `PlayerState`.
8. Implement behavior for:

* Pause operation to change state to PausedState.
* Stop operation to change state to StoppedState.

9. Create a class `PausedState` implementing `PlayerState`.
10. Implement behavior for:

    * Play operation to resume music.
    * Stop operation to stop music.
11. Create a context class `MusicPlayer`:

    * Store the current player state.
    * Provide methods `play()`, `pause()`, and `stop()`.
12. In the `main()` method:

    * Create a `MusicPlayer` object.
    * Read commands from the user continuously.
    * Execute actions based on the entered command.
    * Exit the program when `"exit"` is entered.
13. End the program.

---

## PROGRAM:

```java id="w4z8pk"
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java id="x6p9tr"
import java.util.Scanner;

interface PlayerState {

    void play(MusicPlayer player);

    void pause(MusicPlayer player);

    void stop(MusicPlayer player);
}

// Stopped State
class StoppedState implements PlayerState {

    public void play(MusicPlayer player) {

        player.setState(new PlayingState());

        System.out.println("Music Playing");
    }

    public void pause(MusicPlayer player) {
        // No output
    }

    public void stop(MusicPlayer player) {
        // No output
    }
}

// Playing State
class PlayingState implements PlayerState {

    public void play(MusicPlayer player) {
        // No output
    }

    public void pause(MusicPlayer player) {

        player.setState(new PausedState());

        System.out.println("Music Paused");
    }

    public void stop(MusicPlayer player) {

        player.setState(new StoppedState());

        System.out.println("Music Stopped");
    }
}

// Paused State
class PausedState implements PlayerState {

    public void play(MusicPlayer player) {

        player.setState(new PlayingState());

        System.out.println("Music Playing");
    }

    public void pause(MusicPlayer player) {
        // No output
    }

    public void stop(MusicPlayer player) {

        player.setState(new StoppedState());

        System.out.println("Music Stopped");
    }
}

// Context Class
class MusicPlayer {

    private PlayerState state;

    public MusicPlayer() {

        state = new StoppedState();
    }

    public void setState(PlayerState state) {

        this.state = state;
    }

    public void play() {

        state.play(this);
    }

    public void pause() {

        state.pause(this);
    }

    public void stop() {

        state.stop(this);
    }
}

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        MusicPlayer player = new MusicPlayer();

        while (true) {

            String command = sc.nextLine();

            if (command.equalsIgnoreCase("exit")) {
                break;
            }

            if (command.equalsIgnoreCase("play")) {

                player.play();

            } else if (command.equalsIgnoreCase("pause")) {

                player.pause();

            } else if (command.equalsIgnoreCase("stop")) {

                player.stop();
            }
        }

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="205" height="190" alt="image" src="https://github.com/user-attachments/assets/c3a24b51-3dfc-4d9c-988a-cead9108bcb8" />


---

## RESULT:

Thus, the Java program to demonstrate the **Design Pattern** using state-based behavior management was implemented successfully and the output was verified.
