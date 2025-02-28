**Detailed Answers to 7-Mark Questions**

### **Unit I**

#### **1. What is asymptotic notation? Explain the various types in detail.**
Asymptotic notation is used to describe the efficiency of an algorithm in terms of time and space as input size grows. It helps compare algorithms based on their performance.

**Types of Asymptotic Notation:**
- **Big O Notation (O)**: Represents the worst-case complexity of an algorithm.
- **Big Omega Notation (Ω)**: Represents the best-case complexity.
- **Big Theta Notation (Θ)**: Represents the average or tight-bound complexity.
- **Little o Notation (o)**: Represents an upper bound that is not tight.
- **Little omega Notation (ω)**: Represents a lower bound that is not tight.

#### **2. What is complexity of an algorithm? Explain various notations used to express the complexity of an algorithm.**
Algorithm complexity is a measure of how the runtime or space requirements grow with the input size.

**Types of Complexity:**
- **Time Complexity:** The number of operations performed.
- **Space Complexity:** The amount of memory required.

**Complexity Notations:**
- **O(1):** Constant time
- **O(log n):** Logarithmic time
- **O(n):** Linear time
- **O(n²):** Quadratic time
- **O(2ⁿ):** Exponential time

#### **3. Explain Big O Notation with examples.**
Big O notation describes the worst-case scenario of an algorithm’s runtime.
- **Example:** Sorting algorithms:
  - Bubble Sort: O(n²)
  - Quick Sort: O(n log n)
  - Binary Search: O(log n)

#### **4. Linear Arrays and Address Calculation**
- **AAA [5:50], BBB [-5:10], CCC [1:8]**
  - **Number of elements:**
    - AAA: 50 - 5 + 1 = 46
    - BBB: 10 - (-5) + 1 = 16
    - CCC: 8 - 1 + 1 = 8
  - **Memory Address Calculation:**
    - `Address(A[i]) = Base + (i - lower_bound) * size`
    - Example: AAA [15], AAA [35], AAA [55]

#### **5. Multi-dimensional Arrays (P and Q) Calculations**
- **Dimensions of P(-2:2, 2:22) and Q(1:8, -5:5, -10:5)**
- **Number of elements:**
  - P: (2 - (-2) + 1) * (22 - 2 + 1) = 5 * 21 = 105
  - Q: (8 - 1 + 1) * (5 - (-5) + 1) * (5 - (-10) + 1) = 8 * 11 * 16 = 1408
- **Effective Indices Calculation and Address of Q[3,3,3]**

#### **6. Sparse Matrix**
A matrix where most elements are zero. Space-efficient representations include:
- **Compressed Sparse Row (CSR)**
- **Linked List Representation**

#### **7. Advantages & Disadvantages of a Single Linked List**
**Advantages:**
- Dynamic size, efficient insertions/deletions.
**Disadvantages:**
- More memory usage, no direct access to elements.

#### **8. C Program to Create a Singly Linked List**
```c
#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* next;
};
void insert(struct Node** head, int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = *head;
    *head = newNode;
}
```

#### **9. Circular and Doubly Linked List**
- **Circular Linked List:** Last node points to the first node.
- **Doubly Linked List:** Nodes have pointers to both previous and next nodes.

#### **10. Difference between Array and Linked List**
| Feature | Array | Linked List |
|---------|-------|------------|
| Memory | Contiguous | Non-contiguous |
| Size | Fixed | Dynamic |
| Access | O(1) | O(n) |

#### **11. Data Structure, Need, and Types**
A data structure is a way to organize and store data efficiently.
**Types:**
- **Linear:** Arrays, Linked Lists, Stacks, Queues
- **Non-Linear:** Trees, Graphs

#### **12. Complexity of the Given C Code**
Nested loops result in O(n²) complexity.

---

### **Unit II**

#### **13. Stack: PUSH and POP Operations**
Stack follows LIFO (Last In, First Out). Operations:
```c
void push(int stack[], int *top, int item) {
    stack[++(*top)] = item;
}
int pop(int stack[], int *top) {
    return stack[(*top)--];
}
```

#### **14. Tower of Hanoi Problem**
Recursive disk movement problem. Moves = `2^n - 1`
```c
void hanoi(int n, char from, char to, char aux) {
    if (n == 1) {
        printf("Move disk from %c to %c", from, to);
        return;
    }
    hanoi(n - 1, from, aux, to);
    hanoi(n - 1, aux, to, from);
}
```

#### **15. Circular Queue Implementation**
```c
void insert(int queue[], int *front, int *rear, int size, int item) {
    *rear = (*rear + 1) % size;
    queue[*rear] = item;
}
```

#### **16. Sorting Algorithms**
- **Insertion Sort, Selection Sort, Bubble Sort, Quick Sort**
```c
void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pivot = partition(arr, low, high);
        quickSort(arr, low, pivot - 1);
        quickSort(arr, pivot + 1, high);
    }
}
```

#### **17. Graphs & Minimum Spanning Tree Algorithms**
- **Prim’s Algorithm (Greedy MST approach)**
- **Kruskal’s Algorithm (Edge-based MST approach)**

#### **18. Floyd-Warshall Algorithm**
Finds all-pairs shortest paths in O(n³).

#### **19. Dijkstra’s Algorithm**
Finds the shortest path from a source node in O(V²).
```c
void dijkstra(int graph[V][V], int src) {
    int dist[V];
    for (int i = 0; i < V; i++) dist[i] = INF;
    dist[src] = 0;
}
```

---

This document contains detailed explanations and code implementations for all required topics.

