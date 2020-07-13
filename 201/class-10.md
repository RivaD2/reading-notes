![Buffy](https://media.giphy.com/media/JszzkKOlV6gTK/giphy.gif)

# When Everything Is Wrong | Debugging 
### Look, like any language, JavaScript is hard and mistakes will be made. So, let's talk about ways to find errors in your code!

#### We talked about scripts earlier and how they are processed. It is important to remember the following:
* Statements can be executed in different orders
* Some tasks are unable to be completed until other functions or statements have been run
* The interpreter uses the concept of **EXECUTION CONTEXTS**. There is one global execution context and each function creates another one. They are tied to variable scope

**We talked about how the interpreter runs through code one line at a time...SO, when a statement needs data from another friendly function, the interpreter says, "Hey, move to the front of the line!". It stacks that new data, or function on top of the current task.**

------------
### TYPES OF ERRORS AND HOW TO DEAL WITH THEM

* If a statement produces an error, an **EXCEPTION** is thrown
* Whenever this happens, the interpreter will look for error-handling code and if there is none, it will stop running
* Error objects can help you locate mistakes and browsers have tools within them to help you figure them out

**There are 7 different types of built-in error objects:**
1. Error: this is generic
1. SyntaxError: proper syntax hasn't been followed
1. ReferenceError: A variable has not been declared within scope
1. TypeError: An unexpected data type that can't be coerced
1. RangeError: Numbers are not in an acceptable range
1. [URIError](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/URIError): methods used incorrectly
1. EvalError: `eval()` function used incorrectly

### Ok, so how do we deal with errors now that we know what errors are?

* Once an error has been made, we can debug the script to fix them and handle erros in a graceful manner (Sounds silly right? Learn about the "try", "catch" and "finally" [statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch))
* The developer tools are available in every browser out there today and can help us on our debugging journey ahead
* Look, errors happen and sometimes they might not be something we could have prevented so, we will need to make sure we have written error handling-code
--------------
### DEBUGGING IS ABOUT DEDUCTION...
![AndyS](https://media.giphy.com/media/xT5LMMg8TfVQvl5wUE/giphy.gif)

### Let's go over the workflow for techniques that help us to find errors in our code:
* **Where is the problem?** This is a good place to start as this helps to narrow down where the issues seems to occur
  * Where does the error message even occur?
  * What TYPE of error is there?
  * Check how far the script has run
* What is **REALLY** the problem?
  * This is where you try and pinpoint the exact line of code that could be the culprit
  * Setting breakpoints can help you to locate any variables have values that don't belong
  * **TAKE A BITE OUT OF IT AT TIME**...separate the code into chunks and test smaller pieces to give them the green light
  * Check all functions and parameters
* **KEEP NOTES** of what has been tested/worked and what hasn't been tested. It is easy to get lost in all that fun problem solving!
* The JS console can be extremely helpful in identifying bugs and is foung by accessing the dev tools or by right-clicking and selecting inspect
* Console-logging is yet another way to identify bugs and get a clearer picture as to what has gone wrong

### There is a lot to learn about debugging and practice will get you far but there is no way to ensure perfection. We have to use the tools at our desposal and luckily, there are many out there that can help us!

**TO LEARN MORE ABOUT JS DEBUGGING CLICK [HERE](https://raygun.com/javascript-debugging-tips)!