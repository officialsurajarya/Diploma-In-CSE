# UNIT-7 Exceptions

## Errors in Python
Errors are issues in a program that prevent it from executing properly. Errors are also called **bugs** or **faults** and can be caused by user mistakes or programming errors. They can be categorized into three types:

---

### 1. **Syntax Errors**
These occur when the code violates the syntax rules of the Python language. Detected during code parsing, syntax errors prevent the program from running.

#### Examples:
1. Missing parentheses:
   ```python
   print("Hello"  # SyntaxError
   ```
2. Missing colon:
   ```python
   if a > 0
       print("A is positive")  # SyntaxError
   ```

---

### 2. **Runtime Errors**
These occur when the syntax of the code is correct but an error arises during program execution. Common causes include invalid input, division by zero, or undefined variables.

#### Examples:
1. **ValueError**:
   ```python
   a = int(input("Enter a number: "))  # RuntimeError if input is non-numeric
   ```
2. **ZeroDivisionError**:
   ```python
   a = 12
   b = 0
   c = a / b  # ZeroDivisionError
   ```

---

### 3. **Logical Errors**
Logical errors occur when the program runs without crashing but produces incorrect results due to flawed logic or misinterpretation of requirements.

#### Example:
```python
a = 5
b = 10
avg = a + b / 2  # Incorrect logic for average
print(avg)  # Logical error
```

---

## Exceptions
An **exception** is an unexpected event that occurs during program execution, disrupting its normal flow. Unlike syntax errors, exceptions occur at runtime.

#### Example:
```python
x = 5
y = "hello"
z = x + y  # TypeError
```

---

## Exception Handling
Python provides a mechanism to handle exceptions gracefully using `try` and `except` blocks.

### Syntax:
```python
try:
    # Code that may raise an exception
except ExceptionType:
    # Code to handle the exception
```

### Example:
```python
try:
    x = 5
    y = "hello"
    z = x + y
except TypeError:
    print("Error: Cannot concatenate int and string")
```

---

## Exception Hierarchy
Python organizes exceptions in a hierarchical structure, with `BaseException` as the root class. Common exception classes include:
- `ArithmeticError`
  - `ZeroDivisionError`
- `EnvironmentError`
  - `OSError`
  - `IOError`

Understanding this hierarchy helps in targeting specific exceptions effectively.

---

## User-Defined Exceptions
User-defined exceptions allow programmers to create custom error types for specific scenarios.

### 1. Using `raise` Keyword
The `raise` statement explicitly triggers an exception. You can use it to create and raise a custom exception.

#### Syntax:
```python
raise ExceptionType("Error message")
```

#### Example:
```python
a = 12
b = 0
if b == 0:
    raise ZeroDivisionError("b cannot be zero")
```

### 2. Using `assert` Keyword
The `assert` statement checks a condition, and if it evaluates to `False`, it raises an `AssertionError`.

#### Syntax:
```python
assert condition, "Error message"
```

#### Example:
```python
def divide(a, b):
    assert b != 0, "Division by zero is not allowed!"
    return a / b

print(divide(12, 2))  # Works fine
print(divide(12, 0))  # Raises AssertionError
```