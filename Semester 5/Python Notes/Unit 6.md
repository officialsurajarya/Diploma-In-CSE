
# UNIT-6 Modules

## Python Modules
A **Python module** is a file containing Python definitions and statements. Modules can include:
- Functions
- Classes
- Variables

Modules allow code reusability and organization. There are two types of modules:

---

### 1. In-Built/Pre-Defined Modules
Python comes with many built-in modules for various purposes. To view all built-in modules, use:
```python
help("modules")
```

#### Example: Using Built-In Modules
```python
import math
import datetime

# Using datetime module
print(datetime.datetime.now())

# Using math module
r1 = math.sqrt(16)
r2 = math.pow(2, 3)
print(int(r1))  # Output: 4
print(r2)       # Output: 8.0
```

---

### 2. User-Defined Modules
User-defined modules are created by the programmer to simplify project-specific tasks.

#### Creating a Python Module
Write desired functions in a `.py` file, for example, `calc.py`:
```python
def add(a, b):
    return a + b

def sub(a, b):
    return a - b

def mul(a, b):
    return a * b

def div(a, b):
    return a / b
```

#### Importing a Module
You can use the `import` statement to use functions from the module:
```python
import calc

r = calc.add(23, 23)
print("Sum of two numbers:", r)
```

---

## Standard Modules
### 1. `sys` Module
The `sys` module provides functions and variables to manipulate the Python runtime environment. To use its features, import it:
```python
import sys
```

#### Key Features:
1. **`sys.version`:** Returns the Python version in use.
   ```python
   print(sys.version)  # Output: 3.12.5
   ```

2. **`sys.path`:** Displays the module search paths.
   ```python
   print(sys.path)
   ```

3. **`sys.exit`:** Terminates the program.
   ```python
   print("Hello world!")
   sys.exit()
   print("This won't execute.")
   ```

4. **`sys.argv`:** Stores command-line arguments (CLA) in a list.
   ```python
   for arg in sys.argv:
       print(arg)  # The first argument is the script name.
   ```

---

### 2. `math` Module
The `math` module provides mathematical constants and functions.

#### Example:
```python
import math

# Greatest Common Divisor (GCD)
r = math.gcd(12, 36)
print("GCD:", r)  # Output: 12

# Rounding functions
c = math.ceil(10.01)
f = math.floor(10.99)
print("Ceil:", c, "Floor:", f)  # Output: Ceil: 11 Floor: 10
```

---

### 3. `time` Module
The `time` module provides functionalities to work with time.

#### Example:
```python
import time

# `time()` function: Returns time in seconds since the epoch.
print(time.time())

# `ctime()` function: Returns the current date and time.
print(time.ctime())
```

---

### The `dir()` Function
The `dir()` function lists all properties and methods of an object. If no parameter is passed, it lists names in the current scope.

#### Example:
```python
# Attributes and methods of a list
print(dir(list))

# Names in the current scope
print(dir())
```