# Unit 4: Stacks, Queues, and Recursion

---

**4.1 Introduction to Stacks**  
A **stack** is a linear data structure that follows the **Last In First Out** (LIFO) principle, where the last element added is the first one to be removed. It operates with two main operations:
- **Push**: Adds an element to the top of the stack.
- **Pop**: Removes the top element from the stack.

Think of a stack as a pile of plates, where you can only take the top plate off or add a new one to the top.

---

**4.2 Representation of Stacks**  
A stack can be represented in memory in two main ways:
1. **Array Representation**: Using a fixed-size array to store the stack elements. A variable keeps track of the top index.
2. **Linked List Representation**: Using a linked list where each node points to the previous node in the stack, and the top of the stack points to the first element.

---

**4.3 Implementation of Stacks**  
Stacks can be implemented using an array or a linked list. Here is an example of stack operations using an array in C:

```c
#define MAX 5
int stack[MAX];
int top = -1;

int isEmpty() {
    return top == -1;
}

int isFull() {
    return top == MAX - 1;
}

void push(int value) {
    if (isFull()) {
        printf("Stack Overflow\n");
        return;
    }
    stack[++top] = value;
}

int pop() {
    if (isEmpty()) {
        printf("Stack Underflow\n");
        return -1;  // Indicates stack is empty
    }
    return stack[top--];
}

int peek() {
    if (isEmpty()) {
        printf("Stack is empty\n");
        return -1;
    }
    return stack[top];
}
```

---

**4.4 Applications of Stacks**  
Stacks are used in various applications, including:
- **Expression Evaluation**: Stacks are used in evaluating arithmetic expressions (e.g., infix, postfix, and prefix expressions).
- **Undo Mechanism**: Used in applications like text editors where the last action is undone first.
- **Function Call Management**: The program uses a stack to manage function calls, where each function call is pushed onto the stack, and on return, it is popped.

---

**4.5 Introduction to Queues**  
A **queue** is another linear data structure that follows the **First In First Out** (FIFO) principle, where the first element added is the first one to be removed. It operates with two main operations:
- **Enqueue**: Adds an element to the rear of the queue.
- **Dequeue**: Removes an element from the front of the queue.

A real-world analogy is a queue in a ticket counter, where the first person in line is served first.

---

**4.6 Implementation of Queues**  
Queues can be implemented using an array or a linked list. Here's a simple queue implementation using an array in C:

```c
#define MAX 5
int queue[MAX];
int front = -1, rear = -1;

int isEmpty() {
    return front == -1;
}

int isFull() {
    return rear == MAX - 1;
}

void enqueue(int value) {
    if (isFull()) {
        printf("Queue Overflow\n");
        return;
    }
    if (front == -1) front = 0;  // First element enqueued
    queue[++rear] = value;
}

int dequeue() {
    if (isEmpty()) {
        printf("Queue Underflow\n");
        return -1;  // Queue is empty
    }
    int value = queue[front++];
    if (front > rear) front = rear = -1;  // Reset when queue is empty
    return value;
}

int peek() {
    if (isEmpty()) {
        printf("Queue is empty\n");
        return -1;
    }
    return queue[front];
}
```

---

**4.7 Circular Queues**  
A **circular queue** is a more efficient version of a queue where the queue is treated as a circular structure. It allows the elements to wrap around when the end of the queue is reached, and it uses the space more effectively by reusing positions that are dequeued.

- **Array Representation**: The rear and front pointers are adjusted so that when the queue reaches the end, it continues from the beginning of the array if space is available.

---

**4.8 De-queues (Double-Ended Queues)**  
A **dequeue (double-ended queue)** allows elements to be added or removed from both ends. Operations on a dequeue are:
- **InsertFront**: Adds an element to the front of the queue.
- **InsertRear**: Adds an element to the rear of the queue.
- **DeleteFront**: Removes an element from the front.
- **DeleteRear**: Removes an element from the rear.

Dequeues can be implemented using an array or linked list.

---

**4.9 Applications of Queues**  
Queues have several important applications:
- **Job Scheduling**: In operating systems, queues are used for scheduling tasks, ensuring that processes are handled in the order they arrive.
- **Breadth-First Search (BFS)**: In graph traversal, BFS uses a queue to explore nodes level by level.
- **Traffic Management**: In real-world traffic systems, queues manage the vehicles waiting in line, like at toll booths or traffic lights.

---

**4.10 Recursion**  
**Recursion** is a programming technique where a function calls itself to solve a problem. A recursive function typically has two parts:
1. **Base case**: The condition that stops the recursion.
2. **Recursive case**: The part where the function calls itself to move towards the base case.

**Example of a Recursive Function** (Factorial calculation):

```c
int factorial(int n) {
    if (n == 0 || n == 1) {
        return 1;  // Base case
    }
    return n * factorial(n - 1);  // Recursive case
}
```

**Applications of Recursion**:
- **Factorial Calculation**
- **Fibonacci Series**
- **Tree Traversals**
- **Solving Maze Problems**
- **Sorting Algorithms** (e.g., Quick Sort, Merge Sort)

---
