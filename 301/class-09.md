# Functional Programming | Refactoring Code 
![programmer](https://media.giphy.com/media/349qKnoIBHK1i/giphy.gif)
**Ah yes, functional programming, we all know it to be another programming paragigm. Let's talk more about this hot topic and some of core concepts.**

## What is functional programming?
* Functional programming or FP, is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. 
* Functional programming is declarative rather than imperative, and application state flows through pure functions. Contrast with object oriented programming, where application state is usually shared and colocated with methods in objects.
* Functional code tends to be more concise, more predictable, and easier to test than imperative or object oriented code.

**Before we talk about FP, let's revisit what a **function** is, and what can be accomplished by using them**:

### A function is a process which takes some input, called arguments, and produces some output called a return value. Functions may serve the following purposes:

* **Mapping:** Produce some output based on given inputs. A function maps input values to output values.
* **Procedures:** A function may be called to perform a sequence of steps. The sequence is known as a procedure, and programming in this style is known as procedural programming.
* **I/O:** Some functions exist to communicate with other parts of the system, such as the screen, storage, system logs, or network.

## Let's look at the core concepts of FP:

1. **Pure functions**
1. **Function composition**
1. **Avoid shared state**
1. **Avoid mutating state**
1. **Avoid side effects**

* **PURE FUNCTIONS:** A function which given the same inputs, always returns the same output, and has no side-effects. Pure functions have many beneficial properties, and form the foundation of functional programming. 
* Pure functions make function calls completely independent of other function calls, which simplifies changes and refactoring. A change in one function, or the timing of a function call won’t ripple out and break other parts of your program.

## A function is only pure if, given the same input, it will always produce the same output. 

**Here's a good example of a pure function:**
```
const highpass = (cutoff, value) => value >= cutoff;

highpass(5, 5); // => true
highpass(5, 5); // => true
highpass(5, 5); // => true

// The same input values will always map to the same output value
```
* **FUNCTION COMPOSITION:** [Function composition](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-function-composition-20dfb109a1a0) is the process of combining two or more functions in order to produce a new function or perform some computation.

* **SHARED STATE:** Shared state is any variable, object, or memory space that exists in a shared scope, or as the property of an object being passed between scopes. A shared scope can include global scope or closure scopes.
* The problem with shared state is that in order to understand the effects of a function, you have to know the entire history of every shared variable that the function uses or affects.
* When you avoid shared state, the timing and order of function calls don’t change the result of calling the function. 

* **IMMUTABILITY:** An [immutable object](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)is an object that can’t be modified after it’s created. Conversely, a mutable object is any object which can be modified after it’s created.
* In other functional programming languages, there are special immutable data structures called trie data structures (pronounced “tree”) which are effectively deep frozen — meaning that no property can change, regardless of the level of the property in the object hierarchy.

* **SIDE EFFECTS:** A side effect is any application state change that is observable outside the called function other than its return value. Side effects include:
1. Modifying any external variable or object property (e.g., a global variable, or a variable in the parent function scope chain)
1. Logging to the console
1. Writing to the screen
1. Writing to a file
1. Writing to the network
1. Triggering any external process
1. Calling any other functions with side-effects1

* Side effects are mostly avoided in functional programming, which makes the effects of a program much easier to understand, and much easier to test.

## FP utilitzes higher order functions. A higher order function is any function which takes a function as an argument, returns a function, or both. 
**Read more about higher order functions [here](https://eloquentjavascript.net/05_higher_order.html)**

----------------------
## We covered some ground on functional programming. Now let's look into REFACTORING. Luckily, refactoring is much easier thanks to functional programming
![Tom](https://media.giphy.com/media/CzbiCJTYOzHTW/giphy.gif)

>There's a middle ground between speed and comprehension and that's where good code lives.
>
### Do we really want to leave our code messy due to tight deadlines on projects? The answer is NO. Like a cook in a kitchen, it is much easier to clean as we go. So, let's take that dirty code and refactor it.

## What is refactoring?

* Refactoring is a systematic process of improving code
without creating new functionality that can transform
a mess into clean code and simple design.

## What is clean code anyway?

* Clean code is code that is easy to read, understand and maintain. Clean code makes software development predictable
and increases the quality of a resulting product.

## How do we refactor our code, how does it all work? 

* Performing refactoring step-by-step and running tests after each change are key elements of refactoring that make it
predictable and safe.
1. Composing Methods: Much of refactoring is devoted to correctly composing methods but also making sure that they are streamlined.
1. Moving Features between Objects: This involves functionality between classes, creating new classes, and hiding implementation details from public access.
1. Organizing Data: This involves data handling, replacing primitives with rich class functionality,  and untangling of class associations, which makes classes more portable and reusable.
1. Simplifying Conditional Expressions: Conditionals tend to get more and more complicated in their logic over time. This involves taking multiple conditionals that lead to the same result or action and consolidating all of them into ONE single expression.
1. Simplify Method Calls: Here we can rename methods, add or remove parameters, separate queries from modifiers and preserve whole Objects.
1. Deal with Generalization: For example, this could involve replacing delegation with inheritance and forming template methods.

**Please check out some of the links I used to reference the information above. There is so much more to learn about functional programming and refactoring:**

* [Refactoring Techniques](https://refactoring.guru/refactoring/techniques/dealing-with-generalization)

* [Master the Javascript Interview: What is functional Programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)

* [Refactoring JS for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)