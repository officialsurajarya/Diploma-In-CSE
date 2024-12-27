# Unit 3: Class and Objects in Java

1. **Class Fundamentals:**
   - A **class** in Java is a blueprint or template for creating objects. It defines the attributes (variables) and behaviors (methods) that objects created from the class will have.
   - A class is defined using the `class` keyword:
     ```java
     class Car {
         String model;
         int year;

         void display() {
             System.out.println("Model: " + model + ", Year: " + year);
         }
     }
     ```

2. **Constructors:**
   - A **constructor** is a special method that is called when an object is created. It initializes the object and its attributes.
   - **Default Constructor**: If no constructor is defined, Java provides a default constructor.
   - **Parameterized Constructor**: A constructor that takes parameters to initialize the object with specific values.
     ```java
     class Car {
         String model;
         int year;

         // Default constructor
         Car() {
             model = "Unknown";
             year = 0;
         }

         // Parameterized constructor
         Car(String model, int year) {
             this.model = model;
             this.year = year;
         }
     }
     ```

3. **Declaring Objects (Object & Object Reference):**
   - **Object**: An instance of a class created in memory. An object can have its own data (attributes) and methods.
   - **Object Reference**: A reference variable that holds the address of an object.
     ```java
     Car myCar = new Car("Toyota", 2020);  // Creating an object of class Car
     ```

4. **Creating and Accessing Variables and Methods:**
   - You can access the variables and methods of an object using the dot (`.`) operator.
     ```java
     myCar.model = "Honda";  // Accessing and modifying the model variable
     myCar.display();        // Calling the display() method
     ```

5. **Static and Non-static Variables/Methods:**
   - **Static variables and methods** are shared by all objects of a class. They belong to the class itself, rather than to any specific object.
     - **Static variable:** A variable declared with the `static` keyword.
     - **Static method:** A method declared with the `static` keyword.
     ```java
     class Example {
         static int counter = 0;  // Static variable

         static void increment() {  // Static method
             counter++;
         }
     }

     Example.increment();  // Calling the static method without creating an object
     System.out.println(Example.counter);  // Output: 1
     ```

   - **Non-static variables and methods** belong to a specific object. Each object has its own copy of non-static variables and methods.
     ```java
     class Person {
         String name;  // Non-static variable
         
         void greet() {  // Non-static method
             System.out.println("Hello, " + name);
         }
     }

     Person p = new Person();
     p.name = "Alice";  // Accessing non-static variable
     p.greet();  // Calling non-static method
     ```

6. **Defining Packages:**
   - A **package** is a namespace that organizes a set of related classes and interfaces. It helps in avoiding name conflicts and maintaining modular code.
   - You can define a package using the `package` keyword at the beginning of a Java file:
     ```java
     package mypackage;

     public class MyClass {
         public void display() {
             System.out.println("Inside mypackage!");
         }
     }
     ```

7. **Creating and Accessing a Package:**
   - To create and access classes in a package, use the `import` statement in other classes:
     ```java
     import mypackage.MyClass;

     public class Main {
         public static void main(String[] args) {
             MyClass obj = new MyClass();
             obj.display();  // Accessing the method from the imported package
         }
     }
     ```

8. **Importing Packages:**
   - You can import specific classes or all classes from a package using the `import` keyword.
     - Importing a single class:
       ```java
       import mypackage.MyClass;
       ```
     - Importing all classes from a package:
       ```java
       import mypackage.*;
       ```

9. **Understanding CLASSPATH:**
   - **CLASSPATH** is an environment variable that tells the Java Virtual Machine (JVM) where to look for classes and packages.
   - You can set the CLASSPATH to include directories or JAR files that contain compiled classes.
   - Example of setting CLASSPATH:
     ```bash
     export CLASSPATH=/path/to/classes:/path/to/jarfiles
     ```
   - When you run a Java program, the JVM uses the CLASSPATH to find and load class files.

10. **Autoboxing:**
    - **Autoboxing** is the automatic conversion of primitive data types into their corresponding wrapper classes (objects) and vice versa.
    - For example, an `int` is automatically converted to an `Integer` when assigned to an `Integer` object:
      ```java
      int num = 10;
      Integer obj = num;  // Autoboxing: int to Integer
      ```

11. **String:**
    - A **String** is a sequence of characters. In Java, strings are objects of the `String` class.
    - Strings are immutable, meaning their values cannot be changed after they are created.
    - Example:
      ```java
      String greeting = "Hello, World!";
      System.out.println(greeting.length());  // Output: 13
      ```

12. **StringBuffer:**
    - `StringBuffer` is a mutable sequence of characters. Unlike `String`, it allows modification of its content without creating new objects.
    - Example:
      ```java
      StringBuffer sb = new StringBuffer("Hello");
      sb.append(" World");
      System.out.println(sb);  // Output: Hello World
      ```

In summary, this unit introduces the core principles of classes and objects in Java, including how to create and manage classes, objects, and methods. It covers key concepts such as static vs. non-static variables, packages, autoboxing, and the use of `String` and `StringBuffer` for handling text. Understanding these concepts is crucial for writing organized, efficient, and reusable Java programs.