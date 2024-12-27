# Unit 3: Linked Lists

A **linked list** is a linear data structure in which elements (nodes) are stored in a non-contiguous memory location, and each node contains two parts: the data and a reference (or link) to the next node in the sequence. Linked lists are dynamic in nature, allowing efficient insertion and deletion operations compared to arrays.

---

#### **3.1 Introduction to Linked List**
A linked list consists of a collection of nodes, where each node contains:
- **Data**: The value or information held by the node.
- **Link (or Pointer)**: A reference to the next node in the list (in the case of singly linked lists).

**Types of Linked Lists**:
- **Singly Linked List**: Each node points to the next node in the list. The last node points to `NULL`.
- **Doubly Linked List**: Each node points to both the next and the previous nodes, providing two-way traversal.
- **Circular Linked List**: The last node points back to the first node, forming a circle.

**Advantages**:
- Dynamic memory allocation.
- Efficient insertion and deletion of elements.
- No memory wastage, unlike arrays where space must be allocated beforehand.

**Disadvantages**:
- Random access is not possible (to access an element, you must traverse from the head).
- Requires extra memory for the pointer/reference.

---

#### **3.2 Representation of Linked Lists in Memory**
In a **linked list**, each element is represented as a node. The node is typically stored in dynamic memory (using pointers in languages like C or references in Java).

- **Singly Linked List Representation**:
  - Each node is represented as an object with two fields: **data** and **next**.
  - The **next** field stores the address (pointer) of the next node in the list, and the last node's **next** points to `NULL`.

  **Example**:  
  ```plaintext
  Head -> [Data|Next] -> [Data|Next] -> [Data|NULL]
  ```

- **Doubly Linked List Representation**:
  - Each node contains three fields: **data**, **next**, and **prev**.
  - The **next** field stores the pointer to the next node, while the **prev** field stores the pointer to the previous node.
  
  **Example**:  
  ```plaintext
  Head <-> [Prev|Data|Next] <-> [Prev|Data|Next] <-> [Prev|Data|NULL]
  ```

- **Circular Linked List**:
  - The **next** pointer of the last node points back to the head node, making the list circular.
  
  **Example**:  
  ```plaintext
  Head -> [Data|Next] -> [Data|Next] -> [Data|Head]
  ```

---

#### **3.3 Operations on Linked Lists**
Common operations that can be performed on linked lists include **insertion**, **deletion**, and **traversal**.

- **Insertion**:
  - **At the beginning**: Add a new node and make it the head of the list.
  - **At the end**: Traverse the list to find the last node and link it to the new node.
  - **At a given position**: Traverse to the required position and adjust the links accordingly.

  **Code Example for Insertion at the Beginning**:
  ```c
  void insertAtBeginning(Node **head, int data) {
      Node *newNode = (Node*)malloc(sizeof(Node));
      newNode->data = data;
      newNode->next = *head;
      *head = newNode;
  }
  ```

- **Deletion**:
  - **At the beginning**: Remove the head node and point the head to the next node.
  - **At the end**: Traverse to the last node and remove the previous node.
  - **At a given position**: Traverse to the desired position and adjust the links.

  **Code Example for Deletion at the Beginning**:
  ```c
  void deleteAtBeginning(Node **head) {
      if (*head != NULL) {
          Node *temp = *head;
          *head = (*head)->next;
          free(temp);
      }
  }
  ```

- **Traversal**:
  - Traverse through the list from the head node and print the data stored in each node.

  **Code Example for Traversal**:
  ```c
  void traverse(Node *head) {
      while (head != NULL) {
          printf("%d -> ", head->data);
          head = head->next;
      }
      printf("NULL\n");
  }
  ```

---

#### **3.4 Applications of Linked Lists**
Linked lists are widely used in various applications due to their dynamic nature and efficient insertion and deletion operations:
- **Dynamic Memory Allocation**: Used in memory management systems where the memory needs to be allocated or freed dynamically.
- **Implementation of Data Structures**: Linked lists are used to implement data structures like **stacks**, **queues**, and **hash tables**.
- **Navigation Systems**: Doubly linked lists are used in systems where bi-directional traversal is required (e.g., navigation through browser history).
- **Music Playlist**: Music players use linked lists to manage playlists, where songs can be inserted, deleted, or traversed in both directions.

---

#### **3.5 Doubly Linked Lists**
In a **doubly linked list**, each node contains three fields:
- **Data**: The value or information held by the node.
- **Next**: A pointer to the next node in the list.
- **Prev**: A pointer to the previous node in the list.

This structure allows traversal in both directions (forward and backward).

**Advantages of Doubly Linked Lists**:
- Easy to traverse in both directions.
- Efficient insertion and deletion from both ends.
- Can be used to implement **deques** (double-ended queues).

**Disadvantages**:
- Requires extra memory for the `prev` pointer.
- Slightly more complex to implement than singly linked lists.

---

#### **3.6 Operations on Doubly Linked Lists**
The operations on **doubly linked lists** are similar to those of singly linked lists, with the addition of handling the **prev** pointer.

- **Insertion**:
  - **At the beginning**: Insert a new node before the current head and update the `prev` pointer of the original head.
  - **At the end**: Insert a new node after the last node and update the `next` pointer of the previous node.
  - **At a given position**: Insert a new node after or before a specific node, updating both the `next` and `prev` pointers.

  **Code Example for Insertion at the Beginning**:
  ```c
  void insertAtBeginning(Node **head, int data) {
      Node *newNode = (Node*)malloc(sizeof(Node));
      newNode->data = data;
      newNode->prev = NULL;
      newNode->next = *head;
      if (*head != NULL) {
          (*head)->prev = newNode;
      }
      *head = newNode;
  }
  ```

- **Deletion**:
  - **At the beginning**: Remove the head node and update the `prev` pointer of the new head.
  - **At the end**: Traverse to the last node and remove it, updating the `next` pointer of the second-to-last node.
  - **At a given position**: Adjust both `next` and `prev` pointers to remove the node.

  **Code Example for Deletion at the Beginning**:
  ```c
  void deleteAtBeginning(Node **head) {
      if (*head != NULL) {
          Node *temp = *head;
          *head = (*head)->next;
          if (*head != NULL) {
              (*head)->prev = NULL;
          }
          free(temp);
      }
  }
  ```

- **Traversal**:
  - **Forward traversal**: Traverse from the head to the last node, printing each node's data.
  - **Backward traversal**: Traverse from the tail to the head node, printing each node's data.

  **Code Example for Forward Traversal**:
  ```c
  void forwardTraverse(Node *head) {
      while (head != NULL) {
          printf("%d <-> ", head->data);
          head = head->next;
      }
      printf("NULL\n");
  }
  ```

---
