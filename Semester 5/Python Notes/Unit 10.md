# Unit-10 Regular Expression

## Regular Expression (RegEx)
A **Regular Expression (RegEx)** is a special sequence of characters used to define a search pattern for strings. Regular expressions are commonly used for string operations, such as searching, matching, and manipulating text.

### Key Points:
- **RegEx in Python**: To work with regular expressions in Python, you must import the `re` module.
- **re Module**: Python's `re` module provides functionalities for working with regular expressions.

---

## Match Function
The `match` function checks for a match at the beginning of the string. If the match is found, it returns a match object; otherwise, it returns `None`.

**Syntax:**  
```python
re.match(pattern, string)
```

---

## Matching a String
There are three ways to match a string:

1. **`re.match(pattern, string)`**: Checks if the pattern matches the start of the string.
2. **`re.search(pattern, string)`**: Searches the entire string for the pattern.
3. **`re.findall(pattern, string)`**: Returns all occurrences of the pattern in the string.

**Example:**
```python
import re

text = "There are 123 apples and 45 oranges."
print(re.match('re', text))  # Output: None
print(re.match('The', text))  # Output: <re.Match object; span=(0, 3), match='The'>

print(re.search('an', text))  # Output: <re.Match object; span=(21, 23), match='an'>
print(re.findall('es', text))  # Output: ['es', 'es']
```

---

## Special Characters in RegEx
Regular expressions use special characters, known as metacharacters, to define search criteria. Commonly used metacharacters include:

1. **Dot (.)**: Matches any single character except a newline.
2. **Caret (^)**: Matches the start of a string.
3. **Dollar Sign ($)**: Matches the end of a string.
4. **Asterisk (*)**: Matches zero or more occurrences of the preceding character.
5. **Plus (+)**: Matches one or more occurrences of the preceding character.
6. **Question Mark (?)**: Matches zero or one occurrence of the preceding character.
7. **Brackets ([])**: Matches any one of the characters inside the brackets.
8. **Parentheses (())**: Used for grouping and capturing.

**Example: Dot (.) Meta-character:**
```python
import re

text = "batsman"
print(re.match("b.t", text))  # Output: <re.Match object; span=(0, 3), match='bat'>

text = "ba\ntsman"
print(re.match("b.t", text))  # Output: None (dot doesn't match newline)
```

---

## Grouping in Python
Grouping allows you to create subpatterns within a regular expression using parentheses `()`. These groups can be accessed using `group()`.

**Example:**
```python
import re

text = "hello world Welcome"
pattern = "(hello) (world)"
match = re.search(pattern, text)
if match:
    print("Full match:", match.group(0))  # Full match: hello world
    print("Group 1:", match.group(1))    # Group 1: hello
    print("Group 2:", match.group(2))    # Group 2: world
```

---

## Splitting a String
You can split a string using the `re.split()` function. This is useful for splitting based on patterns or characters.

**Example:**
```python
import re

text = "This is a simple sentence"
result = re.split(" ", text)
print(result)  # Output: ['This', 'is', 'a', 'simple', 'sentence']
```