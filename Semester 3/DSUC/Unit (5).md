# Unit 5: Trees

A **tree** is a hierarchical data structure consisting of nodes, where each node contains a value and references (or links) to its child nodes. The concept of trees is widely used in computer science to model hierarchical relationships, such as file systems, organizational structures, and databases.

---

#### **5.1 Concept of Trees**
A **tree** is a collection of nodes connected by edges, with the following characteristics:
- **Root**: The topmost node in a tree. It has no parent.
- **Node**: A data element in the tree, which may or may not have children.
- **Leaf Node**: A node with no children.
- **Parent and Child**: A parent node has one or more child nodes.
- **Subtree**: A tree formed by a node and all of its descendants.
- **Depth**: The distance from the root to a particular node.
- **Height**: The length of the longest path from a node to a leaf.

**Basic Terminology**:
- **Degree of a node**: The number of children a node has.
- **Level of a node**: The number of edges from the root to the node.
- **Path**: A sequence of nodes where each consecutive node is connected by an edge.
- **Height of a tree**: The length of the longest path from the root to any leaf node.

**Types of Trees**:
- **Binary Tree**: Each node has at most two children (left and right).
- **Binary Search Tree (BST)**: A binary tree where for each node, the left child’s value is less than the node’s value, and the right child’s value is greater.
- **AVL Tree**: A self-balancing binary search tree where the height difference between the left and right subtrees is at most 1.
- **Heap**: A special type of binary tree where the parent’s value is either greater than or less than the children’s values (depending on whether it’s a max-heap or min-heap).

---

#### **5.2 Representation of Binary Tree in Memory**
A **binary tree** is represented using nodes, where each node contains:
- **Data**: The value or information stored in the node.
- **Left pointer**: A reference (pointer) to the left child.
- **Right pointer**: A reference (pointer) to the right child.

In **memory**, a binary tree is typically represented as a collection of structures (in C/C++) or objects (in Java), where each node has references to its left and right children.

**Memory Representation of a Binary Tree**:
- **Node Structure**:
  ```c
  struct Node {
      int data;
      struct Node* left;
      struct Node* right;
  };
  ```

**Binary Tree Example**:
```plaintext
        10
       /  \
     20    30
    /  \    /  \
   40  50  60  70
```
Here, the node with value 10 is the root, and nodes 20 and 30 are its children. Nodes 40, 50, 60, and 70 are the leaf nodes.

---

#### **5.3 Traversing Binary Trees**
Traversing a binary tree means visiting all the nodes in a specific order. There are three primary ways to traverse a binary tree:
- **Pre-order Traversal** (Root, Left, Right):
  - Visit the root node.
  - Traverse the left subtree.
  - Traverse the right subtree.
  
  **Example**: Pre-order of the tree above is: `10, 20, 40, 50, 30, 60, 70`.

  **Code Example** (Pre-order):
  ```c
  void preOrderTraversal(struct Node* root) {
      if (root != NULL) {
          printf("%d ", root->data);  // Visit the root
          preOrderTraversal(root->left);  // Traverse the left subtree
          preOrderTraversal(root->right);  // Traverse the right subtree
      }
  }
  ```

- **In-order Traversal** (Left, Root, Right):
  - Traverse the left subtree.
  - Visit the root node.
  - Traverse the right subtree.
  
  **Example**: In-order of the tree above is: `40, 20, 50, 10, 60, 30, 70`.

  **Code Example** (In-order):
  ```c
  void inOrderTraversal(struct Node* root) {
      if (root != NULL) {
          inOrderTraversal(root->left);  // Traverse the left subtree
          printf("%d ", root->data);  // Visit the root
          inOrderTraversal(root->right);  // Traverse the right subtree
      }
  }
  ```

- **Post-order Traversal** (Left, Right, Root):
  - Traverse the left subtree.
  - Traverse the right subtree.
  - Visit the root node.
  
  **Example**: Post-order of the tree above is: `40, 50, 20, 60, 70, 30, 10`.

  **Code Example** (Post-order):
  ```c
  void postOrderTraversal(struct Node* root) {
      if (root != NULL) {
          postOrderTraversal(root->left);  // Traverse the left subtree
          postOrderTraversal(root->right);  // Traverse the right subtree
          printf("%d ", root->data);  // Visit the root
      }
  }
  ```

---

#### **5.4 Searching, Inserting, and Deleting in Binary Search Trees**
A **binary search tree (BST)** is a binary tree where for each node:
- The left subtree contains nodes with values less than the node’s value.
- The right subtree contains nodes with values greater than the node’s value.

**Searching in a Binary Search Tree**:
- Start at the root.
- If the value is less than the current node, search the left subtree.
- If the value is greater, search the right subtree.
- If the value matches the current node, the search is successful.

**Code Example for Searching**:
```c
struct Node* search(struct Node* root, int key) {
    if (root == NULL || root->data == key) {
        return root;
    }
    if (key < root->data) {
        return search(root->left, key);
    }
    return search(root->right, key);
}
```

**Inserting in a Binary Search Tree**:
- Start at the root.
- Traverse left if the new value is less than the current node.
- Traverse right if the new value is greater.
- Insert the node when a `NULL` pointer is encountered.

**Code Example for Insertion**:
```c
struct Node* insert(struct Node* root, int key) {
    if (root == NULL) {
        struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
        newNode->data = key;
        newNode->left = newNode->right = NULL;
        return newNode;
    }
    if (key < root->data) {
        root->left = insert(root->left, key);
    } else {
        root->right = insert(root->right, key);
    }
    return root;
}
```

**Deleting from a Binary Search Tree**:
- If the node has no children (leaf node), simply remove it.
- If the node has one child, replace the node with its child.
- If the node has two children, find the **inorder successor** (the smallest node in the right subtree) or **inorder predecessor** (the largest node in the left subtree) and replace the node with it.

---

#### **5.5 Introduction to Heap**
A **heap** is a special binary tree-based data structure that satisfies the **heap property**:
- **Max-Heap**: The value of each node is greater than or equal to the values of its children.
- **Min-Heap**: The value of each node is less than or equal to the values of its children.

**Applications of Heaps**:
- **Priority Queue**: Used in scheduling tasks with different priorities.
- **Heap Sort**: A sorting algorithm that uses the heap data structure.

---

#### **5.6 Applications of Trees**
- **Binary Search Trees (BST)**: Used in searching, sorting, and maintaining a dynamic ordered list.
- **AVL Trees**: Used in databases for quick data access and self-balancing operations.
- **Heaps**: Used in priority queues, heap sort, and efficient graph algorithms like Dijkstra’s shortest path.
- **Expression Trees**: Used in compilers to represent arithmetic expressions.
- **File Systems**: Hierarchical structures like directories and files can be represented using trees.

