# Unit-9 Classes in Python

## Principles of Object-Oriented Programming (OOP)
Object-Oriented Programming (OOP) models real-world scenarios by using objects in code. It allows developers to create applications with **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**. This approach reduces redundancy and increases reusability.

---

## Creating a Class
A **class** is a blueprint or template for creating objects, defining their properties and behaviors (methods).

**Syntax:**
```python
class Class_Name:
    body
```

**Example:**
```python
class Details:
    name = "Suraj"
    age = 21
```

---

## Objects
An **object** is an instance of a class, used to access the properties and methods defined in the class.

**Example:**
```python
obj1 = Details()
print(obj1.name)  # Output: Suraj
print(obj1.age)   # Output: 21
```

---

## Class Variables
Class variables are shared among all instances of a class. They are defined within the class, typically at the top.

**Example:**
```python
class MyClass:
    var = "xyz"
```

---

## Instance Methods
Instance methods operate on individual objects (instances) of a class and use `self` as the first argument.

**Syntax:**
- Without parameters:
  ```python
  def method_name(self):
      function_body
  ```
- With parameters:
  ```python
  def method_name(self, param1, param2):
      function_body
  ```

**Example:**
```python
class Mobile:
    def showModel(self):
        print("RealMe X")

realme = Mobile()
realme.showModel()  # Output: RealMe X
```

---

## File Organization in OOP
In Python, organizing files for OOP involves structuring code into multiple files and classes for better modularity, reusability, and maintenance.

---

## Inheritance
Inheritance allows a subclass to inherit properties and methods from a parent class.

### Types of Inheritance:
1. **Single Inheritance**: One subclass inherits from one parent class.
2. **Multiple Inheritance**: A subclass inherits from multiple parent classes.
3. **Multilevel Inheritance**: A subclass inherits from another subclass.
4. **Hierarchical Inheritance**: Multiple subclasses inherit from a single parent class.
5. **Hybrid Inheritance**: A combination of two or more types of inheritance.

**Syntax:**
```python
class ParentClass:
    body

class ChildClass(ParentClass):
    body
```

**Example:**
```python
class Animal:  
    def speak(self):  
        print("Animal Speaking")  

class Dog(Animal):  
    def bark(self):  
        print("Dog barking")  

d = Dog()  
d.bark()   # Output: Dog barking
d.speak()  # Output: Animal Speaking
```

---

## Polymorphism
Polymorphism allows objects of different classes to be treated as objects of a common superclass. There are two types:

1. **Compile-Time Polymorphism (Static Polymorphism)**: Achieved through **method overloading**.
   **Example:**
   ```python
   class Calculator:
       def add(self, *args):
           return sum(args)

   calc = Calculator()
   print(calc.add(2, 3))          # Output: 5
   print(calc.add(2, 3, 4, 5))    # Output: 14
   print(calc.add(1, 2, 3, 4, 5)) # Output: 15
   ```

2. **Run-Time Polymorphism**: Achieved through **method overriding**.
   **Example:**
   ```python
   class Animal:
       def sound(self):
           print("Animal makes a sound")

   class Dog(Animal):
       def sound(self):
           print("Dog barks")

   dog = Dog()
   dog.sound()  # Output: Dog barks
   ```

---

## String Splitting Example
**Example:**
```python
str1 = "My name is Ankit"
print(str1.split(" "))  # Output: ['My', 'name', 'is', 'Suraj']
```