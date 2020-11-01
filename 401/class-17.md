# EVENT DRIVEN APPLICATIONS

![fun](https://media.giphy.com/media/LxdS7fXgbjsGc/giphy.gif)

**What is an event?**
*https://www.bbconsult.co.uk/* says:
> "In programming terms, ‘events’ are actions that can be user-generated – such as mouse clicks and keystrokes – or system-generated, such as a program loading. The events themselves can be anything from accepting or rejecting a loan application (referred to as a high-level event), to ‘a user pressed a key’ (a low-level event). An event-driven application is designed to detect events as they occur, and then deal with them using some event-handling procedure."

1. **Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?** 
   
 - Some examples of back-end events include opening a connection to a server, anything that is an instance of the `EventEmitter` class in Node.js. I would even say that every error is also an event in the back-end.
  
2. **Why are events sometimes better than asynchronous actions with callbacks?**
   
- Events can be better in some cases because they take up less memory and are cleaner than many nested callbacks. You don't have to really keep track of them so every event `event` is idempotent. When one action triggers another action, events ensure that the second action will always take place. Asynchronously, I would have to program that second event in the callback of the first every single time!
   
3. **What does an EventEmitter instance do?**
   
- *Medium.com* provides a perfect explanation:
  >"Your event emitter sends out a certain event to any method that is waiting to react to it. Just like in a radio stations broadcast, nobody has to be listening in order to actually broadcast the event, but if there are no listeners then nothing happens.
- Using the EventEmitter class involves signaling that event has happened by passing an arg which is the name of event
        - typically with an event, we want to send some sort of data
        - To send multiple values in an event, encapsulate those values in an obj.
        - In the event listener, the function would receive the arg used in event
        - Typically the arg is called arg, or eventArg
        - Because we will also use the keyword 'extends'  with the Event Emitter class, we can use the keyword 'this'
        - In this class, we can directly emit or raise events
   
1. **When is a program’s call stack, event queue, and event loop active?**
   
- When there is stuff to do! Or, a better way to say this is if there is asynchronous code to be executed, the code gets moved into the event queue, the code then waits for execution,then the event loop checks if it has anything to execute. If it doesn't, then it checks the Callback queue and if Callback queue has code to execute then it pops the code from it to the Main Stack for execution.

### New Vocabulary to Learn:

- **Observer Pattern:** [jsmanifest.com](https://jsmanifest.com/observer-pattern-in-javascript/) says, 
  >"The observer pattern is a design pattern in which subjects (which are simply just objects with methods) maintain a list of observers who are "registered" to be notified of upcoming messages. When they receive some notification event about something from the subject they are attached to, they can use these opportunities to do something useful depending on what was received from the them.

The pattern is most useful in situations when you need multiple objects to get notified simultaneously at the same time of recent changes to state."

- **Listener:** This is usually a  JavaScript function which respond to the event that is occurring.
- **Event Handler:** A block of code (usually a JavaScript function) that runs when the event fires. [MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#:~:text=Each%20available%20event%20has%20an,are%20registering%20an%20event%20handler) says, "When such a block of code is defined to run in response to an event, we say we are registering an event handler"
  
- **Event Driven Programming:** Is basically utilizing various types of event listeners to carry out actions in code rather than relying on an explicit chain of instructions. Event Driven Programming says that each even listener can be self contained which means a programmer no longer has to track every single behavior of every listener and doesn't need to know HOW they are implemented. They just know that the event will be implemented! Game changer!
  
- **Event Loop:** The event loop is responsible for executing code, collecting and processing events, and executing queued sub-tasks.
  
- **Event Queue:** This queue holds all the events that have been heard and holds them until the event loop checks it.
- **Call Stack:** In simple terms, it is a list function executions. It is primarily used for function invocation (call) and is considered to be synchronous. 
  
- **Emit/Raise/Trigger:** Well, these relate to using `EventEmitter`. For example, the `eventEmitter.emit()` method is used to trigger the event.

- **Subscribe:** This is a method relating to observables. This method appears to insert callbacks.

