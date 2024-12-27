# Unit 2: Language Constructs in Java

1. **Variables, Types, and Type Declarations:**
   - **Variable:** A named storage location that can hold a value of a specific data type. The value of a variable can change during the execution of a program.
   - **Types:** Every variable in Java must be declared with a specific data type. The data type defines the kind of data the variable can hold (e.g., integers, floats, characters, etc.).
   - **Type Declarations:** When you declare a variable, you specify its type and name. For example:  
     ```java
     int age;  // Declare an integer variable named age
     String name;  // Declare a String variable named name
     ```

2. **Data Types:**
   - **Integer:** Used to store whole numbers (positive or negative) without decimals.  
     Example: `int x = 5;`
   - **Floating-point types:** Used to store decimal numbers. There are two types:
     - `float`: Stores single-precision 32-bit floating point numbers.  
       Example: `float pi = 3.14f;`
     - `double`: Stores double-precision 64-bit floating point numbers.  
       Example: `double e = 2.71828;`
   - **Character:** Used to store single characters. A character is enclosed in single quotes.  
     Example: `char grade = 'A';`
   - **Boolean:** Used to store true or false values.  
     Example: `boolean isActive = true;`

3. **Operators:**
   - **Arithmetic Operators:** Used to perform basic arithmetic operations.
     - `+`, `-`, `*`, `/`, `%` (addition, subtraction, multiplication, division, modulus)
   - **Relational Operators:** Used to compare two values.
     - `==`, `!=`, `<`, `>`, `<=`, `>=` (equal to, not equal to, less than, greater than, less than or equal to, greater than or equal to)
   - **Logical Operators:** Used for logical operations.
     - `&&` (AND), `||` (OR), `!` (NOT)
   - **Assignment Operators:** Used to assign values to variables.
     - `=`, `+=`, `-=`, `*=`, `/=`, `%=` (simple assignment, increment, decrement, etc.)
   - **Unary Operators:** Used with a single operand.
     - `++`, `--` (increment, decrement), `+` (positive), `-` (negative), `!` (logical NOT)

4. **Iteration and Jump Statements:**
   - **Iteration (Loops):** Used to execute a block of code multiple times.
     - **For Loop:** A loop that runs a specific number of times.
       ```java
       for (int i = 0; i < 5; i++) {
           System.out.println(i);  // Output: 0 1 2 3 4
       }
       ```
     - **While Loop:** A loop that runs as long as the specified condition is true.
       ```java
       int i = 0;
       while (i < 5) {
           System.out.println(i);
           i++;
       }
       ```
     - **Do-While Loop:** A loop that runs at least once, then continues while the condition is true.
       ```java
       int i = 0;
       do {
           System.out.println(i);
           i++;
       } while (i < 5);
       ```
   - **Jump Statements:** Used to control the flow of loops or code execution.
     - `break`: Exits the current loop or switch statement.
     - `continue`: Skips the current iteration of a loop and continues with the next iteration.

5. **Conditional Statements:**
   - **If-Else Clause:** Used for decision-making. If the condition is true, the first block executes; otherwise, the else block executes.
     ```java
     if (x > 10) {
         System.out.println("x is greater than 10");
     } else {
         System.out.println("x is less than or equal to 10");
     }
     ```
   - **Conditional Expressions (Ternary Operator):** A shorthand for `if-else` statements.  
     Syntax: `condition ? expression1 : expression2;`
     ```java
     int max = (a > b) ? a : b;
     ```

6. **Input using the Scanner Class:**
   - The `Scanner` class is used to get input from the user.
     ```java
     import java.util.Scanner;
     
     Scanner sc = new Scanner(System.in);
     System.out.print("Enter your name: ");
     String name = sc.nextLine();
     System.out.println("Hello, " + name);
     ```

7. **Output Statements:**
   - **System.out.println()**: Prints a message with a newline at the end.
     ```java
     System.out.println("Hello, World!");
     ```
   - **System.out.print()**: Prints a message without a newline at the end.
     ```java
     System.out.print("Hello ");
     System.out.print("World!");
     ```

8. **Switch-Case:**
   - A control statement used to execute one of many possible code blocks based on the value of a variable.
     ```java
     int day = 3;
     switch (day) {
         case 1:
             System.out.println("Monday");
             break;
         case 2:
             System.out.println("Tuesday");
             break;
         case 3:
             System.out.println("Wednesday");
             break;
         default:
             System.out.println("Invalid day");
     }
     ```

9. **Arrays:**
   - An array is a collection of similar data items stored at contiguous memory locations.  
     Example:
     ```java
     int[] numbers = {1, 2, 3, 4, 5};
     System.out.println(numbers[0]);  // Output: 1
     ```

10. **Methods:**
    - Methods are blocks of code that perform a specific task and can be called to execute from other parts of the program.
      - **Method Declaration:**
        ```java
        returnType methodName(parameters) {
            // Method body
        }
        ```
      - **Example of Method Declaration and Calling:**
        ```java
        public static int add(int a, int b) {
            return a + b;
        }

        public static void main(String[] args) {
            int result = add(5, 3);
            System.out.println(result);  // Output: 8
        }
        ```

In summary, these Java language constructs provide the foundational building blocks for writing and controlling the flow of programs, from variables and operators to loops and conditionals. Understanding them is essential for writing effective and efficient Java programs.