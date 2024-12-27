### **Unit 1: Hardware Organization of Computer System**

This unit covers the essential aspects of computer architecture, focusing on the organization and functioning of the **CPU**, **instruction formats**, **addressing modes**, and the design differences between **microprogrammed** and **hardwired** control. Additionally, it explores the characteristics of **CISC** and **RISC** architectures.

---

#### **1.1 CPU Organization**

The **CPU (Central Processing Unit)** is the brain of the computer, responsible for executing instructions. It consists of various components including registers, the arithmetic logic unit (ALU), and control units.

##### **1.1.1 General Register Organization**
- In a general register organization, multiple **general-purpose registers** are used to store operands and intermediate results during the execution of instructions.
- **Register Organization** allows for faster processing by reducing the need for memory access.
  
##### **1.1.2 Stack Organization**
- The stack organization uses a **stack** to store and retrieve data. It follows the **Last In, First Out (LIFO)** principle.
- The **stack pointer (SP)** register keeps track of the top of the stack.
- Stack-based instructions include **push** (store data on the stack) and **pop** (retrieve data from the stack).

##### **1.1.3 Instruction Formats**
- Instruction formats define the structure of the binary code that represents an instruction. These formats determine how the instruction's **opcode**, **operand**, and **addressing mode** are laid out.
  
  - **Three Address Instruction Format**:
    - Contains 3 addresses (two operands and one destination).
    - Example: `ADD R1, R2, R3` (R1 = R2 + R3).
  
  - **Two Address Instruction Format**:
    - Contains 2 addresses (one operand and one destination).
    - Example: `ADD R1, R2` (R1 = R1 + R2).
  
  - **One Address Instruction Format**:
    - Contains 1 address, the operand is implicit (often accumulator).
    - Example: `ADD R1` (Acc = Acc + R1).
  
  - **Zero Address Instruction Format (Stack-based)**:
    - No operand address; the operand is implicitly popped from the stack.
    - Example: `ADD` (Pop two operands from the stack, add them, and push the result back).

  - **RISC Instruction Format**:
    - Simple and consistent format, typically **fixed-length** instructions.
    - Example: `ADD R1, R2, R3` (R1 = R2 + R3) with no extra memory operands.

---

#### **1.2 CPU Design: Microprogrammed vs Hardwired Control**

##### **1.2.1 Microprogrammed Control**
- In a **microprogrammed control** unit, instructions are executed by sequences of micro-operations, which are stored in a **control memory** (microcode).
- **Microinstructions** specify control signals for each step in the execution of a machine-level instruction.
  
  - **Advantages**:
    - Easier to modify and extend.
    - More flexibility as changes can be made via the microcode.
  
  - **Disadvantages**:
    - Slower execution compared to hardwired control.
    - Complex hardware to manage microcode.

##### **1.2.2 Hardwired Control**
- In **hardwired control**, the control unit is designed using combinational logic to directly produce the required control signals for each machine-level instruction.
- It uses **decoding logic** and flip-flops to generate control signals in real-time for the operations.

  - **Advantages**:
    - Faster execution due to direct logic paths.
    - More efficient for fixed instruction sets.
  
  - **Disadvantages**:
    - Less flexible; changes require redesigning the control logic.
    - Harder to modify or extend.

---

#### **1.3 Reduced Instruction Set Computers (RISC)**

##### **1.3.1 CISC Characteristics**
- **CISC (Complex Instruction Set Computer)** systems have a rich set of instructions, which can perform complex operations with a single instruction.
  
  - **Characteristics of CISC**:
    - Large and complex instruction set with various addressing modes.
    - Instructions can have multiple operands.
    - Instructions are of variable length.
    - CISC processors often use multiple cycles per instruction.
  
  - **Example**: Intel x86 architecture.
  
##### **1.3.2 RISC Characteristics**
- **RISC (Reduced Instruction Set Computer)** systems focus on simplifying the instruction set to improve performance.
  
  - **Characteristics of RISC**:
    - Smaller instruction set with simple instructions, each typically taking one cycle to execute.
    - Fixed-length instructions.
    - Few addressing modes (usually register-based).
    - Emphasis on **load/store** architecture (memory access happens only through specific load and store instructions).
  
  - **Example**: ARM, MIPS.

---

#### **1.3.3 Comparison of CISC vs RISC**

| Feature                         | **CISC**                                 | **RISC**                                |
|----------------------------------|------------------------------------------|-----------------------------------------|
| **Instruction Set**              | Large and complex                        | Small and simple                        |
| **Instruction Length**           | Variable length                          | Fixed length                            |
| **Execution Time**               | Multiple cycles per instruction         | Typically one cycle per instruction     |
| **Addressing Modes**             | Many (including indirect)                | Few, usually register-based             |
| **Memory Access**                | Can access memory directly in instructions| Separate load/store instructions        |
| **Complexity**                   | Complex control logic                    | Simpler control logic                   |
| **Examples**                     | Intel x86, Motorola 68000                | ARM, MIPS                               |

---

### **Summary:**
- **CPU Organization** involves understanding various register and memory architectures such as **general register organization** and **stack organization**, as well as different **instruction formats** like three-address, two-address, and RISC instruction formats.
- **CPU Design** can either be **microprogrammed** or **hardwired**. The microprogrammed approach is more flexible but slower, while the hardwired approach is faster but less adaptable.
- **CISC** architectures have complex instructions with multiple operands and addressing modes, while **RISC** architectures focus on a simpler instruction set with fewer addressing modes for faster execution. Both have their advantages depending on application needs.