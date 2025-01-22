# Unit 2: Arrays

**2.1 Concept of Arrays**  
An **array** is a data structure that stores a fixed-size sequence of elements of the same data type in contiguous memory locations. It provides a way to store multiple values in a single variable rather than declaring separate variables for each value.

- **Characteristics**:
  - **Fixed Size**: The size of the array is defined at the time of creation and cannot be changed later.
  - **Indexing**: Elements in an array are accessed via their index, starting from 0 in most programming languages.
  - **Homogeneous Elements**: All elements in an array are of the same data type (e.g., all integers, all characters, etc.).

- **Declaration**:  
  In C:
  ```c
  int arr[5];  // declares an array of 5 integers
  ```
  In Python:
  ```python
  arr = [1, 2, 3, 4, 5]  # declares a list (which functions like an array)
  ```

**2.2 Storage Representation of Multi-Dimensional Arrays**  
Multi-dimensional arrays are arrays of arrays. They can represent matrices or tables, where data is stored in more than one dimension (rows and columns).

- **2D Array** (Matrix):
  A 2D array can be represented as an array of arrays. Each element in the main array is a 1D array.
  - Example in C:
    ```c
    int arr[3][3];  // A 3x3 matrix (2D array)
    ```
    In memory, it is stored in a **row-major order**, meaning that the elements of each row are stored contiguously.
    
  - **Memory Representation** (Row-major order for 3x3 matrix):
    ```
    arr[0][0], arr[0][1], arr[0][2], arr[1][0], arr[1][1], arr[1][2], arr[2][0], arr[2][1], arr[2][2]
    ```
    The data is stored in consecutive memory locations in this order.

- **3D Array**: A three-dimensional array can be thought of as an array of 2D arrays.
  - Example in C:
    ```c
    int arr[2][2][2];  // A 2x2x2 matrix (3D array)
    ```

**2.3 Operations on Arrays with Algorithms**  

- **Searching**: Finding an element in an array. Common algorithms include:
  - **Linear Search**: A simple search that checks each element one by one until the desired element is found.
    - **Algorithm**:
      1. Start from the first element.
      2. Compare each element with the target.
      3. If a match is found, return the index; otherwise, return -1 (not found).

      ```c
      int linearSearch(int arr[], int n, int target) {
          for (int i = 0; i < n; i++) {
              if (arr[i] == target) return i;
          }
          return -1;  // Not found
      }
      ```

- **Traversing**: Visiting each element in an array, often used to display the elements or perform operations on them.
  - **Algorithm**:
    - Loop through each index of the array and access the element at that index.

    ```c
    void traverse(int arr[], int n) {
        for (int i = 0; i < n; i++) {
            printf("%d ", arr[i]);
        }
    }
    ```

- **Inserting**: Adding an element at a specific position in an array. This involves shifting the elements after the insertion point to the right.
  - **Algorithm** (Inserting at index `i`):
    1. Shift elements from index `i` to the right.
    2. Insert the new element at index `i`.
    3. Increment the array size.

    ```c
    void insert(int arr[], int *n, int element, int index) {
        for (int i = *n; i > index; i--) {
            arr[i] = arr[i - 1];
        }
        arr[index] = element;
        (*n)++;
    }
    ```

- **Deleting**: Removing an element from a specific position in an array. This involves shifting the elements after the deleted element to the left.
  - **Algorithm** (Deleting at index `i`):
    1. Shift elements from index `i+1` to the left.
    2. Decrease the array size.

    ```c
    void delete(int arr[], int *n, int index) {
        for (int i = index; i < *n - 1; i++) {
            arr[i] = arr[i + 1];
        }
        (*n)--;
    }
    ```
