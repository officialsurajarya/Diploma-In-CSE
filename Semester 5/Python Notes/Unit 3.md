# Unit 03

## Topic 1: Indentation Requirements in Python
Python indentation is a way of telling a Python interpreter that a group of statements belongs to a particular block of code. The default indentation in Python is four spaces, but you can use any number of spaces as long as you maintain consistency within the block.

---

## Topic 2: Conditional Statements in Python
Conditional statements in Python are used to execute specific blocks of code based on the truth value of a condition.

### 1. `if` Statement
The `if` statement executes a block of code if the condition evaluates to `True`.

```python
num = int(input("Enter a number: "))
if num == 5:
    print("Hello")
```

### 2. `if-else` Statement
The `if-else` statement executes one block of code if the condition is `True`, otherwise, it executes another block.

#### Syntax
```python
if condition:
    # body of if
else:
    # body of else
```

#### Example
```python
n = int(input("Enter a number: "))
if n % 2 == 0:
    print(n, "is an even number")
else:
    print(n, "is an odd number")
```

### 3. `elif` Statement
The `elif` keyword is used for checking multiple conditions.

#### Syntax
```python
if condition1:
    # code if condition1 is true
elif condition2:
    # code if condition2 is true
else:
    # code if all conditions are false
```

#### Example
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))
if a > b and a > c:
    print(a, "is the greatest")
elif b > a and b > c:
    print(b, "is the greatest")
else:
    print(c, "is the greatest")
```

---

## Topic 3: Looping
Looping means repeating something over and over until a particular condition is satisfied. The loop terminates when the condition becomes false.

### Types of Loops in Python
1. **While Loop**
   Executes a block of statements repeatedly until the condition becomes false.

#### Syntax
```python
initialization
while condition:
    # body
    update
```

#### Example: Print numbers from 1 to 10
```python
i = 1
while i <= 10:
    print(i)
    i += 1
```

2. **For Loop**
   Used for iterating over a sequence (e.g., list, tuple, string, or range).

#### Syntax
```python
for variable in range(start, stop, step):
    # body
```

#### Example: Print numbers from 1 to 10
```python
for i in range(1, 11):
    print(i)
```

---

## Examples

### 1. Print the table of a number entered by the user
#### Using `while` loop
```python
n = int(input("Enter a number: "))
i = 1
while i <= 10:
    print(n * i, end=" ")
    i += 1
```

#### Using `for` loop
```python
n = int(input("Enter a number: "))
for i in range(1, 11):
    print(n * i, end=" ")
```

### 2. Reverse a number
#### Using `while` loop
```python
num = int(input("Enter a number: "))  # e.g., 164
rev = 0
while num != 0:
    rem = num % 10
    rev = rev * 10 + rem
    num = num // 10
print(rev)
```

#### Using string manipulation
```python
name = input("Enter a number: ")
print(name[::-1])
```

### 3. Fibonacci Series (First 10 Numbers)
```python
a, b = 0, 1
print(a, b, end=" ")
for _ in range(8):
    c = a + b
    print(c, end=" ")
    a, b = b, c
```

### 4. Check if a Number is Palindrome
```python
n = int(input("Enter a number: "))
temp = n
rev = 0
while n != 0:
    rem = n % 10
    rev = rev * 10 + rem
    n = n // 10
if temp == rev:
    print("Number is palindrome")
else:
    print("Number is not palindrome")
```

### 5. Check if a Number is Armstrong
```python
n = int(input("Enter a number: "))
temp = n
sum = 0
while n != 0:
    rem = n % 10
    sum += rem ** 3
    n = n // 10
if temp == sum:
    print("Number is Armstrong")
else:
    print("Number is not Armstrong")
```

---

## Topic 4: `break` and `continue`

### 1. `break`
Terminates the loop immediately when encountered.

#### Example: Using `while` loop
```python
i = 1
while i <= 10:
    if i == 6:
        break
    print(i)
    i += 1
```

#### Example: Using `for` loop
```python
for i in range(1, 11):
    if i == 5:
        break
    print(i)
```

### 2. `continue`
Skips the current iteration and proceeds to the next.

#### Example
```python
for i in range(1, 11):
    if i == 5:
        continue
    print(i)
```

---

## Prime Number Check
A prime number is divisible only by itself and 1. Negative numbers, 0, and 1 are not prime.

```python
num = int(input("Enter a number: "))
if num > 1:
    for i in range(2, (num // 2) + 1):
        if num % i == 0:
            print(num, "is not a Prime Number")
            break
    else:
        print(num, "is a Prime Number")
else:
    print(num, "is not a Prime Number")
