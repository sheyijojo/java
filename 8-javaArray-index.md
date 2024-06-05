## Get Element By Index 
```md
Now that we have an array declared and initialized, we want to be able to get values out of it.

We use square brackets, [ and ], to access data at a certain index:
```

```java
double[] prices = {13.1, 15.87, 14.22, 16.66};
System.out.println(prices[1]);



//If we try to access an element outside of its appropriate index range, we will receive an ArrayIndexOutOfBoundsException error.

//For example, if we were to run the command System.out.println(prices[5]), we’d get the following output:

//java.lang.ArrayIndexOutOfBoundsException: 5

```


## Exercise

```java

## Main.java
import java.util.Arrays;
public class Main {
  public static void main(String[] args) {
    Newsfeed sampleFeed = new Newsfeed();
        
    System.out.println("The top topic is " + sampleFeed.getFirstTopic());
        
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(3);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(1);
        
    System.out.println("The " + sampleFeed.topics[1] + " topic has been viewed " + sampleFeed.views[1] + " times!");
  }
}

## Newsfeed.java
public class Newsfeed {
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  public int[] views = {0, 0, 0, 0};
  
  public Newsfeed(){

  }
    
  public String[] getTopics(){
    return topics;
  }
  
  // Create getFirstTopic() below
  public String getFirstTopic(){
    return topics[0];
  }
  
  public void viewTopic(int topicIndex){
    
  }
}
```

##

```md
Inside the Newsfeed class, create a method called getFirstTopic() that returns a String and accepts no parameters.

Inside the getFirstTopic() method, return the first element of the topics array.

##

We have added an array called views to keep track of how many viewers visit a topic.

Every time someone views a topic, we want to increase the value of the corresponding element in views by 1.

For example, if someone views an “Opinion” piece (index of 0 in topics), we will increase the value of the 0th index of views by 1.

Inside the viewTopic() method, implement this functionality. The parameter topicIndex represents the location of the element in topics that was viewed.

Note: switch over to the Main.java file to see the output of the program you wrote.


## main.java
import java.util.Arrays;
public class Main {
  public static void main(String[] args) {
    Newsfeed sampleFeed = new Newsfeed();
        
    System.out.println("The top topic is " + sampleFeed.getFirstTopic());
        
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(3);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(1);
        
    System.out.println("The " + sampleFeed.topics[1] + " topic has been viewed " + sampleFeed.views[1] + " times!");
  }
}


## Newsfeed

We have added an array called views to keep track of how many viewers visit a topic.

Every time someone views a topic, we want to increase the value of the corresponding element in views by 1.

For example, if someone views an “Opinion” piece (index of 0 in topics), we will increase the value of the 0th index of views by 1.

Inside the viewTopic() method, implement this functionality. The parameter topicIndex represents the location of the element in topics that was viewed.

Note: switch over to the Main.java file to see the output of the program you wrote.



public class Newsfeed {
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  public int[] views = {0, 0, 0, 0};
  
  public Newsfeed(){

  }
    
  public String[] getTopics(){
    return topics;
  }
  
  // Create getFirstTopic() below
  public String getFirstTopic(){
    return topics[0];
  }
  
  public void viewTopic(int topicIndex){
    topics[topicIndex] = topics[topicIndex] + 1; 
    views[topicIndex] = views[topicIndex] + 1;
  }
}

## Thier solution
public class Newsfeed {
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  public int[] views = {0, 0, 0, 0};
  
  public Newsfeed(){

  }
    
  public String[] getTopics(){
    return topics;
  }
  
  public String getFirstTopic(){
    return topics[0];
  }

  
  public void viewTopic(int topicIndex){
    views[topicIndex]++;
  }
}

```

## Creating an Empty Array