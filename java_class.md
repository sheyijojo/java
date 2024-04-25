## Java class 

```java
public class Store {
  // instance fields, initialize the variables
  String productType;
  int inventoryCount;
  double inventoryPrice;
  
  // constructor method,
  public Store(String product, int count, double price) {
    productType = product;
    inventoryCount = count;
    inventoryPrice = price;
  }
  
  // main method
  public static void main(String[] args) {
    Store lemonadeStand = new Store("lemonade", 42, .99);
    Store cookieShop = new Store("cookies", 12, 3.75);
    
    System.out.println("Our first shop sells " + lemonadeStand.productType + " at " + lemonadeStand.inventoryPrice + " per unit.");
    
    System.out.println("Our second shop has " + cookieShop.inventoryCount + " units remaining.");
  }
}


```

## Sample 2

```java
public class Car {
// scope of Car class starts after curly brace

  public static void main(String[] args) {
    // scope of main() starts after curly brace

    // program tasks

  }
  // scope of main() ends after curly brace

}
// scope of Car class ends after curly brace

```
## Every class will have main method and to create an instance, you need a constructor. 

- Constructors are like normal methods within the class but are used to initialize the object of the class.

- In Java, every time the new keyword is used to create an object, at least one constructor is called.

`https://www.codecademy.com/resources/docs/java/constructors?page_ref=catalog`




```java
public class Store {
  // declare instance fields here!
   String ProductType;
  
  // constructor method
  public Store() {
    System.out.println("I am inside the constructor method.");
  }
  
  // main method
  public static void main(String[] args) {
    System.out.println("This code is inside the main method.");
    
    Store lemonadeStand = new Store();
    
    System.out.println(lemonadeStand);
  }
}

```

### Constructor Parameters
To create objects with dynamic, individual states, we’ll use a combination of the constructor method and instance fields.

```java
public class Car {
  String color;
  int mpg;
  boolean isElectric;

  // constructor 1
  public Car(String carColor, int milesPerGallon) {
    color = carColor;
    mpg = milesPerGallon;
  }
  // constructor 2
  public Car(boolean electricCar, int milesPerGallon) {
    isElectric = electricCar;
    mpg = milesPerGallon;
  }
}





```
