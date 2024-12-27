# Unit 6: Sorting and Searching
---

**6.1 Introduction to Sorting and Searching**

- **Sorting**: The process of arranging elements in a specific order, usually in ascending or descending order. Sorting helps in efficiently searching for elements, organizing data, and optimizing other algorithms.

- **Searching**: The process of finding a specific element or value within a collection (such as an array or list). The goal is to determine whether the element exists and, if it does, to retrieve its position.

---

**6.2 Search Algorithms (Linear and Binary)**

1. **Linear Search**:
   - **Description**: Linear search is the simplest searching algorithm. It checks each element in the array sequentially until the desired element is found or the entire array has been searched.
   - **Time Complexity**: O(n), where `n` is the number of elements in the array.
   - **Algorithm** (in C):
     ```c
     int linearSearch(int arr[], int n, int target) {
         for (int i = 0; i < n; i++) {
             if (arr[i] == target) {
                 return i;  // Target found at index i
             }
         }
         return -1;  // Target not found
     }
     ```
   - **Usage**: Best for unsorted data or small datasets.

2. **Binary Search**:
   - **Description**: Binary search is a more efficient search algorithm that works on sorted arrays. It repeatedly divides the search interval in half. If the target value is less than the middle element, it narrows the search to the left half; otherwise, it narrows the search to the right half.
   - **Time Complexity**: O(log n), where `n` is the number of elements in the array.
   - **Algorithm** (in C):
     ```c
     int binarySearch(int arr[], int n, int target) {
         int left = 0, right = n - 1;
         while (left <= right) {
             int mid = left + (right - left) / 2;
             if (arr[mid] == target) {
                 return mid;  // Target found at mid
             } else if (arr[mid] < target) {
                 left = mid + 1;  // Target is in the right half
             } else {
                 right = mid - 1;  // Target is in the left half
             }
         }
         return -1;  // Target not found
     }
     ```
   - **Usage**: Works only on sorted data, much faster than linear search for large datasets.

---

**6.3 Sorting Algorithms**

1. **Bubble Sort**:
   - **Description**: Bubble sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. This process is repeated until the list is sorted.
   - **Time Complexity**: O(n^2), where `n` is the number of elements.
   - **Algorithm** (in C):
     ```c
     void bubbleSort(int arr[], int n) {
         for (int i = 0; i < n - 1; i++) {
             for (int j = 0; j < n - 1 - i; j++) {
                 if (arr[j] > arr[j + 1]) {
                     // Swap arr[j] and arr[j + 1]
                     int temp = arr[j];
                     arr[j] = arr[j + 1];
                     arr[j + 1] = temp;
                 }
             }
         }
     }
     ```
   - **Usage**: Simple but inefficient for large datasets.

2. **Insertion Sort**:
   - **Description**: Insertion sort builds the final sorted array one element at a time. It picks the next element and places it in the correct position among the previously sorted elements.
   - **Time Complexity**: O(n^2), where `n` is the number of elements.
   - **Algorithm** (in C):
     ```c
     void insertionSort(int arr[], int n) {
         for (int i = 1; i < n; i++) {
             int key = arr[i];
             int j = i - 1;
             while (j >= 0 && arr[j] > key) {
                 arr[j + 1] = arr[j];
                 j--;
             }
             arr[j + 1] = key;
         }
     }
     ```
   - **Usage**: Efficient for small datasets or nearly sorted data.

3. **Quick Sort**:
   - **Description**: Quick sort is a divide-and-conquer algorithm. It selects a "pivot" element and partitions the array into two sub-arrays (elements less than the pivot and elements greater than the pivot). It then recursively sorts the sub-arrays.
   - **Time Complexity**: O(n log n) on average, but O(n^2) in the worst case.
   - **Algorithm** (in C):
     ```c
     int partition(int arr[], int low, int high) {
         int pivot = arr[high];
         int i = (low - 1);
         for (int j = low; j < high; j++) {
             if (arr[j] < pivot) {
                 i++;
                 // Swap arr[i] and arr[j]
                 int temp = arr[i];
                 arr[i] = arr[j];
                 arr[j] = temp;
             }
         }
         // Swap arr[i + 1] and arr[high]
         int temp = arr[i + 1];
         arr[i + 1] = arr[high];
         arr[high] = temp;
         return (i + 1);
     }

     void quickSort(int arr[], int low, int high) {
         if (low < high) {
             int pi = partition(arr, low, high);
             quickSort(arr, low, pi - 1);  // Sort before pivot
             quickSort(arr, pi + 1, high); // Sort after pivot
         }
     }
     ```
   - **Usage**: Very efficient for large datasets.

4. **Selection Sort**:
   - **Description**: Selection sort works by repeatedly finding the smallest (or largest) element in the unsorted portion of the array and swapping it with the first unsorted element.
   - **Time Complexity**: O(n^2), where `n` is the number of elements.
   - **Algorithm** (in C):
     ```c
     void selectionSort(int arr[], int n) {
         for (int i = 0; i < n - 1; i++) {
             int minIndex = i;
             for (int j = i + 1; j < n; j++) {
                 if (arr[j] < arr[minIndex]) {
                     minIndex = j;
                 }
             }
             // Swap arr[i] and arr[minIndex]
             int temp = arr[i];
             arr[i] = arr[minIndex];
             arr[minIndex] = temp;
         }
     }
     ```
   - **Usage**: Simple but inefficient for large datasets.

5. **Merge Sort**:
   - **Description**: Merge sort is a divide-and-conquer algorithm. It divides the array into two halves, sorts each half, and then merges the sorted halves together.
   - **Time Complexity**: O(n log n), where `n` is the number of elements.
   - **Algorithm** (in C):
     ```c
     void merge(int arr[], int left, int mid, int right) {
         int n1 = mid - left + 1;
         int n2 = right - mid;
         int L[n1], R[n2];
         for (int i = 0; i < n1; i++) L[i] = arr[left + i];
         for (int j = 0; j < n2; j++) R[j] = arr[mid + 1 + j];
         
         int i = 0, j = 0, k = left;
         while (i < n1 && j < n2) {
             if (L[i] <= R[j]) {
                 arr[k++] = L[i++];
             } else {
                 arr[k++] = R[j++];
             }
         }
         while (i < n1) arr[k++] = L[i++];
         while (j < n2) arr[k++] = R[j++];
     }

     void mergeSort(int arr[], int left, int right) {
         if (left < right) {
             int mid = left + (right - left) / 2;
             mergeSort(arr, left, mid);
             mergeSort(arr, mid + 1, right);
             merge(arr, left, mid, right);
         }
     }
     ```
   - **Usage**: Efficient for large datasets, especially when data is stored externally (e.g., on disk).

6. **Heap Sort**:
   - **Description**: Heap sort is a comparison-based sorting algorithm that uses a binary heap data structure. It builds a max-heap and repeatedly extracts the maximum element.
   - **Time Complexity**: O(n log n), where `n` is the number of elements.
   - **Usage**: Efficient and works well for large datasets.

---