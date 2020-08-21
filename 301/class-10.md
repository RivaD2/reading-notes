# THE CALL STACK AND DEBUGGING
## What is a call stack and why do we need it? In the JS engine, there is function hierarchy and execution order. Let's learn more!
![call stack](https://miro.medium.com/max/748/1*-MMBHKy_ZxCrouecRqvsBg.png)

What is the call stack?
* It is is primarily used for function invocation (call).
* Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It is **synchronous**.
* It is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
* LIFO means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.
* When a function is invoked (called), the function and everything with it (its parameters and variables) are pushed into the call stack to form a stack frame. 
* This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
* The call stack remembers the position of each stack frame and the next function to be executed.
* After execution, the call stack will remove the function, thus making it synchronous.


## While each operation is being processed, nothing else can happen — rendering is paused. This is because JavaScript is single threaded. Only one thing can happen at a time.

## What is a stack overflow?
* A stack overflow happens when a recursive function (a function that calls itself) without an exit point. 
* The browser (hosting environment) has a maximum stack call that it can accommodate before throwing a stack error. Let's see an example:
```
function callMyself(){
  callMyself();
}

callMyself();
```
* The `callMyself()` will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.

## Understanding how the call stack works is important and is vital to Asynchronous Programming
* We have a callback function, an event loop, and a task queue. This is **Asynchronous JS**.The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

How does Asynchronous Programming and the call stack tie in to Web API features?
* Many Web API features now use asynchronous code to run, especially those that access or fetch some kind of resource from an external device ( for example, accessing a database and returning data from it).
* Asynchronous callbacks are functions that are specified as arguments when calling a function which will start executing code in the background. When the background code finishes running, it calls the callback function to let you know the work is done, or to let you know that something of interest has happened.
* When we pass a callback function as an argument to another function, we are only passing the function's reference as an argument, i.e, the callback function is not executed immediately. It is “called back”  asynchronously somewhere inside the containing function’s body. 

**Remember event listeners? They can hold a perfect example of an asynchronous callback function:**
```
btn.addEventListener('click', () => {
  alert('You clicked me!');

  let pElem = document.createElement('p');
  pElem.textContent = 'This is a newly-added paragraph.';
  document.body.appendChild(pElem);
});
```
**In the above example, the first parameter is the type of event to be listened for, and the second parameter is a callback function that is invoked when the event is fired.**

## As we move into learning about the client-server relationship and API's, we will see a new kind of Asynchronous function...PROMISES.
* We see [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) used in modern Web APIs. A good example is the fetch() API, which is basically like a modern, more efficient version of XMLHttpRequest.

**Please click down below to read more about the call stack and asynchronous functions. I used the articles below to reference the material for this reading:**

1. [The JS call stack, what is it and why it's necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
2. [Understanding JS function executions: call stack ,event loop, tasks and more](https://medium.com/@gaurav.pandvia/understanding-javascript-function-executions-tasks-event-loop-call-stack-more-part-1-5683dea1f5ec)
3. [Introducing Asynchronous JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing)