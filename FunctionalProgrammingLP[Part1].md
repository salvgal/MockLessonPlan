# Lesson Plan: Functional Programming and Lambda Expressions in JAVA 8


## Level Set (5 min)

### Prerequisite:
Basic Java and OOP programming up to Java 7.

### What this course cover:

1. Understanding lambdas
2. Using lambdas
3. Functional Interfaces
4. Collections improvements

### Why lambdas?

* Enables <span class="underline">Functional
Programming</span> in Java
* Code more readable and concise
* APIs and libraries are easier to use
* Enables support for parallel processing (getting the best out of multi-core processors in terms of performances)

### Requirements:

* Be sure Java (version 8 or superior) is up an running on your machine.
  On terminal, type the command `java -version` to check your version
* IntelliJ Idea or any similar IDE with Java integration


## Functional Programming vs Object Oriented Programming ( You Do - 5 min)

* Functional programming doesn’t allow developers to
do new things, but it adds new features for writing more readable code,
hence more maintainable.

* Functional programming is a new programming
paradigm that allows to write elegant code in certain situations. We
will keep using the OOP paradigm while using Java.

* In OOP everything is an object, all code blocks are
associated with classes and objects. What if you want to create a method
not tied to any class?
(Discuss all above with the students)
 

## How to create a lambda expression (You do - 5 min)

Lambda let the developer create these methods that perform an action not tied to an object/class. 
These are calle **Lambda Expressions**, or simplified **Lambdas**. These methods can
also be treated as values (this means that it will be possible to assign a
piece of code to a variable and treat is as a variable value).

Example:

```java
aBlockOfCode = {
    //some code here
}
```
That is equal to:
```java
aBlockOfCode = public void method(){
    //some code here
}
```
> Note: access modifier is already assigned in the variable, the return type is
> automatically detected by Java, and method name can be substitute by the variable name.
> All these keywords are not needed and can be omitted for simplicity.

Now we have an entire block of code that can be passed as variable in a
method and being executed. It is indeed a **Lambda Expression** when
used with the **-\>** operator:

```java
aBlockOfCode = () -> {
    //some code here
}
```
Hence, in order to create a Lambda expression, we just simply create
a normal method, omit access modifiers, return type, and
method name, adding the arrow operator -\>, and assign to a
variable.

> Note: if the method contains only one line of code, we can omit the
curly braces and the lambda expression can be written as:

```java
aBlockOfCode = () -> //a line of code here
```


## Practice (We do - 10 min):

### Practice 1 : Create a lambda expression as following
```java
greetFunction = () -> System.out.println("Hello World");
```
Now the variable greetFunction can be passed as method parameter.

### Practice 2 : Create and reduce a lambda expression as following

Create a regular method that double any number and assign the expression to a variable:
```java
public int double(int a) {
  return a * 2;
}
```
Assign it to a variable:
```java
doubleNumberFunction = public int double(int a) {
  return a * 2;
}
```
Now let’s get rid of the not necessary keywords as
described above:
```java
doubleNumberFunction = (int a) {
  return a * 2;
}
```
Finally let’s add the arrow operator, but since
there is only one line of code, we can also omit the braces and the
return keyword (for a one-line only method omitting the return keyword
is required):
```java
doubleNumberFunction = (int a) -> a * 2;
```
This is it\! Our new lambda expression is ready to be used.


## Extra Practice (We Do - 5 min):

Create new lambda expressions as the one below:
```java
addFunction = (int a, int b) -> a + b;
```
(method take as input two parameters and return the sum)
```java
safeDivisionFunction = (int a, int b) -> {
  if(b==0) return 0;
  return a / b;
};
```
(method take as input two parameters and return the division in a safely
manner)
```java
stringLengthCountFunction = (String s) -> s.length();
```
(method take as input a String and return its length)
 
## Functional Interface (You do - 5 min):

**Roadblock** - The problem we have here is that the variable we have
created have not a type, the java compiler will not accept them, so the
following question:

Q. How to declare a lambda expression?

A. Using functional interface\!

In general, a functional interface is a simple interface containing a
method that allow the lambda expression to be executed in Java.


### Code snippet:
```java
public class Greeter {
    
  public static void main(String[] args) {

    GreetInterface greetFunction = () -> System.out.println("Hello world");
 
    //lambda expression executed as interface implementation
    greetFunction.method();

    //lambda expression passed as method parameter
    greeterFunction(greetFunction);
    
    }

  public static void greeterFunction(GreetInterface greet) {
    
    greet.method();
      
  }

   interface GreetInterface {

      void method();

   }
}
```

>Note: Only one method can exist in the interface and it has to have the
>same signature of the lambda expression (not necessarily same method
>name). If we need to create and execute a second lambda expression, we
>need to create a second new interface with only one method in it.


## Lambda expression as anonymous inner class and Type Inference (You do - 5 min):

In general, a lambda expression is very similar to an anonymous inner
class \*

\* <https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html>

 

See the following example:

```java
public class Greeter {
   
   public static void main(String[] args) {

      GreetInterface greetFunction = () -> System.out.println("Hello world");

      //anonymous inner class here
      GreetInterface innerClassGreet = new GreetInterface() {
         public void method() {
            System.out.println("Hello world");
         }
      };

      //inner class execution
      greeterFunction(innerClassGreet);

      //lambda expression execution
      greeterFunction(greetFunction);

   }

   public static void greeterFunction(GreetInterface greet){
      greet.method();
   }
   

   interface GreetInterface{
      void method();
   }

}
```

Since now we tied a lambda expression to an interface, and the interface
has the method signature in it, we can sharpen our lambda expression by
omitting the type for the input parameter and the parenthesis
themselves. Looking at the example above of a lambda expression that
compute the length of a String, we are able to do something as follow:

```java
public static void main(String[] args) {
      
      //Lambda expression reduced from the form: (String s) -> s.length()
      printLambda(s -> s.length());
      
   }
   
   
   public static void printLambda(StringLengthLambda l) {
      System.out.print(l.getLength("Hello Lambda"));
   }
   
   
   interface StringLengthLambda {
      int getLength(String s);
   }

}

```
This is what is called Type Inference. Java 8 compiler seems to be more
and more smart\!


### Extra (5 min):

The class level annotation
_@FunctionalInterface_ is advised to be used
on top of functional interface to make it clear to developers that this
is an interface used for functional programming purposes (i.e. Lambda
expression). This annotation is optional: Java will run the lambda
expression with or without the annotation on top.

```java
@FunctionalInterface
public interface Greeting {
   
   public void perform();
}
```
