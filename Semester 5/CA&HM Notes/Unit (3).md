### **Unit 3: Arithmetic Operations**

This unit focuses on the fundamental arithmetic operations—**addition**, **subtraction**, **multiplication**, and **division**—and how they are performed at the hardware level using algorithms. The unit also discusses various methods for efficiently performing these operations.

---

#### **3.1 Introduction to Arithmetic Operations**

Arithmetic operations are basic computational tasks performed by the **ALU (Arithmetic Logic Unit)** of the **CPU**. These operations are fundamental to all computing tasks, from simple calculations to complex algorithms.

The efficiency of arithmetic operations is crucial for the performance of a computer system. At the hardware level, these operations are implemented through specific **algorithms** and optimized based on the architecture of the computer.

---

### **3.2 Addition Algorithm**

Addition is one of the most basic arithmetic operations. There are various methods used in computer systems to perform addition, such as **binary addition** and **two's complement addition**.

#### **Binary Addition (Unsigned Numbers)**
- **Step 1:** Add the corresponding bits starting from the least significant bit (rightmost).
- **Step 2:** If the sum is 1 or 0, write the result in the result column.
- **Step 3:** If the sum is 2 (1 + 1), carry over 1 to the next column.

##### Example:
```
  1011  (11 in decimal)
+ 1101  (13 in decimal)
---------
  11000  (24 in decimal)
```

#### **Two's Complement Addition (Signed Numbers)**
- The two's complement method is used to represent signed integers.
- For addition of signed numbers, the two's complement representation of negative numbers is used. The carry-out from the most significant bit is ignored in the result.

---

### **3.3 Subtraction Algorithm**

Subtraction of numbers is typically performed using the **two's complement** method. This avoids the need for a separate subtraction unit in the CPU.

#### **Two's Complement Subtraction (Signed Numbers)**
1. **Convert the number to be subtracted into its two's complement form**.
2. **Add the two's complement of the number to the other number** (as in addition).
3. If there is a carry-out, discard it.

##### Example:
```
  0101  (5 in decimal)
- 0011  (3 in decimal)
---------
  0010  (2 in decimal)
```
- Convert `3` to two's complement: `1111 1101` (8-bit representation).
- Add `5 + (-3)` using the two's complement of 3.

---

### **3.4 Multiplication Algorithm**

Multiplication algorithms are designed to simplify the process of multiplying two numbers. There are several methods used in computer systems, including **binary multiplication** and **Booth's algorithm** for signed numbers.

#### **Binary Multiplication (Unsigned Numbers)**
1. **Step 1:** Perform multiplication bit by bit starting from the least significant bit (rightmost).
2. **Step 2:** If the corresponding bit of the multiplier is 1, add the multiplicand to the result; otherwise, skip.
3. **Step 3:** Shift the result left and repeat until all bits are processed.

##### Example:
```
  101  (5 in decimal)
×  110  (6 in decimal)
---------
  000
+ 1010
+ 10100
---------
  11110  (30 in decimal)
```

#### **Booth's Algorithm (Signed Multiplication)**
- Booth's algorithm is used for multiplying signed numbers in **two's complement** representation. It reduces the number of operations by considering pairs of bits in the multiplier.
  
##### Steps:
1. Start with the multiplicand and multiplier in two's complement form.
2. Compare the bits in the multiplier and adjust the result according to the value (using 0, 1, or -1).
3. Continue until all bits in the multiplier are processed.

---

### **3.5 Division Algorithm**

Division can be broken into two categories: **unsigned division** and **signed division**. Both follow similar procedures but handle signs differently.

#### **Unsigned Division**
1. **Step 1:** Perform **long division** by dividing the dividend by the divisor bit by bit.
2. **Step 2:** For each step, determine the quotient and remainder.
3. **Step 3:** Repeat until the division process completes.

##### Example (Decimal):
```
Divide 13 by 3:
Quotient: 4, Remainder: 1
```

#### **Restoring Division (Signed Division)**
- **Restoring Division Algorithm**: Involves restoring the remainder to its previous state if it becomes negative during division.
  - It works by repeatedly shifting the dividend and divisor and restoring the remainder to its initial state when necessary.

#### **Non-Restoring Division (Signed Division)**
- **Non-Restoring Division Algorithm**: This method does not restore the remainder but instead directly modifies it based on the intermediate steps to avoid unnecessary steps.

---

### **Summary:**
- **Addition, subtraction, multiplication, and division** are fundamental operations implemented in the CPU using algorithms.
- **Binary addition** and **two's complement subtraction** simplify operations by treating signed numbers uniformly.
- **Multiplication** can be performed using basic bitwise shifts or more advanced methods like **Booth’s algorithm** for signed numbers.
- **Division** algorithms like **long division** for unsigned numbers and **restoring/non-restoring division** for signed numbers ensure accurate and efficient computation of division operations.