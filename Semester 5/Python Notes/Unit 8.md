
# UNIT-8 Input and Output

## Data Stream
A **data stream** refers to the continuous flow of data, often in real-time, as events occur. Data streams are useful for processing large datasets without loading everything into memory.

---

## Access Modes
Access modes determine how a file is opened and handled (e.g., read, write, append). The `open()` function in Python specifies the mode:

| Mode | Description                                |
|------|--------------------------------------------|
| `r`  | Opens the file for reading only.           |
| `r+` | Opens the file for both reading and writing.|
| `w`  | Opens the file for writing (overwrites).   |
| `w+` | Opens the file for writing and reading.    |
| `a`  | Opens the file for appending.              |
| `a+` | Opens the file for appending and reading.  |

---

## Reading Data from a File
To read data from a file, use the `open()` function with access mode `'r'`.

**Syntax:**
```python
open("File_Name", "Access_Mode")
```

**Example:**
```python
f = open("file1.txt", "r")
print(f.read())
```

---

## Writing Data to a File
To write data to a file, use the `open()` function with access modes `'a'` (append) or `'w'` (write).

### Example 1: Appending Data
```python
f = open("file1.txt", "a")
f.write("Good to see you")
f.close()

# Open and read the file after appending:
f = open("file1.txt", "r")
print(f.read())
```

### Example 2: Overwriting Data
```python
f = open("demofile3.txt", "w")
f.write("Good to see you")
f.close()

# Open and read the file after overwriting:
f = open("demofile3.txt", "r")
print(f.read())
```

---

## Additional File Methods
Python provides several methods for handling files, such as:
- `readline()`: Reads a single line from the file.
- `write()`: Writes data to a file.
- `seek(offset)`: Changes the current file position.

---

## Using Pipes as Data Streams
Pipes enable **inter-process communication (IPC)**, where one process sends data to another.

- **Write End**: Data is sent into the pipe.
- **Read End**: Data is retrieved from the pipe.

Example:
```python
import os

read_end, write_end = os.pipe()

os.write(write_end, b"Hello from pipe!")
data = os.read(read_end, 100)
print(data.decode())  # Output: Hello from pipe!
```

---

## Handling I/O Exceptions
Handling I/O exceptions is crucial for managing errors, such as missing files or permission issues. Use `try-except` blocks for error handling.

### Example: Handling I/O Errors
```python
try:
    f = open("file3.txt", "r")
    print(f.read())
except IOError:
    print("The file you are trying to access does not exist")
```
If the file `file3.txt` does not exist, the output will be:
```
The file you are trying to access does not exist
```