# Another Data Structure - Graphs

**What is a Graph you ask?**
A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

**Terms you should familarize yourself with:**

1. **Vertex** - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
2. **Edge** - An edge is a connection between two nodes.
3. **Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. **Degree** - The degree of a vertex is the number of edges connected to that vertex.

**What types of Graphs are there?**

There are **Undirected** graphs and *Directed** graphs:

    - An Undirected Graph is a graph where each edge is undirected or bi-directional. It does not move in ANY direction
    - A directed Graph (A.K.A DiGraph) is one in which every edge is directed. Each edge in this graph has a direction. Each node is directed at another node with a specific requirement of what node should be referenced next.
    - There are also complete graphs, disconnected connected graphs as well as cyclic and acyclic graphs

![confused](https://media.giphy.com/media/gKsJUddjnpPG0/giphy.gif)


**How do we represent Graphs**

We represent graphs through:

    - Adjacency Matrix: An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix
    - Adjacency List: This way is a much more common way to represent graphs. It is basically a collection of linked lists or it could be an array that lists all of the other vertices that are connected. This graph makes it much easier to see vertices that are connected to one another

**Can we Traverse a Graph?**

Why yes, yes you can! The traversals are similar to traversals of trees. We can utilize the following traversal methods:

    - Breadth First
    - Depth First
