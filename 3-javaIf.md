## Conditionals and Control Flow
- The if-then statement is the most simple control flow we can write. It tests an expression for truth and executes some code based on it.
```java


if (flip == 1) {

  System.out.println("Heads!");

}

```

- The if keyword marks the beginning of the conditional statement, followed by parentheses ().
The parentheses hold a boolean datatype.


```java
public class Order {
  
  public static void main(String[] args) {
    
    double itemCost = 30.99;
    
    // Write an if-then statement:
    if (itemCost > 24.00){
      System.out.println("High value item!");

    }
    
  }
  
}
```

## if-then-else statement:

```java
if (hasPrerequisite) {

  // Enroll in course

} else {

  // Enroll in prerequisite

}


//example2

public class Order {
  
  public static void main(String[] args) {
    
    boolean isFilled = false;
    
    // Write an if-then-else statement:
    if (isFilled == true){
      System.out.println("Shipping");
    }else {
      System.out.println("Order not ready");
    }
    
  }
  
}
```


## If-Then-Else-If

```java
String course = "Theatre";

if (course.equals("Biology")) {

  // Enroll in Biology course

} else if (course.equals("Algebra")) {

  // Enroll in Algebra course

} else if (course.equals("Theatre")) {

  // Enroll in Theatre course

} else {

  System.out.println("Course not found!");

}

```
## Conditional full example 

```java
public class Order {
  boolean isFilled;
  double billAmount;
  String shipping;
  
  public Order(boolean filled, double cost, String shippingMethod) {
		if (cost > 24.00) {
      System.out.println("High value item!");
    }
    isFilled = filled;
    billAmount = cost;
    shipping = shippingMethod;
  }
  
  public void ship() {
    if (isFilled) {
      System.out.println("Shipping");
      System.out.println("Shipping cost: " + calculateShipping());
    } else {
      System.out.println("Order not ready");
    }
  }
  
  public double calculateShipping() {
	 	// declare conditional statement here

    if (shipping.equals("Regular")){
      return 0;

    }else if(shipping.equals("Express")){
      return 1.75;

    }else{
      return 0.50;
    }

    
 	}
  
  public static void main(String[] args) {
    // do not alter the main method!
    Order book = new Order(true, 9.99, "Express");
    Order chemistrySet = new Order(false, 72.50, "Regular");
    
    book.ship();
    chemistrySet.ship();
  }
}

```

## Nested Conditional Statements
- We can create more complex conditional structures by creating nested conditional statements, which is created by placing conditional statements inside other conditional statements:

- When we implement nested conditional statements, the outer statement is evaluated first. If the outer condition is true, then the inner, nested statement is evaluated.

```java
if (outer condition) {
  if (nested condition) {
    Instruction to execute if both conditions are true
  }
}

```

```java
int temp = 45;
boolean raining = true;

if (temp < 60) {
  System.out.println("Wear a jacket!");
  if (raining == true) {
    System.out.println("Bring your umbrella.");
  } else {
    System.out.println("Leave your umbrella home.");
  }
}


/*
In the code snippet above, our compiler will check the condition in the first if-then statement: temp < 60. Since temp has a value of 45, this condition is true; therefore, our program will print Wear a jacket!.

Then, we’ll evaluate the condition of the nested if-then statement: raining == true. This condition is also true, so Bring your umbrella is also printed to the screen.

Note that, if the first condition was false, the nested condition would not be evaluated.

*/

```


## Example of nested conditional

```java
public class Order {
  boolean isFilled;
  double billAmount;
  String shipping;
  String couponCode;
  
  public Order(boolean filled, double cost, String shippingMethod, String coupon) {
		if (cost > 24.00) {
      System.out.println("High value item!");
    }
    isFilled = filled;
    billAmount = cost;
    shipping = shippingMethod;
    couponCode = coupon;
  }
  
  public void ship() {
    if (isFilled) {
      System.out.println("Shipping");
      System.out.println("Shipping cost: " + calculateShipping());
    } else {
      System.out.println("Order not ready");
    }
  }
  
  public double calculateShipping() {
    if (shipping.equals("Regular")) {
      return 0;
    } else if (shipping.equals("Express")) {
      // Add your code here
      if (couponCode.equals("ship50")){
        return .85;
      }else{
        return 1.75;
      }

      
    } else {
      return .50;
    }
 	}
  
  public static void main(String[] args) {
    // do not alter the main method!
    Order book = new Order(true, 9.99, "Express", "ship50");
    Order chemistrySet = new Order(false, 72.50, "Regular", "freeShipping");
    
    book.ship();
    chemistrySet.ship();
  }
}

```

## Switch Statement
```md
An alternative to chaining if-then-else conditions together is to use the switch statement. This conditional will check a given value against any number of conditions and run the code block where there is a match.

Here’s an example of our course selection conditional as a switch statement instead:

```


```java
String course = "History";

switch (course) {
  case "Algebra": 
    // Enroll in Algebra
    break; 
  case "Biology": 
    // Enroll in Biology
    break;
  case "History": 
    // Enroll in History
    break;
  case "Theatre":
    // Enroll in Theatre
    break;
  default:
    System.out.println("Course not found");
}


```


```java

public class Order {
  boolean isFilled;
  double billAmount;
  String shipping;
  
  public Order(boolean filled, double cost, String shippingMethod) {
		if (cost > 24.00) {
      System.out.println("High value item!");
    }
    isFilled = filled;
    billAmount = cost;
    shipping = shippingMethod;
  }
  
  public void ship() {
    if (isFilled) {
      System.out.println("Shipping");
      System.out.println("Shipping cost: " + calculateShipping());
    } else {
      System.out.println("Order not ready");
    }
  }
  
  public double calculateShipping() {
    double shippingCost;
	 	// declare switch statement here
    switch (shipping){
      case "Regular":
        shippingCost = 0;
        break;
      case "Express":
        shippingCost= 1.75;
        break;
      default:
         shippingCost = 0.50;

    }
    
    return shippingCost;
 	}
  
  public static void main(String[] args) {
    // do not alter the main method!
    Order book = new Order(true, 9.99, "Express");
    Order chemistrySet = new Order(false, 72.50, "Regular");
    
    book.ship();
    chemistrySet.ship();
  }
}


```