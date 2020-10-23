# More DATA STRUCTURES: Stacks and Queues

![Stacks and Queues](https://media.giphy.com/media/5dYeglPmPC5lL7xYhs/giphy.gif)

You may be familiar with various types of [data structures and alorithms use to solve them](https://egghead.io/courses/data-structures-and-algorithms-in-javascript). Sets, hash tables, linked lists and binary search trees are all a part of the game. Today, let's talk about stacks and queues!

**WHAT IS A STACK?**

A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

**WITH STACKS, WE CAN:**

- **Push** nodes or items into the stack
- **Pop** nodes or items that off a stack. (When you attempt to pop an empty stack an exception will be raised.)
- **Top** just referes to the  top of the stack.
- **Peek** to view the value of the top Node in the stack. Peeking will also raise and exception.
- **IsEmpty** will returns true when stack is empty otherwise returns false.

**STACKS FOLLOW THESE CONCEPTS**

1. **FILO** First In Last Out
- The first item added in the stack will be the last item popped out of the stack.

1. **LIFO**
- Last In First Out
- The last item added to the stack will be the first item popped out of the stack.

HOW TO SEE HOW IT WORKSs:

- Well, with linkedlist we have the keyword **next**
- With stacks, when we push something into the stack, it becomes the new top. When we pop something from the stack, **YOU POP THE TOP** and set the **NEXT TOP** as **top.next**
- **Pushing** a Node onto a stack will always be an O(1) operation as it takes the same amount of time no matter how many Nodes (n) you have in the stack.
- When adding a Node, you **push it into the stack by assigning it as the new top, with its next property equal to the original top.**
- **Popping a Node off a stack** means removing a node from the top. With a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
- As I mentioned earlier, peeking means inspecting the top Node of the stack. With a peek, the **next property is not reassigned because we need the reference to the next Node in the stack. This way, the top will stay the top until we decide to pop.

**TIP**

**BEFORE USING POP, check isEmpty first! This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block. You will also want to check isEmpty before a Peek. **

-----------------------------------
## QUEUES

**Let's cover some vocabulary first:**

1. **Enqueue** are Nodes or items that are added to the queue.
1. **Dequeue** are Nodes or items that are removed from the queue. If the queue is empty when call is made, an exception will be raised.
1. **Front** is the front/first Node of the queue.
1. **Rear** refers to the rear/last Node of the queue.
1. **Peek** allows you to view the front node in the queue. If you call it when the queue is empty, an exception will be raised.
1. **IsEmpty** returns true when queue is empty otherwise returns false.

**WITH QUEUES WE CAN: Enqueue and DeQueue**

![Queue actions](https://java2blog.com/wp-content/uploads/2017/09/Queue.png)

**TIP:**
Likes stacks, Enqueus and Dequeues are done with an 0(1) operation. When you use dequeue, you would also want to check isEmpty before performing this action. This way, no exception will be raised and you can go on your merry way!

- Queues also abide by the rules of FILO and LILO

------------

**Resources**
1. [https://codefellows.github.io/](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)