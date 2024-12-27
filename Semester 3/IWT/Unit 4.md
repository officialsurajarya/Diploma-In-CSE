# Unit 4: JavaScript 

JavaScript is a programming language commonly used to create interactive effects within web browsers. It is often used for client-side scripting, making web pages dynamic and interactive.

Here’s a breakdown of the topics related to **JavaScript**:

---

### **1. JavaScript Introduction**
- **JavaScript** is a lightweight, interpreted programming language that is primarily used for enhancing web pages with interactive and dynamic features.
- It runs on the **client-side** (in the browser) but can also run on the server-side (using Node.js).
- JavaScript allows for changes in the content of the web page without reloading, such as:
  - Validating forms
  - Creating interactive maps
  - Handling animations and event responses

---

### **2. Variables in JavaScript**
- Variables are used to store data that can be referenced or manipulated later in the program.
- **Declaration**: Variables in JavaScript can be declared using three keywords: `var`, `let`, and `const`.
  - **var**: Declares a variable with function-scoped or globally-scoped. (Older syntax)
  - **let**: Declares a block-scoped variable, more modern and preferred for use in most cases.
  - **const**: Declares a block-scoped variable that cannot be reassigned after initialization.

  Example:
  ```javascript
  var name = "John";  // var declaration
  let age = 30;       // let declaration
  const country = "India"; // const declaration
  ```

---

### **3. Data Types in JavaScript**
JavaScript supports various data types:
1. **Primitive Data Types**:
   - **Number**: Represents both integer and floating-point numbers.
     ```javascript
     let num = 5;
     let price = 19.99;
     ```
   - **String**: Represents sequences of characters.
     ```javascript
     let name = "Alice";
     ```
   - **Boolean**: Represents true or false values.
     ```javascript
     let isActive = true;
     ```
   - **Undefined**: A variable that has been declared but not assigned a value.
     ```javascript
     let x;
     console.log(x);  // undefined
     ```
   - **Null**: Represents the intentional absence of any object value.
     ```javascript
     let car = null;
     ```
   - **Symbol**: A unique and immutable data type used for creating unique identifiers for objects (ES6+).
   - **BigInt**: Used for large integers beyond the range of the Number type.

2. **Non-Primitive Data Types**:
   - **Object**: A collection of key-value pairs (similar to dictionaries or hashmaps).
     ```javascript
     let person = {
       name: "John",
       age: 30,
       city: "New York"
     };
     ```

---

### **4. Operators in JavaScript**
Operators are used to perform operations on variables and values.

- **Arithmetic Operators**: Perform mathematical calculations.
  ```javascript
  let sum = 5 + 3; // Addition
  let diff = 10 - 2; // Subtraction
  let product = 4 * 2; // Multiplication
  let quotient = 10 / 2; // Division
  let remainder = 10 % 3; // Modulus (remainder)
  ```

- **Comparison Operators**: Compare values.
  ```javascript
  let isEqual = 5 == 5;  // Equal to (checks value)
  let isIdentical = 5 === "5"; // Identical (checks value and type)
  let isGreater = 10 > 5;  // Greater than
  let isLess = 3 < 5;  // Less than
  ```

- **Logical Operators**: Used to combine multiple boolean expressions.
  ```javascript
  let and = true && false;  // AND
  let or = true || false;   // OR
  let not = !true;  // NOT
  ```

- **Assignment Operators**: Assign values to variables.
  ```javascript
  let x = 10;    // Simple assignment
  x += 5;        // Add and assign
  x -= 3;        // Subtract and assign
  ```

- **Ternary Operator**: A shorthand for `if-else` condition.
  ```javascript
  let result = (10 > 5) ? "Yes" : "No";  // If true, "Yes"; else, "No"
  ```

---

### **5. Control Flow in JavaScript**

#### **a. if-else Statement**
- Used to execute different blocks of code based on a condition.
  ```javascript
  let age = 20;
  if (age >= 18) {
    console.log("Adult");
  } else {
    console.log("Not an Adult");
  }
  ```

#### **b. for Loop**
- Used to repeat a block of code a specified number of times.
  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i); // Outputs 0, 1, 2, 3, 4
  }
  ```

#### **c. while Loop**
- Repeats a block of code while the specified condition is true.
  ```javascript
  let count = 0;
  while (count < 5) {
    console.log(count);
    count++;
  }
  ```

#### **d. do-while Loop**
- Similar to the `while` loop, but guarantees the code block runs at least once before checking the condition.
  ```javascript
  let num = 0;
  do {
    console.log(num);
    num++;
  } while (num < 5);
  ```

---

### **6. Declaring Functions in JavaScript**
Functions allow us to encapsulate code into reusable blocks.

#### **a. Function Declaration**
```javascript
function greet(name) {
  console.log("Hello, " + name);
}
greet("John");  // Output: Hello, John
```

#### **b. Function Expression**
A function can also be assigned to a variable.
```javascript
const sayGoodbye = function() {
  console.log("Goodbye!");
};
sayGoodbye();  // Output: Goodbye!
```

#### **c. Arrow Functions (ES6)**
A shorter syntax for writing functions.
```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Output: 5
```

---

### **7. Calling Functions with Parameters**
Functions can accept parameters to perform actions with dynamic data.
```javascript
function sum(a, b) {
  return a + b;
}
console.log(sum(10, 20));  // Output: 30
```

---

### **8. Adding JavaScript to Web Documents**
JavaScript can be added to HTML documents in various ways:
1. **Inline**: Directly within the HTML element using the `onclick` or other event attributes.
   ```html
   <button onclick="alert('Hello World!')">Click Me</button>
   ```

2. **Internal**: Using a `<script>` tag in the `<head>` or `<body>` section.
   ```html
   <script>
     console.log("JavaScript is working");
   </script>
   ```

3. **External**: Linking to an external JavaScript file using the `src` attribute.
   ```html
   <script src="script.js"></script>
   ```

---

### **9. JavaScript Objects**
Objects are collections of key-value pairs, used to store multiple related data.
```javascript
let person = {
  name: "Alice",
  age: 25,
  greet: function() {
    console.log("Hello, " + this.name);
  }
};
console.log(person.name);  // Output: Alice
person.greet();  // Output: Hello, Alice
```

---

### **10. Document Object Model (DOM)**
The DOM represents the structure of an HTML document as a tree of objects. JavaScript can interact with the DOM to modify HTML and CSS.

- **Accessing Elements**:
  ```javascript
  let element = document.getElementById("myElement");
  console.log(element.innerHTML);
  ```

- **Changing Content**:
  ```javascript
  document.getElementById("demo").innerHTML = "New content";
  ```

- **Manipulating Styles**:
  ```javascript
  document.getElementById("myElement").style.color = "red";
  ```

---

### **11. HTML Events and Calling JavaScript Functions on Events**
Events in JavaScript occur when a user interacts with HTML elements (clicking, typing, etc.). JavaScript can respond to these events.

- **Common Events**: `onclick`, `onmouseover`, `onload`, `onchange`, etc.
  ```html
  <button onclick="alert('Button clicked!')">Click me</button>
  ```

- **Event Listeners**: More flexible way of handling events.
  ```javascript
  document.getElementById("myButton").addEventListener("click", function() {
    alert("Button clicked!");
  });
  ```

---
