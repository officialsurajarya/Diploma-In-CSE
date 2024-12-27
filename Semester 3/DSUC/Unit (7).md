# Unit 7: Graph

A **graph** is a non-linear data structure consisting of a set of nodes (vertices) and a set of edges (connections) that represent relationships between the nodes. Graphs are used to model relationships in various real-world problems, such as social networks, routing algorithms, and network topologies.

---

#### **7.1 Introduction to Graph**
A **graph** is defined as a collection of nodes (vertices) and edges that connect pairs of nodes. Graphs can be classified into several types based on their structure:

**Types of Graphs**:
- **Undirected Graph**: In an undirected graph, edges have no direction. If there is an edge between vertices A and B, you can travel from A to B or from B to A.
- **Directed Graph (Digraph)**: In a directed graph, edges have a direction. An edge from vertex A to vertex B does not imply an edge from B to A.
- **Weighted Graph**: In a weighted graph, edges have weights or costs associated with them.
- **Unweighted Graph**: In an unweighted graph, all edges are treated equally, with no specific weights assigned.
- **Cyclic Graph**: A graph that contains at least one cycle (a path where the first and last vertices are the same).
- **Acyclic Graph**: A graph that does not contain any cycles.

**Graph Terminology**:
- **Vertex (Node)**: A point in the graph where edges meet.
- **Edge**: A connection between two vertices.
- **Adjacent**: Two vertices are adjacent if there is an edge between them.
- **Degree**: The number of edges connected to a vertex. In a directed graph, there are in-degrees (edges coming into a vertex) and out-degrees (edges leaving a vertex).
- **Path**: A sequence of edges connecting a sequence of vertices.
- **Cycle**: A path in a graph where the first and last vertices are the same.

**Graph Representation**:
- **Adjacency Matrix**: A 2D array where element `matrix[i][j]` is 1 if there is an edge between vertex i and vertex j, otherwise 0.
- **Adjacency List**: A list where each vertex has a list of adjacent vertices. This representation is more space-efficient for sparse graphs.

---

#### **7.2 Basic Operations on Graph**
Several fundamental operations can be performed on graphs, including:

1. **Add a Vertex**: Add a new vertex to the graph.
2. **Add an Edge**: Add an edge between two vertices.
3. **Remove a Vertex**: Remove a vertex and all edges associated with it.
4. **Remove an Edge**: Remove an edge between two vertices.
5. **Check for Edge**: Check if there is an edge between two vertices.
6. **Get Neighbors**: Retrieve all adjacent vertices of a given vertex.

These operations are essential for manipulating graphs in algorithms and applications.

---

#### **7.3 Depth First Search (DFS)**
**Depth First Search (DFS)** is a graph traversal algorithm that explores as far as possible along each branch before backtracking. DFS starts at a selected vertex and explores its neighbors before moving to the next level.

**DFS Characteristics**:
- DFS can be implemented using either recursion or an explicit stack.
- DFS is particularly useful for searching deep into a graph and finding paths or cycles.
- It can be used for traversing or searching trees and graphs.

**DFS Algorithm**:
1. Start from the root node (or any arbitrary node).
2. Visit the node and mark it as visited.
3. Explore each adjacent node that hasn't been visited yet by recursively calling DFS on that node.
4. Backtrack when no unvisited adjacent node is found.

**DFS Code Example** (using recursion):
```c
void DFS(int graph[MAX_VERTICES][MAX_VERTICES], int visited[MAX_VERTICES], int vertex, int numVertices) {
    visited[vertex] = 1;  // Mark the current node as visited
    printf("%d ", vertex);  // Process the current node
    for (int i = 0; i < numVertices; i++) {
        if (graph[vertex][i] == 1 && !visited[i]) {
            DFS(graph, visited, i, numVertices);  // Recursively visit unvisited neighbors
        }
    }
}
```

**DFS Example**:
For a graph:
```plaintext
    0
   / \
  1   2
 / \
3   4
```
DFS starting from node 0 would visit the nodes in the following order: `0, 1, 3, 4, 2`.

---

#### **7.4 Breadth First Search (BFS)**
**Breadth First Search (BFS)** is another graph traversal algorithm, but it explores all the nodes at the present depth level before moving on to nodes at the next depth level. BFS is often used in finding the shortest path in an unweighted graph.

**BFS Characteristics**:
- BFS uses a **queue** to keep track of the nodes to be explored.
- BFS explores neighbors level by level, making it useful for finding the shortest path in an unweighted graph.

**BFS Algorithm**:
1. Start at the root node (or any arbitrary node).
2. Mark the node as visited and enqueue it.
3. While the queue is not empty, dequeue a node and visit its unvisited neighbors, enqueuing each of them.
4. Repeat until all reachable nodes are visited.

**BFS Code Example** (using a queue):
```c
#include <stdio.h>
#include <stdlib.h>

#define MAX_VERTICES 100

void BFS(int graph[MAX_VERTICES][MAX_VERTICES], int visited[MAX_VERTICES], int start, int numVertices) {
    int queue[MAX_VERTICES];
    int front = -1, rear = -1;
    
    visited[start] = 1;  // Mark the start node as visited
    queue[++rear] = start;  // Enqueue the start node
    
    while (front != rear) {
        int current = queue[++front];  // Dequeue the next node
        
        printf("%d ", current);  // Process the current node
        
        for (int i = 0; i < numVertices; i++) {
            if (graph[current][i] == 1 && !visited[i]) {
                visited[i] = 1;  // Mark the neighbor as visited
                queue[++rear] = i;  // Enqueue the neighbor
            }
        }
    }
}
```

**BFS Example**:
For the same graph as before:
```plaintext
    0
   / \
  1   2
 / \
3   4
```
BFS starting from node 0 would visit the nodes in the following order: `0, 1, 2, 3, 4`.

---

### **Summary of Differences Between DFS and BFS**
- **DFS**: Explores as deep as possible down a branch before backtracking. It uses a stack (recursive or explicit) and can be implemented more easily using recursion.
- **BFS**: Explores all nodes at the current level before moving to the next level. It uses a queue and is ideal for finding the shortest path in unweighted graphs.

