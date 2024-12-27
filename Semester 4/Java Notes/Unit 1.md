# Unit 1. Introduction and Features  

**Fundamentals of Object-Oriented Programming (OOP) vs. Procedure-Oriented Programming:**

1. **Procedure-Oriented Programming (POP):**
   - Focuses on functions or procedures to operate on data.
   - Programs are divided into functions that perform tasks in sequence.
   - Data is separate from functions and is passed between functions.
   - Easier to understand and use for small programs, but can become difficult to manage for large systems.

2. **Object-Oriented Programming (OOP):**
   - Focuses on objects, which are instances of classes that combine both data and functions.
   - Data and functions are bundled together inside classes.
   - Promotes code reuse, scalability, and easier maintenance through principles like inheritance, polymorphism, and encapsulation.
   - Helps in organizing large and complex programs by breaking them into smaller, more manageable components.

---

**Object-Oriented Programming Concepts:**

1. **Classes and Objects:**
   - **Class:** A blueprint or template for creating objects. It defines the attributes and methods that objects created from the class will have.
   - **Object:** An instance of a class. It represents a real-world entity with specific attributes and behaviors as defined by the class.

2. **Object Reference:**
   - A reference is a variable that holds the memory address of an object. It's used to interact with the object.

3. **Abstraction:**
   - Hides the internal workings of an object and only exposes the necessary functionality. This allows users to interact with the object without needing to know the details of how it works internally.
   - Example: A car's engine is abstracted; you only need to know how to drive, not how the engine works.

4. **Encapsulation:**
   - Bundles data (attributes) and methods (functions) together in a class, and restricts access to certain details through access modifiers (like `private`, `protected`, and `public`).
   - Example: A bank account has private attributes for balance but exposes public methods to deposit and withdraw money.

5. **Inheritance:**
   - Allows a class to inherit properties and methods from another class. The class that inherits is called the subclass, and the class being inherited from is called the superclass.
   - Promotes code reuse and hierarchical relationships between classes.
   - Example: A `Dog` class can inherit from a `Animal` class.

6. **Polymorphism:**
   - Refers to the ability of one function or method to behave differently depending on the object it is acting on. It can be achieved through method overriding or method overloading.
   - Example: A method `speak()` might behave differently for `Dog` and `Cat` objects.

---

**Introduction to Eclipse (IDE) for Java Development:**

- **Eclipse** is a powerful, widely used Integrated Development Environment (IDE) primarily for Java development but also supports other languages like C/C++, PHP, and Python.
  
**Key Features of Eclipse:**
   1. **Code Editing:** Offers syntax highlighting, code completion, and error checking to make coding more efficient.
   2. **Debugging:** Built-in tools to help developers step through code, set breakpoints, and inspect variables during runtime.
   3. **Project Management:** Supports creating, managing, and organizing large projects.
   4. **Plugins:** A wide range of plugins to extend the functionality of the IDE for various tasks such as version control, testing, and deployment.
   5. **Integration with Build Systems:** Integrates well with build tools like Maven and Gradle for easy dependency management and project building.
   6. **Refactoring Tools:** Helps in improving and restructuring code without changing its external behavior.

In summary, OOP principles allow for more modular, reusable, and scalable code. Eclipse provides an efficient environment for Java programming with powerful features that aid in development, debugging, and project management.