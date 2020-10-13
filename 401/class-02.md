# Classes, Inheritance and Functional Programming

**Let's do a quick recap on the Node Module System and how to create and load a module:**

    - At the core of node is a concept called Modules
    - Node has modules that give us other capabilites. These objects different
    objects than the ones we have access to in our browsers
    - None is non-blocking by nature and a single thread is used to handle multiple requests
    - In node, we do not have the window obj, we have what is called, global
    - Each file in Node is a module and we create different modules hwere are various variables and functions are defined
    - These functions/variables are by default private, or scoped to each file. If we want to use functions/vars outside of a file, we have to export them and load them in the file where we need to use them. To do this, we use the require() function.
    - So,
    1. We define the module
    2. export one or more members
    3. use the require function to load the module
    - Remember, npm comes with Node.js

    **Easy right?**

  ![easy](https://media.giphy.com/media/XHy2u1erzDnAgGiIKp/giphy.gif)

**That you've had a quick recap on Node and how to create/load modules, I will cover some questions related to Node.js and then provide you with some terminology that you may find handy:**

1. Why would you want to run JavaScript code outside of a browser you might ask? The browser is great, don't get me wrong. The fact is though,is that we can do things outside of the browser with Node.js that we can't do inside of a browser:
    - JS becomes even more powerful as we are given the access to API's which have the ability to manipulate the file system and OS
    - We are given CRUD operations (for database management)
    - external packages are load as dependencies once Node.js is installed
    - Node.js has a the largest ecosystem of open source libraries
    - Node is highly scalable and superfast
    - Node is asynchronous or non-blocking by nature
    - **Source code is even cleaner as it is used on the frontend and backend, which is well, pretty darn cool!**

2. What is the difference between a module and a package?
   - It is very common for modules to be called packages and vice-versa. What is the real difference here? According to nopmjs.com:
        - A package is a file or directory that is described by a `package.json` file. A package **must** contain a `package.json` file in order to be published to the npm registry.
        - Packages can be unscoped or scoped to a user or Org, and scoped packages can be private or public
        - A package can come in many [formats](https://docs.npmjs.com/about-packages-and-modules)
    - A **module** is any file or directory in the node_modules directory that can be loaded by the Node.js `require()` function.
    - To be loaded by the Node.js require() function, a module must be one of the following:
        - A folder with a package.json file containing a "main" field.
        - A folder with an index.js file in it.
        - A JavaScript file.


**JUST REMEMBER THIS: Modules are NOT required to have a package.json file, so not all modules are packages. Only modules that have a package.json file are also packages.**


3. What does the node package manager do?
    - NPM is a command line tool and a registry of third party libraries that we can add to our Node.js applications
    - Think about this, any functionality you want to add can most likely be found on [npm](https://www.npmjs.com/)!
    - We use NPM to download and install 3rd-party packages from NPM registry
    - All the installed packages and their dependencies are stored under `node_modules` folders.

4. Provide code snippets showing 3 different ways to export a function from a node module:

**We meed to remember that `exports` is an object. It is empty by default. So,` module.exports` is the variable that is returned from the `require()` function**

- Here a simple string message is exposed as a module:

    `module.exports = 'Hello world'`;

- The exports is an object. So, you can attach properties or methods to it: `exports.SimpleMessage = 'Hello world';`

- Here, I expose an object with function:
`module.exports.log = function (myMsg) {
    console.log(myMsg);
};`

- Here I attach an object to module.exports:
- `module.exports = {
    firstName: 'Riva',
    lastName: 'Davidowski'
}`

- Here, I can expose a function that is treated as a class:

    ```
    module.exports = function (firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.fullName = function () {
          return this.firstName + ' ' + this.lastName;
    }
}

```

-------------------------------------
## FUN WITH NEW VOCABULARY TERMS

- **ecosystem** :
A term used to describe a  community around a software component, library, or tool. This includes the both complimentary tools to that component, active community members willing to help on online channels and support by prominent commercial/official organizations

- **Node.js**:
A runtime environment for executing JS code. It is used to build backend API's that power our client applications

- **V8 Engine**:
It is an open sourced JS/web-assembly engine written in C++. Is the name of the engine that powers Google Chrome,  takes our JavaScript and executes it while browsing with Chrome, and  is **independent of the browser in which it's hosted**

- **module**:
Any file or directory in the node_modules directory that can be loaded by the Node.js `require()` function.

- **package**:
A package is a file or directory that is described by a `package.json` file.

- **node package manager (npm)**:
NPM is a command line tool and a registry of third party libraries that we can add to our Node.js applications

- **server**:
 A computer program or device that provides a service to another computer program and its user, also known as the client. It awaits and fulfills requests from the client(in the client/server model)

- **environment**:
It is exactly what it sounds like. Literally everything installed on your machine which can affect either the development and or testing of your application

- **interpreter**:
A computer program that directly executes instructions written in a programming or scripting language, without requiring them previously to have been compiled into a machine language program.

- **compiler**:
Computer software that translates (compiles) source code written in a high-level language (e.g., C++) into a set of machine-language instructions that can be understood by a digital computer's CPU.