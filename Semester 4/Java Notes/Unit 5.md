# Unit 5: Abstract Class and Interface in Java

1. **Defining an Interface:**
   - An **interface** in Java is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields.
   - All methods in an interface are implicitly **abstract**, unless they are default or static methods.
   - To define an interface, use the `interface` keyword:
     ```java
     interface Animal {
         void sound();  // Abstract method (implicitly public and abstract)
     }
     ```

2. **Difference Between Classes and Interfaces:**
   - **Class:**
     - A class can have instance variables, constructors, methods (both abstract and non-abstract), and can implement multiple interfaces.
     - A class can inherit from only **one superclass** (single inheritance).
     - You can instantiate a class (create objects).
   - **Interface:**
     - An interface can only contain method signatures and constants. It cannot contain instance fields or constructors.
     - A class can implement multiple interfaces (support for **multiple inheritance**).
     - Interfaces cannot be instantiated directly.

   **Key Differences:**
   - A class can implement multiple interfaces but can inherit from only one class (single inheritance).
   - Methods in an interface are by default abstract (no method body), whereas methods in a class can have bodies (concrete methods).
   - A class can contain fields and constructors, but an interface cannot contain instance fields or constructors.

3. **Key Points of Abstract Class & Interface:**
   - **Abstract Class:**
     - An abstract class can have both **abstract** and **non-abstract (concrete)** methods.
     - It can have instance variables and constructors.
     - A class can extend only one abstract class, since Java supports **single inheritance** for classes.
     - Abstract methods in an abstract class must be implemented by a subclass, unless the subclass is also abstract.
   - **Interface:**
     - An interface can only have abstract methods (unless using Java 8 features like default or static methods).
     - It cannot have instance fields or constructors.
     - A class can implement multiple interfaces, providing **multiple inheritance**.
     - All methods in an interface are implicitly public and abstract (unless defined as default or static).

4. **Difference Between an Abstract Class & Interface:**
   | Feature                    | Abstract Class                                     | Interface                                      |
   |----------------------------|----------------------------------------------------|------------------------------------------------|
   | **Methods**                 | Can have both abstract and concrete methods       | Can have only abstract methods (except default and static methods in Java 8 and later) |
   | **Fields**                  | Can have instance variables                       | Can have only constants (public, static, final) |
   | **Constructors**            | Can have constructors                              | Cannot have constructors                       |
   | **Access Modifiers**       | Can have access modifiers like private, protected | All methods are implicitly public unless default or static |
   | **Multiple Inheritance**    | Supports single inheritance only                   | Supports multiple inheritance via `implements` |
   | **Instantiation**           | Cannot be instantiated directly                   | Cannot be instantiated directly                |
   | **Keyword to define**       | `abstract class`                                   | `interface`                                    |

   **Example of Abstract Class:**
   ```java
   abstract class Animal {
       abstract void sound();  // Abstract method

       void sleep() {  // Concrete method
           System.out.println("Sleeping...");
       }
   }

   class Dog extends Animal {
       void sound() {  // Implementing abstract method
           System.out.println("Barking...");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Dog dog = new Dog();
           dog.sound();  // Output: Barking...
           dog.sleep();  // Output: Sleeping...
       }
   }
   ```

   **Example of Interface:**
   ```java
   interface Animal {
       void sound();  // Abstract method
   }

   class Dog implements Animal {
       public void sound() {  // Implementing interface method
           System.out.println("Barking...");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Dog dog = new Dog();
           dog.sound();  // Output: Barking...
       }
   }
   ```

5. **Implementation of Multiple Inheritance Through Interface:**
   - **Multiple inheritance** refers to the ability of a class to inherit behaviors from more than one class. Java does not support multiple inheritance for classes, but it does allow a class to implement multiple interfaces, effectively achieving multiple inheritance.
   
   Example:
   ```java
   interface Animal {
       void sound();
   }

   interface Pet {
       void play();
   }

   class Dog implements Animal, Pet {
       public void sound() {
           System.out.println("Barking...");
       }

       public void play() {
           System.out.println("Playing...");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Dog dog = new Dog();
           dog.sound();  // Output: Barking...
           dog.play();   // Output: Playing...
       }
   }
   ```

   - In this example, the `Dog` class implements two interfaces: `Animal` and `Pet`. The class `Dog` provides concrete implementations for both the `sound()` method from `Animal` and the `play()` method from `Pet`.

### Summary:
- **Abstract Class**: Used when you want to provide common behavior for subclasses but leave some methods to be implemented by the subclasses. It can have both abstract and concrete methods, as well as instance fields and constructors.
- **Interface**: Defines a contract for implementing classes, with abstract methods that must be implemented. Interfaces support multiple inheritance in Java, unlike classes.
- **Key Differences**: Abstract classes can have both abstract and concrete methods, whereas interfaces have only abstract methods (with exceptions in Java 8+). A class can implement multiple interfaces, but can extend only one abstract class.

Understanding the difference between abstract classes and interfaces, along with their usage, is crucial for writing flexible and reusable code in Java.