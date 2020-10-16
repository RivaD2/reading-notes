# Linked Lists

**What is a linked list anyway?**

- A data structure that contains nodes that links/points to the next node in the list.

**Ok by now we've covered a lot of ground and we know that data structures are are a way to organize data. Before we can understand linked lists, we need to know WHAT type of data structure they are**

1.  Linked list are **linear data structures**, which means that there is a sequence and an order to how they are constructed and traversed. Think of it this way, in order to get to the end of the list, we have to traverse through all items in the list order sequentially. Let's say that each number below is a **node**:
                   Head--->1--->2--->3--->4---->5----->   NULL

-------------------------------

### What other linear structures have you seen? That's right! Arrays are linear data structures!

**But now you may be asking, ok but if both are linear, how does a link list differ from an array?**

- Well, we need to think about memory allocation here. When working with dynamic languages, we need to get down to the basic of how much memory we are using when we write our code.

- What sets linked lists apart is how they store bytes. Linked lists don’t need to take up a single block of memory as they memory they use can be scattered throughout!Arrays on the other hand will need a continuous block of memory.

- Linked lists are also dynamic data structures. They don't need a set amount of memory to be allocated in order to exist. Linked lists are dynamic remember? So that means they can be small or large.

------------------------------

### What Are the components of a linked list?

- **NODES**: Linked Lists are made of a series of nodes, which are just elements in the list.
- **HEAD**: This is the starting point in the list, also known as the head. Think of the head as the entry point.
- The end of the list isn’t a node, but rather a node that points to **null**, or an empty value.
- **NODE COMPONENTS**:  Nodes have two parts: data, or the information that the node contains, and a reference to the next node. **HOW** nodes work is very important.
        - When thinking about Nodes, think about data only. A node really only cares about how much data it holds and which other node it points to.

- **CURRENT**: The current reference is a reference type of type Node that is currently being looked at. This node is typically used when traversing through a full linked list. When traversing, it is common to reset the current to the head to guarantee you are starting from the beginning of the linked list.

**At this point, I've answered why nodes can scatter memory. It is because a single node has the “address” or a reference to the next node. If that is the case, then they do not have to use a continuous block of memory**


**You still with me?**

![confused](https://media.giphy.com/media/uN5iwZB2v2dH2/giphy.gif)


-------------------------------------

### What other types of lists are there?:

1. **Singly linked lists**: These are the simplest type of linked list, based solely on the fact that they only go in one direction. In a singly, we start at the head and end at null. Easy!
1. **Doubly linked list**: When a node holds a reference pointer to its preceding node,this is a doubly linked list. There are two references contained within each node: a reference to the next node, as well as the previous node. This is helpful when we  want to traverse.
1. **Circular linked list**: These lists DON'T end with a node pointing to a null value. Instead, there is a node that acts as the tail of the list , and the node after the tail node is the beginning of the list. We can easily add things here because we can start the traverse at the tail node, as the first element and last element point to one another.

-----------------------------

### TRAVERSAL: No foreach or Loops here my friends!

- When traversing a linked list, you are not able to use a foreach or for loop.
- To traverse, use a `while()` loop. This will allow you to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

- When traversing through a linked list, the Current node is the most helpful. The Current will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.


------------------------------

### What is Big O Notation?:

- Big O Notation is a way of evaluating the performance of an algorithm.
- A way to think about Big O notation is a way to express the amount of time that a function, action, or algorithm takes to run based on how many elements are passed to a function.
- There are two types of Big O equations to remember: O(1) and O(n).
- 0(1): An [O(1)](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996) function takes **constant time**, which which means it doesn't matter how many elements we have, or how huge our input is. It will ALWAYS take the same amount of time and memory to run our algorithm.
- 0(n): An O(n) function is linear, so as an input grows, the space and time that we need to run that algorithm grows linearly. So, the more elements we have here, there is more time and memory is needed.




**Resources:**
-[medium.com](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)