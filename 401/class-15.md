# TREES | ANOTHER DATA STRUCTURE

**WHAT ARE TREES?**

![ent](https://media.giphy.com/media/ZvGFBHVxrqola/giphy.gif)

Trees are a form of data structure. They consist of connected parent nodes and their children. 
Like a linked list, every tree has a head node, with children below them. In a basic tree, there is no limit to how the number of children a parent can have.


**HOW DO WE SET THEM UP**
- In JS, we can set a tree up using a constructor function:
- 
```
function Tree (data) {
 var node =  new Node (data)
 this._root = node
}
function Node (data) {
  this.data = data
  this.parent = null
  this.children = []
}
var myTree = new Node('First Node')
````
- To do anything with a tree, we must first create/add nodes to the tree. We
can add nodes using the `prototype` method.

**WHEN THEY ARE SET UP, WHAT ELSE CAN WE DO WITH THEM?**

- Once the tree is set up, we need to be able to navigate, or traverse its data. There are two ways we can do this, **Breadth First Search (or BFS)** and **Depth First Search (or DFS)**. To get a better understanding of the ways we can traverse, click [here](https://medium.com/basecs/breaking-down-breadth-first-search-cebe696709d9)

- A simple way to describe DFS is saying that we will traverse down through the subtrees of a binary search tree.
- A BFS is all about traveling down the tree section by section — or, level by level. *Vaidehi Joshi at Medium.com* says this about BFS:

>We traverse through one entire level of children nodes first, before moving on to traverse through the grandchildren nodes. And we traverse through an entire level of grandchildren nodes before going on to traverse through great-grandchildren nodes.
 

- The Breadth First Search method keeps a store of its traversed nodes using a stack, and that Depth First Search keeps it all together using a queue.

- The major difference in depth-first search and breadth-first search is the data structure used to implement both of these very different algorithms. While DFS uses a [stack data structure](https://rivad2.github.io/reading-notes/401/class-10.html), BFS leans on the [queue data structure](https://rivad2.github.io/reading-notes/401/class-10.html). 


**NEW VOCABULARY TO LEARN**


1. **Node**: A node is the individual item/data that makes up the data structure
2. **Root**: The root is the first/top Node in the tree
3. **Left Child**: The node that is positioned to the left of a root or node
4. **Right Child**: The node that is positioned to the right of a root or node
5. **Edge**: The edge in a tree is the link between a parent and child node
6. **Leaf**: A leaf is a node that does not contain any children
7. **Height**: The height of a tree is determined by the number of edges from the root to the bottommost node

-----------------------
**RESOURCES**
- [medium.com](https://medium.com/@iampika/javascript-trees-b8f3b4261c3a)
- [codefellows.github.io](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)