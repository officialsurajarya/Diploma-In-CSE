# Unit 1: PHP Introduction

---

### **Introduction to PHP**

PHP (Hypertext Preprocessor) is a widely-used, open-source scripting language designed for web development. It can be embedded into HTML and is commonly used to build dynamic web pages and applications.

1. **How PHP Works**:
   - PHP is a **server-side scripting language**, meaning that it runs on the web server rather than in the user's browser.
   - When a user makes a request for a PHP page, the web server processes the PHP code and returns the result (usually HTML) to the user's browser.
   - **Flow**:
     - The browser sends a request to the server.
     - The server processes the PHP script.
     - The server returns the output (HTML) to the browser.
     - The browser displays the page to the user.

2. **The php.ini File**:
   - The `php.ini` file is the main configuration file for PHP.
   - It defines settings such as error reporting, file upload limits, session handling, and various other PHP runtime configurations.
   - **Example**: You can change the file upload size by modifying `upload_max_filesize` in the `php.ini` file.

---

### **Basic PHP Syntax**

PHP code is embedded within HTML and executed on the server. It starts with `<?php` and ends with `?>`.

```php
<?php
  echo "Hello, World!";
?>
```

- **PHP Tags**: The PHP code is enclosed in `<?php` and `?>` tags.
- **Statements**: PHP statements end with a semicolon (`;`).
- **Whitespace**: PHP is not sensitive to spaces, tabs, or line breaks, except in strings or keywords.

---

### **PHP Variables**

- **Definition**: Variables in PHP are denoted by a dollar sign (`$`) followed by the variable name.
- **Example**:
  ```php
  $name = "Suraj";
  $age = 21;
  ```
- **Data Types**:
  - PHP supports various data types, including strings, integers, floats, arrays, objects, and booleans.
  - PHP is loosely typed, so you don't need to declare a variable's type before using it.

---

### **PHP Operators**

1. **Arithmetic Operators**: Used for basic mathematical operations.
   - `+`, `-`, `*`, `/`, `%`

2. **Assignment Operators**: Used to assign values to variables.
   - `=`, `+=`, `-=`, `*=`, `/=`

3. **Comparison Operators**: Used to compare values.
   - `==`, `!=`, `>`, `<`, `>=`, `<=`

4. **Logical Operators**: Used for logical operations.
   - `&&`, `||`, `!`

5. **String Operators**:
   - `.` (concatenation) - combines two strings.
   - `.=`, appends to a string.

---

### **Decision Making in PHP**

PHP provides several conditional structures to control the flow of execution based on conditions:

1. **if Statement**:
   ```php
   if ($age >= 18) {
     echo "Adult";
   }
   ```

2. **if-else Statement**:
   ```php
   if ($age >= 18) {
     echo "Adult";
   } else {
     echo "Minor";
   }
   ```

3. **switch Statement**:
   ```php
   switch ($day) {
     case "Monday":
       echo "Start of the week";
       break;
     case "Friday":
       echo "End of the week";
       break;
     default:
       echo "Midweek";
   }
   ```

---

### **Loops in PHP**

Loops allow you to execute code repeatedly.

1. **while Loop**:
   ```php
   $i = 0;
   while ($i < 5) {
     echo $i;
     $i++;
   }
   ```

2. **for Loop**:
   ```php
   for ($i = 0; $i < 5; $i++) {
     echo $i;
   }
   ```

3. **foreach Loop** (used for arrays):
   ```php
   $arr = [1, 2, 3, 4];
   foreach ($arr as $value) {
     echo $value;
   }
   ```

---

### **Arrays in PHP**

- **Indexed Arrays**: Arrays with numeric indexes.
  ```php
  $fruits = ["Apple", "Banana", "Cherry"];
  ```

- **Associative Arrays**: Arrays with named keys.
  ```php
  $person = ["name" => "John", "age" => 30];
  ```

- **Multidimensional Arrays**: Arrays within arrays.
  ```php
  $matrix = [[1, 2], [3, 4]];
  ```

---

### **Strings in PHP**

1. **String Concatenation**:
   ```php
   $first_name = "John";
   $last_name = "Doe";
   $full_name = $first_name . " " . $last_name;
   ```

2. **String Functions**:
   - `strlen()`: Returns the length of a string.
   - `strpos()`: Finds the position of a substring.
   - `substr()`: Extracts a part of the string.

---

### **PHP OOPs Concept**

Object-Oriented Programming (OOP) allows for modular, reusable, and organized code. PHP supports OOP with the following concepts:

1. **Classes and Objects**:
   - **Class**: A blueprint for creating objects.
   - **Object**: An instance of a class.
   ```php
   class Car {
     public $color;
     function setColor($color) {
       $this->color = $color;
     }
   }
   $myCar = new Car();
   $myCar->setColor("Red");
   ```

2. **Inheritance**: Classes can inherit properties and methods from other classes.
   ```php
   class SportsCar extends Car {
     public $speed;
   }
   ```

3. **Polymorphism**: Same method can behave differently in different classes.
4. **Encapsulation**: Keeping data safe within a class and only accessible through methods.

---

### **PHP Forms (Form Handling, Validation)**

1. **Form Handling**:
   PHP is often used to collect and process data from HTML forms using the `GET` or `POST` methods.
   ```html
   <form method="POST" action="process.php">
     <input type="text" name="username">
     <input type="submit" value="Submit">
   </form>
   ```

2. **Form Validation**:
   PHP can be used to validate form data before processing.
   ```php
   if ($_SERVER["REQUEST_METHOD"] == "POST") {
     if (empty($_POST["username"])) {
       echo "Username is required.";
     }
   }
   ```

---

### **GET and POST Methods**

1. **GET Method**: Sends data as URL parameters (less secure, suitable for non-sensitive data).
   ```php
   $name = $_GET['name'];
   ```

2. **POST Method**: Sends data in the HTTP body (more secure, suitable for sensitive data).
   ```php
   $name = $_POST['name'];
   ```

---

### **PHP Functions**

- Functions in PHP allow you to group code into reusable blocks.
  ```php
  function greet($name) {
    return "Hello, " . $name;
  }
  echo greet("Suraj");
  ```

---

### **Introduction to Cookies**

- **Cookies** are small pieces of data stored on the client side (browser) that can be used to remember information between requests.

1. **Setting Cookies**:
   ```php
   setcookie("user", "John", time() + 3600);  // Expires in 1 hour
   ```

2. **Using Cookie Information**:
   ```php
   if (isset($_COOKIE['user'])) {
     echo "Welcome " . $_COOKIE['user'];
   }
   ```

---

### **Sessions in PHP**

1. **Creating Sessions**:
   PHP sessions store data on the server side. To start a session, you use `session_start()`.

   ```php
   session_start();
   $_SESSION['username'] = 'John';
   ```

2. **Timeout in Sessions**:
   You can set a session timeout by configuring the session parameters or using custom logic to track the session time and invalidate it after a certain period of inactivity.

