**Detailed Answers to 7-Mark Questions**

### **Unit V**

#### **17. Graphs & Minimum Spanning Tree Algorithms**

A **Graph** is a data structure consisting of **vertices (nodes)** and **edges (connections between nodes)**. Graphs can be **directed** or **undirected** and may have weighted or unweighted edges.

A **Minimum Spanning Tree (MST)** is a subset of a connected, weighted graph that includes all the vertices with the minimum possible total edge weight and without any cycles. Two primary algorithms used to find the MST are **Prim’s Algorithm** and **Kruskal’s Algorithm**.

#### **Prim’s Algorithm (Greedy MST approach)**
Prim’s Algorithm is a **greedy algorithm** that finds the MST by continuously adding the smallest edge that expands the current tree.

**Steps:**
1. Start from an arbitrary vertex.
2. Select the smallest edge connecting to an unvisited vertex.
3. Repeat until all vertices are included.

**Time Complexity:** O(E log V) using a priority queue.

**Example:**
1. Start with vertex A.
2. Pick the smallest edge.
3. Continue until all vertices are included.

#### **Kruskal’s Algorithm (Edge-based MST approach)**
Kruskal’s Algorithm sorts all edges in increasing order and selects edges one by one, ensuring no cycles are formed.

**Steps:**
1. Sort all edges by weight.
2. Pick the smallest edge, ensuring no cycle is formed.
3. Repeat until (V-1) edges are included.

**Time Complexity:** O(E log E) due to sorting.

**Example:**
1. Sort edges.
2. Pick the smallest edge.
3. Continue until MST is complete.

#### **18. Floyd-Warshall Algorithm**
The **Floyd-Warshall Algorithm** finds the shortest paths between all pairs of vertices in a weighted graph. It uses dynamic programming and progressively updates distances.

**Steps:**
1. Initialize a distance matrix with direct edge weights.
2. Consider each vertex as an intermediate point.
3. Update distances using the relation:  
   `dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j])`

**Time Complexity:** O(V³)

**Example:**
1. Given a weighted graph, initialize a matrix.
2. Compute shortest paths iteratively.

#### **19. Dijkstra’s Algorithm**
Dijkstra’s Algorithm finds the shortest path from a **single source vertex** to all other vertices in a graph with **non-negative edge weights**.

**Steps:**
1. Assign all vertices a distance of infinity, except the source vertex (0).
2. Pick the vertex with the smallest tentative distance.
3. Update the distances of adjacent vertices.
4. Repeat until all vertices are visited.

**Time Complexity:** O(V²) using an adjacency matrix or O(E log V) using a priority queue.

**Implementation:**
```c
void dijkstra(int graph[V][V], int src) {
    int dist[V];
    for (int i = 0; i < V; i++) dist[i] = INF;
    dist[src] = 0;
    // Further implementation for priority queue processing
}
```

#### **20. B-Trees and B+ Trees**
A **B-Tree** is a balanced search tree with multiple children per node, reducing the depth and making operations efficient.

**Operations in B-Trees:**
- **Insertion:** Keys are inserted in sorted order.
- **Deletion:** Merges nodes when necessary to maintain balance.
- **Search:** Similar to binary search but generalized for multiple children.

**B+ Tree vs. B-Tree:**
- In a **B-Tree**, keys and values are stored in all nodes.
- In a **B+ Tree**, internal nodes store only keys, and all values are stored in leaf nodes.

**Example Construction:**
1. Start with an empty tree.
2. Insert keys while maintaining the balance.
3. Split nodes when they exceed the maximum allowed keys.

#### **21. Graph Representations & Applications**
Graphs can be represented using different methods:

1. **Adjacency Matrix:** A 2D array where `matrix[i][j]` stores the weight of the edge between vertex `i` and `j`. 
   - Space Complexity: O(V²)
   - Efficient for dense graphs.

2. **Adjacency List:** Each vertex maintains a list of its neighboring vertices.
   - Space Complexity: O(V + E)
   - Efficient for sparse graphs.

**Applications of Graphs:**
- **Networking:** Routing and shortest path algorithms.
- **Social Media Analysis:** Modeling user connections.
- **AI and Machine Learning:** Graph-based recommendation systems.
- **Biology:** Protein interaction networks.
- **Cybersecurity:** Analyzing attack paths in network security.

---

This section now provides detailed explanations of each concept with examples, algorithms, and real-world applications.

