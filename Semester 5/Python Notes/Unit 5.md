# Unit-5 Functions

## Functions

A **function** is a block of code that runs only when it is called. You can pass data, known as parameters, into a function. A function contains three components:

1. **Declaration**: A function is declared in Python using the `def` keyword.  
   **Syntax:**  
   ```python
   def Function_Name():
   ```
2. **Definition**: The body of the function, which contains the code to execute.
3. **Calling**: Invoking the function to execute its block of code.

### Example:
```python
def add(a, b):
    print(a + b)
add(12, 13)
```

### Filter Functions
The `filter` function returns an iterator where items are filtered through a function to test if they are accepted or not.

**Syntax:**  
```python
filter(function, iterable)
```

**Example:**
```python
ages = [5, 12, 17, 34, 56, 23, 11]
def my_Fun(x):
    return x >= 18

adults = filter(my_Fun, ages)
for x in adults:
    print(x, end=" ")
```

---

## Function Parameters in Python

### 1. Default Parameters
Default arguments are values assigned to a function parameter when no argument is provided during a function call. They are also known as optional arguments.

**Example:**
```python
def myFun(name="Suraj", age=21):
    print("My name is", name, "and my age is", age)

myFun()
myFun("Muskan", 19)
```

### 2. Keyword Parameters
Keyword parameters allow passing arguments to a function using parameter names instead of their order.

**Example:**
```python
def KeyArg(int, float, str):
    print("int:", int)
    print("float:", float)
    print("String:", str)

KeyArg(10, 34.23, "Hello")
KeyArg(float=2.8, int=20, str="G")
```

### 3. Variable Number of Parameters
A function can accept a variable number of arguments by using `*` before the parameter name in the function definition.

**Example:**
```python
def MultiArg(*argTuple):
    print(argTuple)

MultiArg(5, 10, "Hello", "Suraj", True)
```

---

## Function Documentation
Function documentation helps users understand what a function does and how to use it. It is provided using docstrings, which are enclosed in triple quotes (`""" """` or `''' '''`).

**Example:**
```python
def my_function(food):
    """
    Prints each item in the food list.
    """
    for x in food:
        print(x)

fruits = ["apple", "banana", "cherry"]
my_function(fruits)
```

---

## Scope in Python
A variable is only available within the region it is created. This is called scope. There are two types:

### 1. Local Scope
Variables created inside a function belong to the local scope of that function and can only be used inside it.

**Example:**
```python
def myfunc():
    x = 300  # Local Variable
    print(x)

myfunc()
```

### 2. Global Scope
Variables created in the main body of Python code are global and can be accessed from any function.

**Example:**
```python
x = 300
def myfunc():
    print(x)

myfunc()
print(x)
```

---

## First-Class Citizens
A first-class citizen supports all operations generally available to other entities. These operations include:

1. Passing as arguments
2. Returning values from functions
3. Conditional modifications
4. Value assignments

---

## `map()` Function
The `map` function executes a specified function for each item in an iterable. The item is passed as a parameter.

**Syntax:**  
```python
map(function, iterable)
```

**Examples:**
1. Square numbers:
   ```python
   numbers = [1, 2, 3, 4]
   def square(num):
       return num * num

   squared_Num = map(square, numbers)
   result = list(squared_Num)
   print(result)
   ```

2. Convert strings to integers:
   ```python
   list1 = ['12', '34', '65', '22']
   list2 = map(int, list1)
   print(list(list2))
   ```

---

## `lambda` (Anonymous) Functions
Lambda functions are small, anonymous functions that can take any number of arguments but have only one expression.

**Syntax:**  
```python
lambda arguments: expression
```

**Examples:**
```python
anony = lambda a, b: a < b
print(anony(5, 4))
print(anony(4, 5))

x = lambda c, d: c * d
print(x(2, 3))
```

---

## Inner Functions
A function defined inside another function is known as an inner or nested function. Nested functions can access variables of the enclosing scope.

**Example:**
```python
def greeting(first, last):
    # nested helper function
    def getFullName():
        return first + " " + last

    print("Hi, " + getFullName() + "!")

greeting('Steven', 'Larson')
```

---

## Recursion in Python
A function that calls itself repeatedly until a condition is met is called a recursive function. It is composed of:

1. **Base Case**: Terminates the recursion.
2. **Recursive Case**: Keeps calling the function.

**Examples:**

1. Print numbers from n to 1:
   ```python
   def revNum(n):
       if n == 0:
           return
       print(n)
       revNum(n - 1)

   revNum(5)
   ```

2. Calculate factorial:
   ```python
   def fact(n):
       if n == 0 or n == 1:
           return 1
       else:
           return n * fact(n - 1)

   print(fact(5))
   ```