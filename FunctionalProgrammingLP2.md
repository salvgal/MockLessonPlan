<div class="WordSection1">

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>PART <span class="GramE">1 :</span> JAVA 8 LAMBDA

 

Prerequisite: All the material below can be applied only if Java 8 is
running on the JVM. Inferior Java version will not work.

 

What this course cover:

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Understanding lambdas

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Using lambdas

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Functional Interfaces

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Collections improvements

 

Why lambdas?

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Enables <span class="underline">Functional
Programming</span> in Java

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Code more readable and concise

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>APIs and libraries are easier to use

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Enables support for parallel processing (getting
the best out of multi-core processors in terms of performances)

 

Requirements:

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Be sure Java (version 8 or superior) is up and
running on your machine. On terminal, type the command *java -version*

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image001.png)</span>

 

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>IntelliJ Idea or another similar IDE with Java
integration

 

Functional Programming vs Object Oriented Programming:

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Functional programming doesn’t allow developers to
do new things, but it adds new features for writing more readable code,
hence more maintainable.

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Functional programming is a new programming
paradigm that allows to write elegant code in certain situations. We
will keep using the OOP paradigm while using Java.

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>In OOP everything is an object, all code blocks are
associated with classes and objects. What if you want to create a method
not tied to any class?

 

How to create a lambda expression:

<span style="font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">     
</span></span></span>Lambda let the developer create these functions
that perform an action not tied to an object/class. These are called
**Lambda Expressions**, or simplified **Lambdas.** These functions can
be treated as values (this means that it will be possible to assign a
piece of code to a variable and treat is as a variable value).

Example:

<span style="mso-tab-count:1">      </span><span style="mso-no-proof:
yes">![](FunctionalProgrammingLessonPlan.fld/image002.png)</span>

Similar to this:

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image003.png)</span>

<span style="mso-tab-count:1">           
</span><span style="mso-spacerun:yes">      </span>Note: access modifier
is already assigned in the variable, and the return type is
automatically detected by Java, while method name is not needed since we
have a variable name for referring to it, so all these keywords can be
omitted for simplicity.

<span style="mso-tab-count:1">            </span>

Now we have an entire block of code that can be passed as variable in a
method and being executed. It is indeed a **Lambda Expression** when
used with the **-\>** operator:

<span style="mso-tab-count:2">                       
</span><span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image004.png)</span>

Hence, in order to create a Lambda expression, we just simply can create
a normal method, getting rid of the access modifier, return type, and
method name, while adding the arrow operator -\>, and assign to a
variable.

 

Note: if the method contains only one line of code, we can omit the
curly braces and the lambda expression can be written as:

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image005.png)</span>

 

PRACTICE 1 (We Do):

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Create a lambda expression as
<span class="GramE">following :</span>

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image006.png)</span>

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Now the variable greetFunction can be passed as
method parameter.

 

PRACTICE 2 (We Do):

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Create a regular method that double any input
parameter and assign it to a variable:

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image007.png)</span>

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Assign it to a variable:

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image008.png)</span>

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Now let’s get rid of the not necessary keywords as
described above:

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image009.png)</span>

<span style="mso-ascii-font-family:Calibri;mso-fareast-font-family:Calibri;
mso-hansi-font-family:Calibri;mso-bidi-font-family:Calibri"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">      
</span></span></span>Finally let’s add the arrow operator, but since
there is only one line of code, we can also omit the braces and the
return keyword (for a one-line only method omitting the return keyword
is required):

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image010.png)</span>

This is it\! Our new lambda expression.

 

EXTRA PRACTICE (If time permitted):

 

Create new lambda expressions as the one below:

 

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image011.png)</span><span style="mso-spacerun:yes"> </span>

(method take as input two parameters and return the sum)

 

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image012.png)</span><span style="mso-spacerun:yes"> </span>

(method take as input two parameters and return the division in a safely
manner)

 

 

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image013.png)</span><span style="mso-spacerun:yes"> </span>(method
take as input a String and return its length)

<div style="mso-element:para-border-div;border:none;border-bottom:solid windowtext 1.0pt;
mso-border-bottom-alt:solid windowtext .75pt;padding:0in 0in 1.0pt 0in;
margin-left:.5in;margin-right:0in">

 

</div>

 

Functional Interface:

Roadblock - The problem we have here is that the variable we have
created have not a type, the java compiler will not accept them, so the
following question:

Q. How to declare a lambda expression?

A. Using functional interface\!

 

In general, a functional interface is a simple interface containing a
method that allow the lambda expression to be executed in Java.

 

Code snippet:

            public class Greeter {
    
       
    
       public static void main(String[] args) {
    
    
    
          GreetInterface greetFunction = () -> System.out.println("Hello world");
    
    
    
          //lambda expression executed as interface implementation
    
          greetFunction.method();
    
    
    
          //lambda expression passed as method parameter
    
          greeterFunction(greetFunction);
    
    
    
       }
    
    
    
       public static void greeterFunction(GreetInterface greet){
    
          greet.method();
    
       }

``` 



   interface GreetInterface{

      void method();

   }
```

``` 
}
```

 

Note: Only one method can exist in the interface and it has to have the
same signature of the lambda expression (not necessarily same method
name). If we need to create and execute a second lambda expression, we
need to create a second new interface with only one method in it.

 

Lambda expression as anonymous inner class and Type Inference:

In general, a lambda expression is very similar to an anonymous inner
class \*

<span style="font-family:&quot;Times New Roman&quot;,serif;mso-fareast-font-family:
&quot;Times New Roman&quot;"><https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html></span>

 

See the following example:<span style="font-size:9.0pt;
font-family:Menlo;mso-fareast-font-family:&quot;Times New Roman&quot;;color:#CC7832"></span>

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

 

Since now we tied a lambda expression to an interface, and the interface
has the method signature in it, we can sharpen our lambda expression by
omitting the type for the input parameter and the parenthesis
themselves. Looking at the example above of a lambda expression that
compute the length of a String, we are able to do something as follow:

 

    public class TypeInferenceExample {
    
    
    
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

 

This is what is called Type Inference. Java 8 compiler seems to be more
and more smart\!

 

Extra:

The class level annotation
@<span class="SpellE">FunctionalInterface</span> is advised to be used
on top of functional interface to make it clear to developers that this
is an interface used for functional programming purposes (i.e. Lambda
expression). This annotation is optional: Java will run the lambda
expression with or without the annotation on top.

 

    @FunctionalInterface
    
    public interface Greeting {
    
       
    
       public void perform();
    
    
    
    }

 

PRACTICE:

 

    public class Unit1Exercise {
    
    
    
       public static void main(String[] args) {
    
          List<Person> people = Arrays.asList(
    
                new Person("Charles", "Dickens", 60),
    
                new Person("Lewis", "Carroll", 42),
    
                new Person("Thomas", "Carlyle", 51),
    
                new Person("Charlotte", "Bronte", 45),
    
                new Person("Matthew", "Arnold", 39)
    
                );
    
          
    
          // Step 1: Sort list by last name
    
          
    
          // Step 2: Create a method that prints all elements in the list
    
          
    
          // Step 3: Create a method that prints all people that have last name beginning with C 
    
    
    
       }
    
    
    
    }

 

    public class Person {
    
    
    
       private String firstName;
    
       private String lastName;
    
       private int age;
    
       
    
       
    
       
    
       public Person(String firstName, String lastName, int age) {
    
          super();
    
          this.firstName = firstName;
    
          this.lastName = lastName;
    
          this.age = age;
    
       }
    
       
    
       public String getFirstName() {
    
          return firstName;
    
       }
    
       public void setFirstName(String firstName) {
    
          this.firstName = firstName;
    
       }
    
       public String getLastName() {
    
          return lastName;
    
       }
    
       public void setLastName(String lastName) {
    
          this.lastName = lastName;
    
       }
    
       public int getAge() {
    
          return age;
    
       }
    
       public void setAge(int age) {
    
          this.age = age;
    
       }
    
    
    
       @Override
    
       public String toString() {
    
          return "Person [firstName=" + firstName + ", lastName=" + lastName + ", age=" + age + "]";
    
       }
    
       
    
    }

 

 

PRACTICE SOLUTIONS:

 

    public class Unit1ExerciseSolution {
    
    
    
       public static void main(String[] args) {
    
          List<Person> people = Arrays.asList(
    
                new Person("Charles", "Dickens", 60),
    
                new Person("Lewis", "Carroll", 42),
    
                new Person("Thomas", "Carlyle", 51),
    
                new Person("Charlotte", "Bronte", 45),
    
                new Person("Matthew", "Arnold", 39)
    
          );
    
    
    
          // Step 1: Sort list by last name
    
          Collections.sort(people, (p1, p2) -> p1.getLastName().compareTo(p2.getLastName()));
    
    
    
          // Step 2: Create a method that prints all elements in the list
    
          System.out.println("Printing all persons");
    
          printConditionally(people, p -> true);
    
    
    
          // Step 3: Create a method that prints all people that have last name beginning with C
    
          System.out.println("Printing all persons with last name beginning with C");
    
          printConditionally(people, p -> p.getLastName().startsWith("C"));
    
    
    
          System.out.println("Printing all persons with first name beginning with C");
    
    
    
          printConditionally(people, p -> p.getFirstName().startsWith("C"));
    
    
    
       }
    
    
    
       private static void printConditionally(List<Person> people, Condition condition) {
    
          for (Person p : people) {
    
             if (condition.test(p)) {
    
                System.out.println(p);
    
             }
    
          }
    
       }
    
    
    
       interface Condition {
    
          boolean test(Person p);
    
       }
    
    
    
    }

 

 

 

PART 2: COLLECTIONS AND STREAMS WITH JAVA 8 LAMBDA

 

 

Streams: A sequence of elements supporting sequential and parallel
aggregate operations.

 

Collection:<span style="mso-spacerun:yes">  </span>list of elements \[
1-\>2-\>3-\>4-\>5-\><span class="GramE">6 \]</span>

 

With streams we are able to apply different (multiple) operations on
collections at the same time. To be specific and make an example, image
our collection as a rolling belt used in industry, objects in the
rolling belt will pass through while different operators inspect and do
operations on the objects at the same time. This is what happens to
collections while using streams.

 

Example:

 

    public class StreamsExample {
    
    
    
       public static void main(String[] args) {
    
          List<Person> people = Arrays.asList(
    
                new Person("Charles", "Dickens", 60),
    
                new Person("Lewis", "Carroll", 42),
    
                new Person("Thomas", "Carlyle", 51),
    
                new Person("Charlotte", "Bronte", 45),
    
                new Person("Matthew", "Arnold", 39)
    
                );
    
    
    
    
    
          //EXAMPLE 1:

          //printing out only the names of people who last name start with the letter C
    
          people.stream()
    
          .filter(p -> p.getLastName().startsWith("C"))
    
          .forEach(p -> System.out.println(p.getFirstName()));
    
          
    
          
    
          //EXAMPLE 2:

          //counting the number of people who last name start with the letter D
    
          long count = people.parallelStream()
    
          .filter(p -> p.getLastName().startsWith("D"))
    
          .count();
    
          
    
          System.out.println(count);
    
    
    
       }
    
    
    
    }

 

    public class Person {
    
    
    
       private String firstName;
    
       private String lastName;
    
       private int age;
    
       
    
       
    
       
    
       public Person(String firstName, String lastName, int age) {
    
          super();
    
          this.firstName = firstName;
    
          this.lastName = lastName;
    
          this.age = age;
    
       }
    
       
    
       public String getFirstName() {
    
          return firstName;
    
       }
    
       public void setFirstName(String firstName) {
    
          this.firstName = firstName;
    
       }
    
       public String getLastName() {
    
          return lastName;
    
       }
    
       public void setLastName(String lastName) {
    
          this.lastName = lastName;
    
       }
    
       public int getAge() {
    
          return age;
    
       }
    
       public void setAge(int age) {
    
          this.age = age;
    
       }
    
    
    
       @Override
    
       public String toString() {
    
          return "Person [firstName=" + firstName + ", lastName=" + lastName + ", age=" + age + "]";
    
       }
    
    
    
    }

 

 

Example 1 explanation:

 

Starting with a collection (List) of elements Person named people, we
apply the method stream() using the dot notation, now the collection is
in a stream and multiple operations can be performed.

The first operation is filter(), this operator select only certain
elements of the list that pass a specific condition, the condition is
declared as Lambda expression. In our case, the lambda expression will
take each person from the list (input p) and select based on the last
name starting with the letter ‘C’ (body of the lambda expression).
Finally, only for the selected elements the operator forEach() will be
applied. It takes a new Lambda expression as input. In our case the
lambda method body will print out the first name of each person.

 

 

Example 2 explanation:

Same as Example 1 but in this case the count() operator will be applied,
which does not take a lambda expression in input. It just counts the
elements that are in the filtered collection.

 

 

 

Different operators that can be applied to the stream() method are the
following:

 

<span style="mso-no-proof:yes">![](FunctionalProgrammingLessonPlan.fld/image014.png)</span>

 

 

These will allow a more performant execution of operations on
collections, thanks to Streams and Lambda Expression (Functional
Programming) in Java.

</div>