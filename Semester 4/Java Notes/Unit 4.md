# Unit 4: Inheritance in Java

1. **Definition of Inheritance:**
   - **Inheritance** is a mechanism in object-oriented programming (OOP) where one class acquires the properties and behaviors (fields and methods) of another class. The class that inherits is called the **subclass** (or derived class), and the class from which it inherits is called the **superclass** (or base class).
   - Inheritance allows for code reusability and hierarchical classification.

   ```java
   class Animal {
       void eat() {
           System.out.println("Eating...");
       }
   }

   class Dog extends Animal {  // Dog is a subclass of Animal
       void bark() {
           System.out.println("Barking...");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Dog dog = new Dog();
           dog.eat();  // Inherited from Animal class
           dog.bark();  // Defined in Dog class
       }
   }
   ```

2. **Protected Data:**
   - **Protected** access modifier allows a subclass to access the member (field or method) of the superclass, even if they are in different packages. However, they cannot be accessed directly by other classes outside the subclass.
   - Example:
     ```java
     class Animal {
         protected String name;
     }

     class Dog extends Animal {
         void setName(String name) {
             this.name = name;  // Accessing protected member of superclass
         }
     }
     ```

3. **Private Data:**
   - **Private** access modifier restricts access to the member (field or method) only to the class in which it is defined. It cannot be accessed directly by any subclass or other class.
   - Example:
     ```java
     class Animal {
         private String name;
         
         private void setName(String name) {
             this.name = name;
         }
     }

     class Dog extends Animal {
         void displayName() {
             // Cannot access private members of the superclass
             // this.name = "Dog";  // Error
         }
     }
     ```

4. **Public Data:**
   - **Public** access modifier allows the member (field or method) to be accessed from anywhere, including from other classes or packages.
   - Example:
     ```java
     class Animal {
         public String name;

         public void setName(String name) {
             this.name = name;
         }
     }

     class Dog extends Animal {
         void displayName() {
             System.out.println(name);  // Accessing public member of superclass
         }
     }
     ```

5. **Constructor Chaining:**
   - **Constructor chaining** refers to the process where a constructor calls another constructor in the same or superclass.
   - In Java, constructor chaining is done using the `this()` (same class) or `super()` (superclass) keywords.
   - Example of constructor chaining:
     ```java
     class Animal {
         Animal(String name) {
             System.out.println("Animal: " + name);
         }
     }

     class Dog extends Animal {
         Dog() {
             super("Dog");  // Calling the superclass constructor
             System.out.println("Dog object created");
         }
     }

     public class Main {
         public static void main(String[] args) {
             Dog dog = new Dog();  // Output: Animal: Dog, Dog object created
         }
     }
     ```

6. **Order of Invocation:**
   - The order of constructor invocation in inheritance is always from the **topmost** class (superclass) to the **current** class (subclass).
   - In case of inheritance, the constructor of the superclass is called first, then the constructor of the subclass is called.
   - Example:
     ```java
     class Animal {
         Animal() {
             System.out.println("Animal constructor called");
         }
     }

     class Dog extends Animal {
         Dog() {
             System.out.println("Dog constructor called");
         }
     }

     public class Main {
         public static void main(String[] args) {
             Dog dog = new Dog();  // Output: Animal constructor called, Dog constructor called
         }
     }
     ```

7. **Types of Inheritance:**

   - **Single Inheritance:**
     - A subclass inherits from one superclass.
     - Example:
       ```java
       class Animal {
           void eat() {
               System.out.println("Eating...");
           }
       }

       class Dog extends Animal {
           void bark() {
               System.out.println("Barking...");
           }
       }
       ```

   - **Multilevel Inheritance:**
     - A subclass inherits from another subclass (i.e., a chain of inheritance).
     - Example:
       ```java
       class Animal {
           void eat() {
               System.out.println("Eating...");
           }
       }

       class Dog extends Animal {
           void bark() {
               System.out.println("Barking...");
           }
       }

       class Puppy extends Dog {
           void play() {
               System.out.println("Playing...");
           }
       }
       ```

   - **Hierarchical Inheritance:**
     - Multiple subclasses inherit from a single superclass.
     - Example:
       ```java
       class Animal {
           void eat() {
               System.out.println("Eating...");
           }
       }

       class Dog extends Animal {
           void bark() {
               System.out.println("Barking...");
           }
       }

       class Cat extends Animal {
           void meow() {
               System.out.println("Meowing...");
           }
       }
       ```

   - **Hybrid Inheritance:**
     - A combination of multiple types of inheritance, such as multiple inheritance (class can inherit from multiple classes), which is not directly supported in Java. However, hybrid inheritance can be achieved using interfaces.
     - Example:
       ```java
       interface Animal {
           void eat();
       }

       interface Pet {
           void play();
       }

       class Dog implements Animal, Pet {
           public void eat() {
               System.out.println("Dog is eating...");
           }

           public void play() {
               System.out.println("Dog is playing...");
           }
       }
       ```

8. **Access Control (Private, Public, Protected, Default):**

   - **Private:** The member is accessible only within the class itself. It cannot be accessed by subclasses or other classes.
     ```java
     class Person {
         private String name;
     }
     ```

   - **Public:** The member is accessible from anywhere (within the same class, subclass, or other classes).
     ```java
     class Person {
         public String name;
     }
     ```

   - **Protected:** The member is accessible within the same package and also by subclasses (even if they are in different packages).
     ```java
     class Animal {
         protected String name;
     }
     ```

   - **Default (Package-Private):** If no access modifier is specified, the member is accessible only within the same package.
     ```java
     class Person {
         String name;  // Default access
     }
     ```

### Summary:
Inheritance in Java is a powerful feature that allows one class to inherit the properties and behaviors of another. It helps in creating a hierarchical structure of classes and enables code reuse. By understanding different types of inheritance, constructor chaining, access control modifiers, and the rules of invocation order, you can create well-organized and efficient object-oriented programs.