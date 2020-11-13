# REACT PROPS & STATE

![awesome](https://media.giphy.com/media/MCKQEmHkUyGf6/giphy.gif)

### In the previous reading, I touched on React Components. If you remember, components are a feature that make up a piece of the user interface. They really describe any composable behavior, and this includes rendering, lifecycle, and state.According to [reactjs.org](https://reactjs.org/):
> "props (short for “properties”) and state are both plain JavaScript objects. While both hold information that influences the output of render, they are different in one important way: props get passed to the component (similar to function parameters) whereas state is managed within the component (similar to variables declared within a function)."


#### Read more about [component based UI](https://rivad2.github.io/reading-notes/401/class-26.html)

**Let me answer some questions you may have**

1. **Does a deployed React application require a server?** 
No, as React builds the virtual DOM and does its operations on the client's browser. It implements front-end Views (MVC View) of their web applications. However, you can use Node.js to render them on the server side if you like.

2. **Why do we prefer to test a React application at the behavior rather than the unit level?**
Unit testing tests units of code in isolation from the rest of the application and they work great to learn whether or not individual parts of an application work. However with React, we need to test the units in integration with the rest of the app, from the perspective of the user interacting with the UI. Because React is component based, we really need to ensure everything works as a whole system.

3. **What does npm run build do?**
    - `npm run build` creates a build directory with a production build of your app. 
    - So first we create our React app by running `npm install -g create-react-app`.  
    - Then we create our app by running `create-react-app my-react-tutorial-app`. 
    - That creates a boilerplate for our app and then `npm run build` builds our application for production to the build directory. [pluralsight.com](https://www.pluralsight.com/guides/npm-start-for-react-tutorial-project) says, "The "build" folder would contain all the static files which can be directly used on any web server. Also, the build command transpiles our source code into code which the browser can understand."
  
4. **Describe the actual composition / architecture of a React application**
Well I already mentioned that React is component based so it is super important that we write components that work well together. With this in mind, we can focus on buiding our file structure out by grouping by features or routes, OR we can do it by focusing on file type. We can also go a bit further by separating out components into different folders. I think it is important as well to consider the nesting aspect of a React app. How deep do we really need to go. I would say that composition is best kept simple.


**TIME TO LEARN NEW VOCABULARY**

- **BDD:** 
Stands for Behavor Driven Development and it is a process involves the definition of entities, events, and outputs that the users care about, and giving them names that everybody can agree on. It is a branch of TDD.

- **Acceptance Tests:** 
Also called functional testing, tests outcome, not logic. Acceptance testing provides an additional level of protection against bugs.

- **mounting:** 
In React.js we will see things like `componentDidMount()` and `componentWillMount()`. React figures out how to modify the DOM to match what the components want to be rendered on the screen and it does this by mounting.
We can only be sure a component is output/rendered when it is mounted.

- **build**
 Well there are two ways this is used. It can be used as a version of a program or can refer to using a build tool. In this case, it means to create from source code software assembly which someone or something can use.
