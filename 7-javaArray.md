## JAVA Array

```md
An array holds a fixed number of values of one type. Arrays hold doubles, ints, booleans, or any other primitives. Arrays can also contain Strings as well as object references!

Each index of an array corresponds with a different value. Here is a diagram of an array filled with integer values:
```

```java
//main.java
public class Main{
  public static void main(String[] args){

    String[] robotArticles = {"Oil News", "Innovative Motors", "Humans: Exterminate Or Not?", "Organic Eye Implants", "Path Finding in an Unknown World"};

    int[] robotViewers = {87, 32, 13, 11, 7};
    double[] robotRatings = {2.5, 3.2, 5.0, 1.7, 4.3};
    Newsfeed robotTimes = new Newsfeed(robotArticles, robotViewers, robotRatings);
      
    robotTimes.viewArticle(2);
    robotTimes.viewArticle(2);
    System.out.println("The top article is " + robotTimes.getTopArticle());
    robotTimes.changeRating(3, 5);
  }
}
```

## Newsfeed.java
```java
//Newsfeed.java
public class Newsfeed {
    String[] trendingArticles;
    int[] views;
    double[] ratings;
    
    public Newsfeed(String[] initialArticles, int[] initialViews, double[] initialRatings){
      trendingArticles = initialArticles;
      views = initialViews;
      ratings = initialRatings;
    }
    
    public String getTopArticle(){
      return trendingArticles[0];
    }
    
    public void viewArticle(int articleNumber){
      views[articleNumber] = views[articleNumber] + 1;
      System.out.println("The article '" + trendingArticles[articleNumber] + "' has now been viewed " + views[articleNumber] + " times!");
    }
    
    public void changeRating(int articleNumber, double newRating){
      if (newRating > 5 || newRating < 0) {
        System.out.println("The rating must be between 0 and 5 stars!");
      } else {
        ratings[articleNumber] = newRating;
        System.out.println("The article '" + trendingArticles[articleNumber] + "' is now rated " + ratings[articleNumber] + " stars!");
      }
    }
}
```

## Explained 

```md
## Just like with variables, we can declare and initialize in the same line. This allows us to explicitly initialize the array to contain the data we want to store :

double[] prices = {13.15, 15.87, 14.22, 16.66};


## We can use arrays to hold Strings and other objects as well as primitives:

String[] clothingItems = {"Tank Top", "Beanie", "Funny Socks", "Corduroys"};



```

## Question

```md
For now, our Newsfeed class doesn’t have any methods.

Create a method getTopics() that accepts no parameters, returns a String array, and is accessible by other classes.

Leave the body empty.

Note: it is okay for there to be an error claiming there is no main() method. This method is defined in Main.java.

##

public class Newsfeed {
  public Newsfeed(){
      
  }
  // Create getTopics() below:
  public String[] getTopics(){
    return null;
  }  
}

## ques2
Inside the getTopics() method, create a String array called topics that contains these elements:

"Opinion", "Tech", "Science", "Health" 
Remember to keep the order the same.

Then, return the topics array at the end of the method!

To see the output of the program, switch over to the Main.java file and click “Run”.


## ques3
public class Newsfeed {
  public Newsfeed(){
      
  }
  // Create getTopics() below:
  public String[] getTopics(){
    String[] topics = {"Opinion", "Tech", "Science", "Health" };
    return topics;
  }  
}


## memory addr

When we printed out the array we created in the last exercise, we saw a memory address that did not help us understand what was contained in the array.

If we want to have a more descriptive printout of the array itself, we need a toString() method that is provided by the Arrays package in Java.



`import java.util.Arrays;`

We put this at the top of the file, before we even define the class!

When we import a package in Java, we are making all of the methods of that package available in our code.

The Arrays package has many useful methods, including Arrays.toString(). When we pass an array into Arrays.toString(), we can see the contents of the array printed out:


## 
import java.util.Arrays;

public class Lottery(){
  
  public static void main(String[] args){
    int[] lotteryNumbers = {4, 8, 15, 16, 23, 42};
    String betterPrintout = Arrays.toString(lotteryNumbers);
    System.out.println(betterPrintout);
  }

}
```
```java


## Another example 

// import the Arrays package here Main.java
import java.util.Arrays;
public class Main {
  public static void main(String[] args) {
    Newsfeed sampleFeed = new Newsfeed();
    String[] topics = sampleFeed.getTopics();
    System.out.println(Arrays.toString(topics));
  }
}

```

```java
## Newsfeed.java
public class Newsfeed {
  public Newsfeed(){
      
  }
      
  public String[] getTopics(){
    String[] topics = {"Opinion", "Tech", "Science", "Health"};
    return topics;
  }
}
  
```