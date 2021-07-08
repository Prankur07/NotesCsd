# Introduction to Java

    Programming Fundamentals
    OOP concepts: Access modifiers,Polymorphism,Inheritance,Abstraction
    String concepts
    Collection Framework
    Exception Handling
    Java 8 features: Lambda Expression, Stream API, Date API
    Basics of File Handling
    Threads basic concepts
    Connectivity with database: JDBC

## Introduction to Java

## What is jdk? java development kit

>jdk has all the necessary APIs required to create
a java application and run/execute it on any platform.
    jdk=jre+APIs

## What is jre? java runtime environment

>This jre is having the necessary executables reqd to run a 
Java application. The jre is light weight and cannot be used
to create a Java application.

>javac (java compiler) responsible for compiling java source
code into byte code is not present in the jre folder. It is
only present in the jdk folder.

## Why do we say java is platform independent?

>This is because the bytecode can be shared with any platform
or os and then executed from there using proper jre.

>JDK [JVM] itself is PLATFORM DEPENDENT.

>JDK [JVM] makes your code platform independent. It is its
responsibility to convert the bytecode into proper
machine code that the os can understand and execute.

JVM is Java Virtual Machine

## Lets write a Java code...
```java
class Demo{
    public static void main(String[] a){
        System.out.println("Hello Friend!!!");
    }
}
```


Points:
1. The class name MUST START with CAPITAL LETTER.
2. When you compile the code using javac compiler
it creates the .class file(s) with the same name as 
the class name.
3. A single source file can have any number of classes
defined in it but only one class can be made public.
If a public is present, the source file MUST BE saved
with the same name as public class name.
4. The "public" is an access specifier which says
that this class is accessible to every one.
5. The class is a template stating the common properties
and behavior to be shared by the instances of the class.

## class
Trainee

    name
    birthDate
    mobile
    favoriteFood
    getDetails(){}
    printDetails(){}
    feelHungry(){}

instances

    one=>Abhinav Sharma,2009-08-16,74123658475,Chinese
    two=>Taniska Gupta,2009-06-11,7896321545,Apple

6. Every class will have a class boundary.
The class name should be a NOUN, starting with capital
letter. If multiple word, each word's first letter
should be in caps. For example: ShoppingCart
The variable name should be a NOUN.
The method name must be a VERB,action
The above two should follow lower camel case.
For ex: `feelHungry()`, favoriteFood
7. The main entry point into a Java program for the JVM
is `main()` method. Not every class does need to have a
`main()` method. 

`public static void main(String[] args){}`

**static** implies that this method is even present
and accessible without presence of any object.
void is a return type stating that this method
will not return anything

`main()` is the method name
`String` is a data type. String has been used as an array.


>An array is a collection of homogeneous elements.
The array is always of fixed size.

## COMMAND LINE ARGUMENTS
    java Demo Kiran 89.96 true a

8. A static member is shared between all the instances 
of the class.
9. A static member can access another static member
by using the classname; for accessing any non static
member it has to depend on an object.
10. Creating an object of a class...
```java
Someclass ref1=new Someclass();
```

This ref1, ref2 variables are just like envelopes
of type Someclass. The "new" keyword is responsible
for memory allocation from the heap memory of the JVM.
Once memory allocation is done the memory address
is assined back to the ref variable.


>The same reference variable (envelope) can be assigned
a new address every time( just as we re-use a pen by 
changing the refill).

11. Lets explore the code below:
```java
import java.util.Scanner;
class Demo{
    public static void main(String[] a){
        Scanner scanner=new Scanner(System.in);
        System.out.println("Enter your name:");
        String name=scanner.nextLine();
        System.out.println("Enter age:");
        int age=scanner.nextInt();
        System.out.println("Hello "+name+"\nYou are "+age+" years old");
if(age<18)
        System.out.println("Still you cannot cast your vote");
else
    System.out.println("Go...cast your vote");
        scanner.close();            
    }    
}
```

a) `import` statement is used to include a package.<br>
A package is a folder having related classes.
We are using `java.util` package.<br>
By default, we already have been using `java.lang` 
package. String and the System classes belong to
the `java.lang` package.

b) String is not a primitive data type in Java.
The pdts are :

integer:

    byte[8],short[16],int[32],long[64]
decimal:

    float[32],double[64]
character:

    char[16] to support unicode charset

boolean: only hold true and false as values

```java
Scanner sc=new Scanner(System.in);
```

where `System.in` represents standard input device
which is our keyboard.

    - next() [soma]
    - nextLine() [soma gupta]
    - nextInt()
    - nextBoolean()
    - nextFloat()
    *- char ch=sc.next().charAt(0);    

`System.out.println();`

where System.out represents standard output device
which is our console.

The moment, I write `scanner.close();` the object assigned
to the reference variable scanner becomes eligible for 
garbage collection.

    Using Eclipse IDE
    Concept of constructor
    String as a data type
    Exploring Array concept 
    Polymorphism : Static polymorphism: method overloading
    Using "this" keyword to resolve ambiguity

## Workspace
- a collection of java projects
- a project can contain a collection of java source files
    
    File> New> Java Project
    Right click src folder> New> Class

`// single line`

`/*  */ multiple line` 

```java
Book book1=new Book();
```

## Concept of constructor
A constructor is a special method having the same name as
that of the class. Whenever, we create an instance of the 
class, the constructor is implicitly invoked.
This method does have any return type defined explicitly.
If we do not write a constructor on our own, the java compiler
will provide us a default(no arg) constructor on its own. 
A constructor can be used to initialize the instance variables
to some non default values.

So we can use parametrized constructor
A constructor to which we will supply values from outside.
The `"this"` keyword is used to resolve the ambiguity
between the instance variable and the local variable.<br>
Eg: `this.title=title;`

Therefore, we can overload constructors.
Overloading means the same method showing itself in 
multiple forms.

### Static polymorphism: method overloading

The thing that matters is the method signature:
    
    a) no of parameters
    b) data type of parameters
    c) sequence of parameters

Either one or all of them should be different
to make overloading correct.

## Array
Array is a homogeneous collection of elements.
We create an array in Java by writing,
```java
    data_type arr_name[]=new data_type[size];
    int numbers[]=new int[5];   
    Book books[]=new Book[5];
    
    //We may also use array initializer,
    int[] nums={5,8,6,4};
    //Arrays class is part of your java.util package
```

```java
import java.util.Arrays;
int numbers[]= {7,2,6,4,1,2,3,5,2};
//for(int i=0;i<numbers.length;i++)
    //System.out.println(numbers[i]);
 //Arrays.sort(numbers);//Dual-Pivot Quicksort
    System.out.println(Arrays.toString(numbers));
    Arrays.fill(numbers,3,5,9);
    System.out.println(Arrays.toString(numbers));
        
    //for(int n:numbers) System.out.println(n);
```
In the `Arrays.fill()` method;

    arg1 => array ref
    arg2 => start index
    arg3 => end index(exclusive)
    arg4 => number to replace with

## Methods of String class...
        String s="java programming";
        System.out.println(s.length());
        System.out.println(s.toUpperCase());
        System.out.println(s.charAt(6));//r
        System.out.println(s.indexOf('r'));//6
        System.out.println(s.lastIndexOf('r'));//9
        System.out.println(s.startsWith("Java"));//false
        System.out.println(s.endsWith("ing"));//true
        char letters[]=s.toCharArray();
        System.out.println(Arrays.toString(letters));
