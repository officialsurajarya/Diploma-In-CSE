# Unit 6: Polymorphism in Java

Polymorphism is one of the fundamental concepts in Object-Oriented Programming (OOP) that allows objects to be treated as instances of their parent class. The two main types of polymorphism in Java are **compile-time polymorphism (method overloading)** and **runtime polymorphism (method overriding)**.

### 1. **Method and Constructor Overloading**

#### **Method Overloading:**
- **Method overloading** occurs when multiple methods in the same class have the same name but differ in the number or type of parameters (or both).
- It is a form of **compile-time polymorphism** because the method to be called is resolved during compilation.
  
  **Key points about method overloading:**
  - Overloading does not depend on the return type of the method.
  - Overloaded methods can have different parameter types or a different number of parameters.

  **Example of Method Overloading:**
  ```java
  class Calculator {
      // Method to add two integers
      int add(int a, int b) {
          return a + b;
      }

      // Overloaded method to add three integers
      int add(int a, int b, int c) {
          return a + b + c;
      }

      // Overloaded method to add two double values
      double add(double a, double b) {
          return a + b;
      }
  }

  public class Main {
      public static void main(String[] args) {
          Calculator calc = new Calculator();
          System.out.println(calc.add(10, 20));        // Output: 30
          System.out.println(calc.add(10, 20, 30));    // Output: 60
          System.out.println(calc.add(10.5, 20.5));    // Output: 31.0
      }
  }
  ```

#### **Constructor Overloading:**
- **Constructor overloading** occurs when multiple constructors with different parameter lists are present in the same class.
- This allows you to create objects in different ways, depending on the parameters passed to the constructor.

  **Example of Constructor Overloading:**
  ```java
  class Person {
      String name;
      int age;

      // Constructor with no parameters
      Person() {
          name = "Unknown";
          age = 0;
      }

      // Constructor with parameters
      Person(String name, int age) {
          this.name = name;
          this.age = age;
      }

      void display() {
          System.out.println("Name: " + name + ", Age: " + age);
      }
  }

  public class Main {
      public static void main(String[] args) {
          Person person1 = new Person();
          Person person2 = new Person("Alice", 25);

          person1.display();  // Output: Name: Unknown, Age: 0
          person2.display();  // Output: Name: Alice, Age: 25
      }
  }
  ```

### 2. **Method Overriding**

- **Method overriding** occurs when a subclass provides a specific implementation for a method that is already defined in its superclass.
- This is a form of **runtime polymorphism**, because the method to be called is determined at runtime based on the type of object.
  
  **Key points about method overriding:**
  - The method in the subclass must have the same name, return type, and parameters as the method in the superclass.
  - The `@Override` annotation is often used to indicate that a method is overriding a method in the superclass.

  **Example of Method Overriding:**
  ```java
  class Animal {
      void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      // Overriding the sound method in Animal class
      @Override
      void sound() {
          System.out.println("Dog barks");
      }
  }

  class Cat extends Animal {
      // Overriding the sound method in Animal class
      @Override
      void sound() {
          System.out.println("Cat meows");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Animal animal = new Animal();
          animal.sound();  // Output: Animal makes a sound

          Animal dog = new Dog();  // Upcasting
          dog.sound();  // Output: Dog barks (runtime polymorphism)

          Animal cat = new Cat();  // Upcasting
          cat.sound();  // Output: Cat meows (runtime polymorphism)
      }
  }
  ```

### 3. **Up-Casting and Down-Casting**

#### **Up-Casting:**
- **Up-casting** is the process of assigning a subclass object to a superclass reference. This is safe because every subclass object is an instance of the superclass.
- Upcasting is **automatic** in Java, as the subclass is a type of the superclass.

  **Example of Up-Casting:**
  ```java
  class Animal {
      void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      void sound() {
          System.out.println("Dog barks");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Animal animal = new Dog();  // Upcasting
          animal.sound();  // Output: Dog barks
      }
  }
  ```

#### **Down-Casting:**
- **Down-casting** is the process of assigning a superclass reference back to a subclass type. This is not automatically done and requires an explicit cast.
- Downcasting can result in a **ClassCastException** at runtime if the object being cast is not an instance of the subclass.

  **Example of Down-Casting:**
  ```java
  class Animal {
      void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      void sound() {
          System.out.println("Dog barks");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Animal animal = new Dog();  // Upcasting
          animal.sound();  // Output: Dog barks

          // Downcasting
          Dog dog = (Dog) animal;  // Explicit cast
          dog.sound();  // Output: Dog barks
      }
  }
  ```

  **Example of Invalid Down-Casting (causing ClassCastException):**
  ```java
  class Animal {
      void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      void sound() {
          System.out.println("Dog barks");
      }
  }

  class Cat extends Animal {
      void sound() {
          System.out.println("Cat meows");
      }
  }

  public class Main {
      public static void main(String[] args) {
          Animal animal = new Dog();  // Upcasting
          animal.sound();  // Output: Dog barks

          // Invalid down-casting
          Cat cat = (Cat) animal;  // Throws ClassCastException
          cat.sound();
      }
  }
  ```

### Summary:

- **Method Overloading** is when you define multiple methods with the same name but different parameters (compile-time polymorphism).
- **Method Overriding** is when a subclass provides a specific implementation of a method that is already defined in the superclass (runtime polymorphism).
- **Up-Casting** is when a subclass object is assigned to a superclass reference, and it happens automatically.
- **Down-Casting** is when a superclass reference is explicitly cast to a subclass reference, which can lead to runtime exceptions if not done properly.

Polymorphism allows objects to behave differently based on the context in which they are used, making the program more flexible and extensible.