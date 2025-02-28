I'll now provide answers to the questions from your PDF. Since there are multiple sections, I'll start with the **2-mark questions** and move forward step by step.

---

### **2-Mark Questions Answers**

1. **Define best case, average case, and worst case for analyzing the complexity of a program.**  
   - **Best Case:** The scenario where the algorithm performs the minimum number of operations (e.g., sorted input for a sorting algorithm).  
   - **Average Case:** The expected number of operations for a random input.  
   - **Worst Case:** The scenario where the algorithm performs the maximum number of operations (e.g., reverse-sorted input for sorting).  

2. **Differentiate between Binary Search Tree (BST) and Heap.**  
   - **BST:** A tree where the left subtree has smaller values, and the right subtree has larger values.  
   - **Heap:** A tree where the parent node is either greater than or smaller than both children (Max-Heap or Min-Heap).  
   - **BST supports searching efficiently, whereas Heap is used for priority queue operations.**  

3. **Write the condition for an empty and full circular queue.**  
   - **Empty Queue Condition:** `Front == -1` or `Front == Rear + 1`  
   - **Full Queue Condition:** `(Rear + 1) % Size == Front`  

4. **What do you understand by tail recursion?**  
   - A recursive function is **tail-recursive** if the recursive call is the last operation before returning the result. It helps optimize space as no additional function calls are needed.  
   - **Example:**  
     ```c
     void tailRecursive(int n) {
         if (n == 0) return;
         printf("%d ", n);
         tailRecursive(n - 1);
     }
     ```  

5. **Construct an expression tree for the algebraic expression:**  
   - Expression: `(a - b) / ((c * d) + e)`  
   - **Expression Tree:**
     ```
            "/"
           /   \
         "-"   "+"
        /  \   /  \
       a    b *    e
             / \
            c   d
     ```  

6. **Differentiate between internal sorting and external sorting.**  
   - **Internal Sorting:** Sorting algorithms that work within RAM, such as Quick Sort, Merge Sort, and Heap Sort.  
   - **External Sorting:** Used when data is too large to fit in RAM (e.g., Multiway Merge Sort).  

7. **Advantages and disadvantages of an array over a linked list.**  
   **Advantages:**  
   - Faster random access (`O(1)`)  
   - Memory locality improves cache performance  
   **Disadvantages:**  
   - Fixed size  
   - Costly insertions and deletions (`O(n)`)  

8. **Algorithm for Breadth-First Search (BFS) traversal of a graph.**  
   ```python
   def BFS(graph, start):
       visited = set()
       queue = [start]
       while queue:
           node = queue.pop(0)
           if node not in visited:
               print(node, end=" ")
               visited.add(node)
               queue.extend(graph[node])
   ```  

9. **Height of a complete binary tree with 1,000,000 nodes.**  
   - Height = `log₂(1000000) ≈ 19.93` → **Rounded to 20**  

10. **Which data structure is used to perform recursion and why?**  
    - **Stack** is used because it follows **LIFO**, storing return addresses for function calls.  

11. **Define a sparse matrix.**  
    - A matrix where the majority of elements are **zero**.  

12. **Space-efficient representation of a sparse matrix.**  
    - **Compressed Sparse Row (CSR)** or **Linked List Representation**  

13. **Advantages of a doubly linked list over a singly linked list.**  
    - **Two-way traversal**  
    - **Easier insertion and deletion**  

14. **Example of stable and unstable sorting techniques.**  
    - **Stable:** Merge Sort  
    - **Unstable:** Quick Sort  

15. **Advantages of AVL tree over Binary Search Tree (BST).**  
    - AVL tree maintains **balanced height**, ensuring `O(log n)` search time.  

16. **Explain tail recursion with an example.**  
    - Already explained in **Question 4**.  

17. **Different representations of graphs in memory.**  
    - **Adjacency Matrix**, **Adjacency List**, **Incidence Matrix**  

18. **Binary Search Tree (BST) from insertion sequence:**  
    - Insert **11, 47, 81, 9, 61, 10, 12**
      ```
          11
         /  \
        9   47
         \     \
         10    81
           \   /
           12 61
      ```  

19. **Convert infix `(A+B) *(C-D) ^E*F` to postfix.**  
    - **Postfix:** `AB+CD-E^F* *`  

20. **Rank these complexities in increasing order:**  
    - **O(1) < O(log n) < O(n² log n) < O(n⁴)**  

21. **Various asymptotic notations.**  
    - **Big O (O)** → Upper bound  
    - **Big Omega (Ω)** → Lower bound  
    - **Theta (Θ)** → Tight bound  

22. **Why parentheses are needed in infix but not in postfix expressions?**  
    - In **postfix notation**, the order of operations is explicitly defined by operand placement. No need for parentheses.  

23. **Effect of pivot choice on Quick Sort running time.**  
    - A **bad pivot (min or max element)** leads to **O(n²)** worst-case time complexity.  
    - A **good pivot (median)** ensures **O(n log n)** performance.  

24. **Two different forms of hashing.**  
    - **Open Hashing (Chaining)**  
    - **Closed Hashing (Open Addressing)**  

25. **Significance of binary trees in Huffman Algorithm.**  
    - Huffman coding builds an **optimal prefix tree** where frequent characters are stored closer to the root.  

26. **Number of edges in a regular graph of degree `d` and `n` vertices.**  
    - **Total edges = (d * n) / 2**  

27. **Algorithm to obtain connected components of a graph.**  
    ```python
    def DFS(graph, node, visited):
        visited.add(node)
        for neighbor in graph[node]:
            if neighbor not in visited:
                DFS(graph, neighbor, visited)

    def connected_components(graph):
        visited = set()
        components = []
        for node in graph:
            if node not in visited:
                component = set()
                DFS(graph, node, component)
                components.append(component)
        return components
    ```  

---

I have completed all **2-mark** questions. Would you like me to proceed with **7-mark** questions as well?
