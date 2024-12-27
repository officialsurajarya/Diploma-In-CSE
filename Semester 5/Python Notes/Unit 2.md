# Python Unit-02

## Topic-1: Basic Syntax of Python

1. Python syntax refers to the set of rules that define the combinations of symbols that are considered correct.
2. These rules ensure that programs written in Python are structured and formatted, allowing the Python interpreter to understand and execute them correctly.

Example:
```python
print("Hello world!!!")
```

### Indentation in Python
Indentation refers to the use of whitespace at the beginning of a line of code.
- Indentation defines code blocks in Python.
- It is crucial because, unlike other programming languages that use braces `{}` to define blocks, Python relies on indentation.

Example:
```python
n = 12
if (n % 2 == 0):
    print(n, "is an even number")
print("Thank You")
```

## Topic-2: Python Variables
A variable is a container that stores different types of data. Unlike other programming languages, in Python, you do not need to declare a variable. Based on the assigned value, Python dynamically determines its type.

Example:
```python
a = 99.9
print(type(a))  # <class 'float'>

name = "John Dear"
print(type(name))  # <class 'str'>
```

## Topic-3: Identifiers
Identifiers are unique names assigned to variables, functions, and classes. They uniquely identify entities within a program.

### Rules for Forming Identifiers in Python:
1. The first character must be a letter or an underscore (`_`).
2. Digits can be part of an identifier but not as the first character.
3. Must not be a keyword.
4. Uppercase and lowercase letters are distinct (case-sensitive).

Examples:
- `myfile = 100` (valid)
- `Data+Rec` (invalid)
- `data_10_` (valid)

## Topic-4: Comments
Comments are used to explain the working of code. They have no impact on program execution. 

### Types of Comments in Python:
1. **Single-line comment**: Use the hash symbol (`#`).
   ```python
   # This is a single-line comment
   ```
2. **Multi-line comment**: Use triple quotes (`'''` or `"""`).
   ```python
   '''This is a
   multi-line comment.'''
   ```

## Topic-5: String Value
### Data Types
1. **Primitive**: `int`, `float`, `string`, `boolean`
2. **Non-Primitive**: `list`, `tuple`, `set`, `dictionary`

### String Value
In Python, a string is a primitive data type used to store textual data. Strings are sequences of characters enclosed in single (`'`) or double (`"`) quotes.

Example:
```python
name = "Tonydear"
print(name)
```

## Topic-6: String Methods
1. **`len()`**: Finds the length of a string.
   ```python
   print(len(name))
   ```
2. **`upper()`**: Converts all characters in a string to uppercase.
   ```python
   print(name.upper())
   ```
3. **`lower()`**: Converts all characters in a string to lowercase.
   ```python
   print(name.lower())
   ```
4. **`replace()`**: Updates the current string with a new string.
   ```python
   newName = name.replace("Suraj", "Arya")
   print(newName)
   ```
5. **`count()`**: Finds the number of occurrences of a character.
   ```python
   print(name.count('m'))
   print(name.count('m', 0, 6))
   ```

## Topic-7: The `format()` Method
This method provides functionality for efficient string substitution and data formatting.

### Ways to Use the `format()` Method:
1. **By Empty Placeholder**
   ```python
   details = "My name is {} and my age is {}".format(name, age)
   print(details)
   ```
2. **By Number Index**
   ```python
   print("My age is {1} and my name is {0}".format(name, age))
   ```
3. **By Name Index**
   ```python
   print("My name is {name} and my age is {age}".format(name="Suraj", age=21))
   ```

## Topic-8: Numeric Data Types in Python
In Python, numeric data types represent values that are numeric. 

### Types:
1. **`int`**: Example: `a = 12`
2. **`float`**: Example: `a = 12.34`

## Topic-9: Operators in Python
Operators are used to perform operations on variables and values.

### Types of Operators:
1. **Arithmetic Operators**:
   - Addition (`+`): `print(2 + 3)`  
   - Subtraction (`-`): `print(3 - 1)`
   - Multiplication (`*`): `print(2 * 3)`
   - Division (`/`): `print(5 / 2)`
   - Floor Division (`//`): `print(5 // 2)`
   - Exponentiation (`**`): `print(2 ** 3)`

2. **Assignment Operators**:
   ```python
   a = 5
   a += 5  # a = a + 5
   ```

3. **Relational/Comparison Operators**:
   ```python
   print(4 == 5)  # False
   print(3 != 4)  # True
   ```

4. **Logical Operators**:
   ```python
   print(5 > 2 and 3 < 5)  # True
   print(not(5 > 2))  # False
   ```

5. **Membership Operators**:
   ```python
   print('a' in "Suraj")
   print('x' not in "Suraj")
   ```

6. **Identity Operators**:
   ```python
   a = 12
   b = 23
   print(a is not b)
   ```

7. **Bitwise Operators**:
   ```python
   print(5 & 3)  # AND
   print(5 | 3)  # OR
   print(~5)  # NOT
   ```

## Topic-10: String Operators in Python
1. **`+`**: Concatenates two strings.
   ```python
   print("Hello" + " World")
   ```
2. **`*`**: Repeats the string.
   ```python
   print("Hello" * 3)
   ```
3. **`[]`**: Accesses a character by index.
   ```python
   print("Hello"[1])
   ```
4. **`[ : ]`**: Accesses a range of characters.
   ```python
   print("Hello"[1:4])
   ```
5. **`in`**: Checks if a substring exists in a string.
   ```python
   print("H" in "Hello")
   ```

## Topic-11: Conversion Functions
Python defines type conversion functions to directly convert one data type into another.

1. **Implicit Type Conversion**:
   ```python
   a = 12
   b = 12.6
   c = a + b
   print(c)  # float
   ```

2. **Explicit Type Conversion**:
   ```python
   a = '56'
   a = int(a)
   print(type(a))  # int
   ```

## Topic-12: Input and Output Functions
### `input()` Function
The `input()` function is used to take user input as a string.
```python
a = input("Enter a number: ")
print("The number is", a, "and its type is", type(a))
```

### `print()` Function
The `print()` function outputs a message to the console.

### Example Problems:
1. Write a program to input two numbers and print their sum.
   ```python
   num1 = int(input("Enter 1st number: "))
   num2 = int(input("Enter 2nd number: "))
   print("The sum is", num1 + num2)
   ```

2. Write a program to swap values between three variables.
   ```python
   a = int(input("Enter 1st value: "))
   b = int(input("Enter 2nd value: "))
   c = int(input("Enter 3rd value: "))
   b, c, a = a, b, c
   print("After swap: a=", a, "b=", b, "c=", c)