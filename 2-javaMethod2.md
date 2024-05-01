## Calling methods

```
When we add a non-static method to a class, it becomes available to use on an object of that class. In order to have our methods get executed, we must call the method on the object we created.

```

`A method is a task that an object of a class performs.`

```java
public class SavingsAccount {
  int balance;
    
  public SavingsAccount(int initialBalance){
    balance = initialBalance;
  }
    
  public void checkBalance(){
    System.out.println("Hello!");
    System.out.println("Your balance is " + balance);
  }
    
  public void deposit(int amountToDeposit){
    balance = balance + amountToDeposit;
    System.out.println("You just deposited " + amountToDeposit);
  }
    
 public int withdraw(int amountToWithdraw){
     balance = balance - amountToWithdraw;
     return amountToWithdraw;

 }

public String toString(){
    return "This is a savings account with " + balance + " saved.";
  } 


  public static void main (String[] args){
    SavingsAccount savings = new SavingsAccount(200);
    savings.checkBalance();
    savings.deposit(200);
    savings.withdraw(400);
  }
         
}

```

## Calculator App

```java
//simple calculator with basic arithmetics
public class Calculator{

public Calculator(){

}
public int add(int a, int b){
  return a + b;
}

public int substract(int a, int b){
 return a-b;
}

public int multiply(int a, int b){
 return a*b;
}

public int division(int a, int b){
 return a/b;
}
public int modulo(int a, int b){
 return a%b;
}

public static void main(String[] args){
 Calculator myCalculator = new Calculator();
 System.out.println(myCalculator.add(5,7));
 System.out.println(myCalculator.substract(45, 11));
 }
}



```