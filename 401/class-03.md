# Test Driven Development /OOP and Higher Order Functions

**A quick recap on test driven development**

![Testing](https://media.giphy.com/media/ZY2DmHSTFpmmEH5STD/giphy.gif)

1. **3 advantages to Test Driven Development:**

TTD creates a metric for  quality that can be easy and quick and allows to us to see if there are any functional issues. It also is an advantage as it allows us to have record of our code's functionality and allows for safe refactors of code.


2. **When do you use beforeEach() or afterEach() in a test suite?**

According to [jestjs.io](https://jestjs.io/docs/en/setup-teardown), if you have some work you need to do repeatedly for many tests, you can use `beforeEach()` and `afterEach()`.  They also can handle asynchronous code in the same ways that tests can handle asynchronous code - they can either take a done parameter or return a promise so this is especially helpful when working with databases.

3. **What is one downside of Test Driven Development?**

 According to [devqa.io](https://devqa.io/pros-cons-test-driven-development/) the tests may be hard to write, esp. beyond the unit testing level. At first, TTD slows down development(But in the long run, it actually speeds up development). With anything in the programming world, there is a big difference between doing it well and then writing one that is full of fluff/messy.  Writing good unit tests is an art form! With anything TTD takes time to learn and it can be easy to spend too much time on the test suite.

4. **What’s the primary difference between ES6 Classes and Constructor/PrototypeClasses?**

Ok, ok this is a touchy subject. JS object system is usually based on prototypes, not classes. With the introduction of ES6, things changed and we now see the word `class` being used frequently. **Class inheritance** says class is like a blueprint — a description of the object to be created. Classes inherit from classes and create subclass relationships. **Prototypal Inheritance** means a prototype is a working object instance. Objects inherit directly from other objects.So, the **primary difference** is that class taxonomies are not an automatic side-effect of prototypal OO. Read more about this on [medium.com](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

5. **Name a use case for a static method**
What is a static method you might ask? JS provides methods that belong to the class instead of an instance of that class. An instance is not required to call the static method. These methods are called directly on the class itself. It looks like this:

```
class Foo(){
   static methodName(){
      console.log("bar")
   }
}
```
**Long story short, a use case for Static methods sis when we want to create utility functions for an application. In other words, static methods have no access to data stored in specific objects. Read more [here](https://medium.com/@yyang0903/static-objects-static-methods-in-es6-1c026dbb8bb1)

6. **An example of a Higher Order function and description of the use case it solves:**
Ok, let's say I have an array with nums as input. I really need the average value. Let's take a look:
```
const calculateAverage = (arr) => {
 /*start with zero and one by one add each value of the array to our initial value until
  we’ve looped through the entire array. When done, the accumulator value will be returned*/

  const averageOfValues = arr.reduce((acc,curr) => {
    // Here I said that we will loop through the array of nums and add them all together
    return acc + curr;
  },0)
  //Once I have added them all together and divided them by the total number of numbers (length of the array)
  return averageOfValues/arr.length;
};

```
**When composing an operation, higher order functions like `reduce()` shine especially when we use data sets.**

_________________________________________________

## NEW VOCABULARY!

![Vocab](https://media.giphy.com/media/3orieYwoZPWQ1myQ00/giphy.gif)

- functional programming: According to *medium.com* FP is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Code becomes concise, predicable and easy to test.

- pure function: A function that when given the same inputs, always returns the same output, and
has no side-effects

- higher-order function: A function that takes a function as an argument, or returns a function

- immutable state: Basically referes to the state of an object and means it  cannot be modified after it is created

- object: JavaScript objects are containers for named values called properties or methods. Really everything in JS is an object that has key value pairs.

- object-oriented programming (OOP): On a simple level, using objects to model real world things that we want to represent inside our programs

- class: A class is a blueprint of an Object and are a higher form of constructors and protos

- prototype: The prototype is an object that is associated with every function and object. The prototype holds all methods that can be used multiple times.

- super: A keyword used in OOP that calls the parent method from child method. It is used to call the constructor of the parent class and to access the parent's properties and methods.

- inheritance: At a basic level, inheritance is the concept of one thing gaining the properties or behaviours of something else.

- constructor: THEY FORM THE BASIS FOR EVERYTHING! They set the initial props of the object they create and constructors hold a template and multiple objects out of the template that the constructor holds.

- instance - With constructors, the object instance inherits all props/methods from the constructor. An instance contains data and behavior described by a class and usually means that the `new` keyword was used

- context: Context is related to objects. It refers to the object within the function being executed

- this: is refers to the object that the function is executing in

- Test Driven Development (TDD): A basic definition is TTD is just writing software where you write tests before you write application code.

- Jest: According to *jestjs.io*, Jest is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase. It allows you to write tests

- Continuous Integration (CI): The practice of merging all developers' working copies to a shared codebase several times a day

- unit test: A unit test runs over segments of our programs checking the input and output. These tests allow developers to check individual areas of a program to see where(and why) errors occur.
