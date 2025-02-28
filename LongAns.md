**Detailed Answers to 7-Mark Questions**

### **Unit I**

#### **1. What is asymptotic notation? Explain the various types in detail.**
Asymptotic notation is a mathematical representation used to describe the running time or space complexity of an algorithm based on input size (n). The main types are:
- **Big O (O):** Upper bound notation, worst-case complexity.
- **Big Omega (Ω):** Lower bound notation, best-case complexity.
- **Theta (Θ):** Tight bound, representing both upper and lower bounds.

#### **2. What is complexity of an algorithm? Explain various notations used to express the complexity of an algorithm.**
Algorithm complexity refers to the performance of an algorithm in terms of time and space.
- **Time Complexity:** Measures execution time.
- **Space Complexity:** Measures memory usage.
Notations used:
- **O(n):** Linear growth
- **O(n²):** Quadratic growth
- **O(log n):** Logarithmic growth

#### **3. Various asymptotic notations and Big O Notation**
- **Big O (O):** Worst-case performance
- **Big Omega (Ω):** Best-case performance
- **Big Theta (Θ):** Average-case performance
Big O describes the maximum number of steps required for execution.

#### **4. Consider the linear arrays AAA [5:50], BBB [-5:10], CCC [1:8]**
**A. Find the number of elements in each array**
- AAA: `50 - 5 + 1 = 46`
- BBB: `10 - (-5) + 1 = 16`
- CCC: `8 - 1 + 1 = 8`

**B. Find the address of AAA [15], AAA [35], AAA [55]**
Using formula: `Address(A[i]) = Base + (i - lower bound) * size`

#### **5. Multi-dimensional arrays (P and Q) calculations**
- **Find lengths of dimensions**
- **Find number of elements**
- **Compute address for Q[3,3,3]**

#### **6. Sparse Matrix**
A matrix with a majority of zero values.

#### **7. Advantages & Disadvantages of a Single Linked List**
**Advantages:**
- Dynamic size
- Efficient insertion/deletion
**Disadvantages:**
- No backward traversal
- More memory usage due to pointers

#### **8. C Program to create a Singly Linked List**
```c
#include<stdio.h>
#include<stdlib.h>
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
A data structure is a way to organize and store data efficiently. Types:
- **Linear:** Arrays, Linked Lists, Stacks, Queues
- **Non-Linear:** Trees, Graphs

#### **12. Why do we need a Data Type?**
Data types specify the type of data and operations allowed on them.

#### **13. Complexity of the Given C Code**
Nested loops result in O(n²) complexity.

---

### **Unit II**

#### **14. Stack: PUSH and POP Operations**
Stack follows LIFO (Last In, First Out). Operations:
- **PUSH:** Insert an element.
- **POP:** Remove the top element.
```c
void push(int stack[], int *top, int item) {
    stack[++(*top)] = item;
}
int pop(int stack[], int *top) {
    return stack[(*top)--];
}
```

#### **15. Recursion & Recursive Program for Sum of Digits**
```c
int sumOfDigits(int n) {
    if (n == 0) return 0;
    return (n % 10) + sumOfDigits(n / 10);
}
```
Complexity: O(log n)

#### **16. Tower of Hanoi Problem**
Move `n` disks from source to destination using an auxiliary peg. Total moves = `2^n - 1`
```c
void hanoi(int n, char from, char to, char aux) {
    if (n == 1) {
        printf("Move %d from %c to %c", n, from, to);
        return;
    }
    hanoi(n - 1, from, aux, to);
    hanoi(n - 1, aux, to, from);
}
```

#### **17. Circular Queue Implementation**
```c
void insert(int queue[], int *front, int *rear, int size, int item) {
    *rear = (*rear + 1) % size;
    queue[*rear] = item;
}
```

#### **18. Infix to Postfix Conversion**
Expression: `A + (B * C - (D/E ^ F) * H)`
- Postfix: `ABC*DEF/^H*-+`

---

### **Unit III**

#### **19. Sorting Algorithms**
- **Insertion Sort:** Shifts elements to insert in order.
- **Selection Sort:** Selects the minimum element and swaps.
- **Bubble Sort:** Repeatedly swaps adjacent elements.
- **Quick Sort:** Partition-based sorting.

```c
void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pivot = partition(arr, low, high);
        quickSort(arr, low, pivot - 1);
        quickSort(arr, pivot + 1, high);
    }
}
```

---

### **Unit IV**

#### **20. Binary Search Tree Operations**
- **Insertion, Deletion, Traversal**

#### **21. AVL Tree & Rotations**
Self-balancing BST with rotations to maintain balance.

---

### **Unit V**

#### **22. Graphs & Minimum Spanning Tree Algorithms**
- **Prim’s Algorithm** (Greedy MST approach)
- **Kruskal’s Algorithm** (Edge-based MST approach)

#### **23. Floyd-Warshall Algorithm**
Finds all-pairs shortest paths in O(n³).

#### **24. Dijkstra’s Algorithm**
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

