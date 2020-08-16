![Node](https://live.staticflickr.com/3848/14619855827_2ea3b9f92d.jpg)
## What is Node.js? 
> According to Stack Overflow, Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.
>
**Ok, but what does that all mean really?**
* Well, what this means is that Node.js is strongest at fast, scalable network applications.
* Software developers use I/O to describe how a program will function, depending on what a user enters, so let's keep this in mind as we learn about Node.js
* Node Is Built on Google Chrome’s V8 JavaScript Engine and it is responsible for compiling JavaScript directly to native machine code that your computer can execute.
* Long story short, Node.js is a program we can use to execute JavaScript on our computers.

**If you'd like to install Node.js, click [here](https://nodejs.org/en/download/package-manager/) to learn how**

-----------


## How does it work? 
![how](https://media.giphy.com/media/10yIEN8cMn4i9W/giphy.gif)
* Node.js operates on a single-thread, using non-blocking I/O calls, allowing it to support tens of thousands of concurrent connections held in the event loop.
* I/O stands for Input/Output
* With every input to a computer, there is a output
* The computer's CPU handles all I/O operations and it sends data it receives to the correct path. The path may be to the video card, to the hard drive, or to the RAM for example.

## Let's Talk about NPM the JavaScript Package Manager
* Node is bundled with a package manager called npm and you can check which version of Node you have installed by using  `npm -v`.
* You can install a package locally or globally with npm
* According to Node.js.org:
>Node is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management. 
>
* What are dependencies you might ask? Well, dependencies refer to when a piece of software relies on another one.
* When you have a node project with a package.json file, you can run npm install from the project root and npm will install all the dependencies listed in the package.json. This makes installing a Node.js project from a git repo much, much easier! 
* Node.js is super powerful and is single-threaded. It’s also is event-driven, which means that everything that happens in Node is in reaction to an event.









## Why should you use it? 
1. It makes it really fast to build real-time, high-traffic apps (eg. chats or gaming).
1. It makes it possible to code in JavaScript for both the client and server side 
1. It increases the efficiency of the development process as it fills the gap between frontend and backend developers 
1. NPM (Node Package Manager) gives developers multiple tools and modules to use, thus further boosting their productivity,
as code executes faster than in any other language,
1. Node is perfect for micro services which are a popular solution among enterprise applications.

 **There is so much to learn about Node.js. There are countless articles out there to guide you through the the world of Node.js and NPM. Some of the ones I used to reference are:**
* [sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js/)
* [toptal.com](https://www.toptal.com/nodejs/why-the-hell-would-i-use-node-js)
* [monterail.com](https://www.monterail.com/blog/nodejs-development-enterprises)