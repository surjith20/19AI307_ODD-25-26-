# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Write a Java program to demonstrate **Inheritance and Aggregation** by creating an order management system for Normal and Prime users. Calculate the final payable amount based on user type and display the order details.

---

## AIM:

To implement **Inheritance and Aggregation** concepts using Java classes and methods.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary packages `java.util` and `java.text.DecimalFormat`.
3. Create a parent class `Order` with data members:

* orderId
* customerName
* totalAmount
* deliveryCharge

4. Create a constructor in `Order` class to initialize values.
5. Create a method `calculateFinalAmount()` to calculate total payable amount.
6. Create a method `display()` to display order details.
7. Create a subclass `NormalUser` that extends `Order`.
8. Override the `calculateFinalAmount()` method for Normal users.
9. Create another subclass `PrimeUser` that extends `Order`.
10. Override the `calculateFinalAmount()` method for Prime users with 50% delivery charge discount.
11. In the `main()` method:

    * Read input from the user.
    * Create objects dynamically based on user type.
    * Display order details.
12. End the program.

---

## PROGRAM:

```java
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SURJITH D
Register Number:  212223043006
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName,
                 double totalAmount, double deliveryCharge) {

        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {

        DecimalFormat df = new DecimalFormat("0.00");

        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " +
                           df.format(calculateFinalAmount()));
    }
}

// Normal User Class
class NormalUser extends Order {

    public NormalUser(String orderId, String customerName,
                      double totalAmount,
                      double deliveryCharge) {

        super(orderId, customerName,
              totalAmount, deliveryCharge);
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }
}

// Prime User Class
class PrimeUser extends Order {

    public PrimeUser(String orderId, String customerName,
                     double totalAmount,
                     double deliveryCharge) {

        super(orderId, customerName,
              totalAmount, deliveryCharge);
    }

    double calculateFinalAmount() {

        return totalAmount + (deliveryCharge * 0.5);
    }
}

// Main Class
public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        while(sc.hasNext()) {

            String type = sc.next();
            String orderId = sc.next();
            String customerName = sc.next();

            double totalAmount = sc.nextDouble();
            double deliveryCharge = sc.nextDouble();

            Order o;

            if(type.equalsIgnoreCase("Normal")) {

                o = new NormalUser(orderId,
                                   customerName,
                                   totalAmount,
                                   deliveryCharge);

                o.display("Normal");
            }
            else {

                o = new PrimeUser(orderId,
                                  customerName,
                                  totalAmount,
                                  deliveryCharge);

                o.display("Prime");
            }
        }

        sc.close();
    }
}
```

---

## OUTPUT:


<img width="646" height="541" alt="image" src="https://github.com/user-attachments/assets/bb517c16-f880-4a5d-9801-1b93d7a54c50" />

---

## RESULT:

Thus, the Java program to demonstrate **Inheritance and Aggregation** was implemented successfully and the output was verified.
