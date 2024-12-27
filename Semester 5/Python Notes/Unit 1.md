# Unit 1: Introduction to Python

---

## **1. Brief History of Python**
- Python was created by **Guido van Rossum** in the late 1980s and released in **1991**.
- It was developed as a successor to the ABC programming language to address issues of modularity and code readability.
- Python is named after the British comedy group **"Monty Python"**, not the snake.
- Python's design philosophy emphasizes **readability**, **simplicity**, and **flexibility**.

---

## **2. Python Versions**
- **Python 1.x**: Initial release in 1991 with basic features.
- **Python 2.x**: Introduced in 2000, added many improvements like garbage collection and Unicode support.
  - Last version: **2.7** (2010). Official support ended in 2020.
- **Python 3.x**: Released in 2008, made significant changes to improve performance and consistency.
  - It is the current version series, with regular updates.

---

## **3. Installing Python**
1. Download Python from the [official website](https://www.python.org/).
2. Choose the appropriate version for your operating system (Windows, macOS, Linux).
3. During installation:
   - Check the **"Add Python to PATH"** option.
   - Select the default or custom installation as per your needs.

---

## **4. Environment Variables**
- Environment variables allow the system to locate Python and its libraries.
- Key environment variable: **`PATH`**.
  - Ensure Python's installation directory and the `Scripts` folder are added to the `PATH`.
- On Windows:
  - Edit environment variables via **System Properties > Environment Variables**.
- On Linux/macOS:
  - Add Python paths to the shell configuration file (e.g., `.bashrc`, `.zshrc`).

---

## **5. Executing Python from the Command Line**
1. Open the terminal or command prompt.
2. Type `python` or `python3` to start the interactive Python shell.
3. To run a Python script:
   ```bash
   python script_name.py
   ```
4. Use `exit()` or `Ctrl+D` to exit the interactive shell.

---

## **6. IDLE**
- **IDLE (Integrated Development and Learning Environment)**:
  - Comes with the standard Python installation.
  - Features include an interactive shell, syntax highlighting, and a basic editor.
  - To start IDLE, search for "IDLE" or run `idle` in the terminal/command prompt.

---

## **7. Editing Python Files**
- Python files have the extension **`.py`**.
- Edit Python files using:
  - Basic text editors: Notepad (Windows), TextEdit (macOS), or Nano (Linux).
  - Advanced editors: VS Code, PyCharm, Sublime Text, etc.

---

## **8. Python Documentation**
- Official Python documentation is available at [docs.python.org](https://docs.python.org/).
- It provides comprehensive guides, library references, and tutorials.

---

## **9. Getting Help**
- Use the built-in **`help()`** function:
  ```python
  help(str)  # Displays documentation for the string type
  ```
- Use **`dir()`** to list the attributes of an object:
  ```python
  dir(list)  # Lists methods available for a list
  ```
- Visit Python communities like Stack Overflow or the official Python forums.

---

## **10. Dynamic Types**
- Python uses **dynamic typing**, meaning variables can change their type during execution.
  ```python
  x = 5       # x is an integer
  x = "Hello" # x is now a string
  ```

---

## **11. Python Reserved Words**
- Reserved words are keywords with predefined meanings in Python. They cannot be used as variable names.
- Examples:
  ```
  False, True, None, and, or, not, if, else, elif, while, for, def, return, break, continue, class, try, except
  ```
- View all reserved words:
  ```python
  import keyword
  print(keyword.kwlist)
  ```

---

## **12. Naming Conventions**
- Use meaningful variable names that describe their purpose.
- Follow **PEP 8** style guide:
  - Variables and functions: `snake_case` (e.g., `my_variable`)
  - Classes: `CamelCase` (e.g., `MyClass`)
  - Constants: `UPPER_CASE` (e.g., `PI = 3.14`)
- Avoid starting names with numbers or using special characters (`@, $, %`).