# Unit-4: Collections

## Collections
The Python **Collections** module is defined as a container used to store collections of data (e.g., list, dictionary, set, tuple, etc.). It was introduced to improve the functionalities of the built-in collection containers. Python's collection module was first introduced in version 2.4.

---

## What is a List? How is a List Created?
### 1. Lists
- **List** is a built-in data type that stores a set of values.
- Data stored in a list can be **non-homogeneous**, meaning it can contain elements of different types (e.g., integers, floats, strings).
- Lists **allow duplicate data**.
- Lists are represented using **square brackets** `[]`.
- Lists are **ordered** (follow indexing).
- Lists are **mutable**, meaning their values can be updated.

#### Example:
```python
marks = []  # Empty list
marks = [89, 67, 67, 98, 96, 87]  # List with values
print(marks)
```

### Accessing List Elements
```python
print(marks[3])  # Accessing the 4th element
print(marks[-2]) # Accessing the second last element
```

### Mutable Nature of Lists
```python
marks[4] = 77  # Updating the 5th element
print(marks)
```

### List Slicing
List slicing allows accessing a specific portion or subset of a list.

#### Syntax:
`list_name[start_index:end_index]` (The ending index is not included)

#### Example:
```python
print(marks[1:5])  # From index 1 to 4
print(marks[:4])   # From index 0 to 3
print(marks[1:])   # From index 1 to the end
print(marks[-5:-2])
```

### List Methods
```python
details = [12, 87, 56, 98, 90, 67, 56]
```

1. **`len()`**: Returns the length of the list.
   ```python
   print(len(details))
   ```

2. **`append()`**: Adds an element at the end of the list.
   ```python
   details.append(456)
   print(details)
   ```

3. **`insert()`**: Adds an element at the specified index.
   ```python
   details.insert(1, 1234)
   print(details)
   ```

4. **`sort()`**: Sorts the list in ascending order.
   ```python
   details.sort()
   print(details)
   ```

   **Descending Order**:
   ```python
   details.sort(reverse=True)
   print(details)
   ```

5. **`reverse()`**: Reverses the list.
   ```python
   details.reverse()
   print(details)
   ```

6. **`remove()`**: Removes the first occurrence of a specified element.
   ```python
   details.remove(56)
   print(details)
   ```

7. **`pop()`**: Removes the element at the specified index.
   ```python
   details.pop(4)
   print(details)
   ```

---

## 2. Tuples
- **Tuple** is one of the four built-in data types in Python used to store collections of data.
- Tuples are **immutable** (unchangeable).
- Tuples are **ordered** and allow duplicate elements.
- Tuples are represented using **parentheses** `()`.

### Creating Tuples
```python
tup = ()  # Empty tuple
print(type(tup))
tup1 = (12,)  # Tuple with one element
print(type(tup1))
```

#### Example:
```python
goods = ("apple", "orange", 23, 43)
print(goods[1])
print(type(goods))
```

### Accessing Tuple Items
```python
print(goods[1])        # By index
print(goods[-3])       # By reverse index
```

### Nested Tuples
```python
marks = (23, 45, 67, (23, 23, 3), 23, 13)
print(marks[3][1])
```

### Tuple Slicing
```python
print(marks[1:3])
```

### Tuple Methods
1. **`index()`**: Returns the index of an element.
   ```python
   nums = (45, 67, 89, 98, 89, 89, 87, 89)
   print(nums.index(89))
   ```

2. **`count()`**: Counts the occurrence of an element.
   ```python
   print(nums.count(89))
   ```

---

## 3. Dictionaries
- **Dictionaries** store data in **key-value** pairs: `"key": value`.
- Dictionaries are **unordered**, **mutable**, and do not allow duplicate keys.
- Dictionaries can store lists and tuples.

#### Example:
```python
result = {
    "name": "Suraj",
    "rollNo": 21,
    "cgpa": 9.5,
    "is_Adult": True,
    "marks": [87, 99, 98, 96, 95],
    "subject": ("DBMS", "OOPs", "Java", "Python")
}
```

### Accessing Dictionary Elements
```python
print(result["name"])
print(result["marks"][1])
print(result["subject"][1])
```

### Dictionary Methods
1. **`.keys()`**: Returns all keys.
   ```python
   print(result.keys())
   ```

2. **`.values()`**: Returns all values.
   ```python
   print(result.values())
   ```

3. **`.items()`**: Returns all key-value pairs as tuples.
   ```python
   print(result.items())
   ```

4. **`.get(key)`**: Returns the value of a key.
   ```python
   print(result.get("rollNo"))
   ```

5. **`.update()`**: Updates or adds a key-value pair.
   ```python
   result.update({"City": "Patna"})
   print(result)
   ```

---

## 4. Sets
- Sets are **mutable**, but their elements are **immutable**.
- Sets store **unique values** (no duplicates).
- Sets are **unordered**.
- Sets are represented using **curly braces** `{}`.

#### Creating a Set
```python
marks = {23, 45, 67, 78, 78, 45}
print(marks)  # Duplicates are removed
```

### Set Methods
1. **`add()`**: Adds an element to the set.
   ```python
   marks.add(92)
   print(marks)
   ```

2. **`remove()`**: Removes a specified element.
   ```python
   marks.remove(23)
   print(marks)
   ```

3. **`clear()`**: Empties the set.
   ```python
   marks.clear()
   print(len(marks))
   ```

4. **`pop()`**: Removes a random element.
   ```python
   print(marks.pop())
   ```

---

## Sorting Dictionaries
Sorting allows efficient analysis of data structures. A dictionary is faster for searching compared to a list.

### Ways to Sort a Dictionary:
1. **Sorting by Keys**
   ```python
   print(sorted(names.keys()))
   ```

2. **Sorting by Values**
   ```python
   print(sorted(names.values()))
   ```

3. **Sorting by Items**
   ```python
   print(sorted(names.items()))
   ```

---

## Copying Collections
The `copy` module provides methods for creating copies of collections.

### Types of Copies:
1. **Deep Copy**: Creates a copy where changes do not affect the original object.
   ```python
   copy.deepcopy(x)
   ```

2. **Shallow Copy**: Creates a reference to elements of the original object, so changes affect the original object.
   ```python
   copy.copy(x)
   ```
