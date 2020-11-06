# COMPONENT BASED UI : 

![meaning](https://media.giphy.com/media/hhIpUr1UTF2JG/giphy.gif)

**Let's begin by speaking about what it means to shift away from page-based to component-based design. As we know a website is a collection of pages and really, you've seen components already before. A login page vs a cart page etc.**

## If we start to think about every UI elements and their state, we can start to understand components

### WHY USE COMPONENTS?

I think that *itnext.io* says it best:
>Modern web technologies like components allow organizations to speed up and scale the development of web applications, create simple and decoupled codebases for autonomous teams, allow smooth integrations, increase the number and page of independent team releases, and allow more code reuse.

>Component-driven development means embracing components as the new primitive of the web, and tapping into their modular power to achieve better speed, scalability, and standardization for web application development.

**BUT WAIT, WHAT ARE COMPONENTS?**

**Components** are a feature that make up a piece of the user interface. Let's think about a portfolio page for a programmer. What do you think each component would/could be? Well if they have modals, a modal component. If they have a login, a login page, they would have a login component. If there were a main page, like a projects page, they would have a projects page component. Do you see where I am going here?

Each of those components would exist in the same space, yet interact independently from one another. 
As [medium.com](https://medium.com/@dan.shapiro1210/understanding-component-based-architecture-3ff48ec0c238) says, ..."Components have their own structure, their own methods and their own APIs. Components are also reusable and can be “pasted” into interfaces at will. The independent nature of components allows for developers to create a UI with many different moving parts."

- There are two types of react Components: 
  - Class Components which have constructor and render etc.
  - Functional Components which are just functions that return the render value of the Component

**What are some keywords associated with Component based UI?**

- Well **rendering**, **props** and **state** are all important words to know. Each component is combo of JS and HTML and there are two things that components have that make them React components:
        - **props: is how a parent communicates to child. They are read only from childs perspective. It is also a React word for data that is passed into a Component
        - **state: how a component manages itself so it can read, write, edit its own state and no other
                components know about its state**
- Each componenet is self-contained and props are how they can be connected
- **Rendering** according to[blog.isquaredsoftware.com](https://blog.isquaredsoftware.com/2020/05/blogged-answers-a-mostly-complete-guide-to-react-rendering-behavior/) describes rendering as, ..." the process of React asking your components to describe what they want their section of the UI to look like, now, based on the current combination of props and state."
  
 **As I mentioned above, there are Class Components and Functional Components. So, for each flagged component, React will call either `classComponentInstance.render()` (for class components) or `FunctionComponent()` (for function components), and save the render output.**


- Rendering can be looked at in two phases:
    - The "Render phase" contains all the work of rendering components and calculating changes
    - The "Commit phase" is the process of applying those changes to the DOM
- After React has updated the DOM in the commit phase, it then synchronously runs the `componentDidMount` and `componentDidUpdate` class lifecycle methods, and the `useLayoutEffect` hooks.
  **Let's take a look at using a component and using `componentDidMount()`

```
class App extends React.Component {
  constructor(props) {
    super(props);
    //creating state so that app can know some stuff
    this.state = {
      displayedPage : 'Projects',
      //setting backgroundImage to undefined until I fetch images
      projectPageNasaImages: new Array(3),
      homepageBackgroundUrl: ''
    }
  }
  //This method will be called after it is instantiated and will be called once
  componentDidMount() {
      //async call is here
  }
```
Well, we've just scratched the surface of component based UI in React. Let's talk about some other frameworks besides React and the difference between a **framework and a library, as these two terms get intermingled quite often:**

- Acccording to *freecodecamp.org*, both frameworks and libraries are code written by someone else that is used to help solve common problems.
- A framework inverts the control of the program. It tells the developer what they need. A library doesn’t. The programmer calls the library where and when they need it.
- The technical difference between a framework and library lies in a term called [inversion of control](https://www.tutorialsteacher.com/ioc/inversion-of-control).
- WE are in charge of the flow of the app when we use a library and choose where to call the library. With a framework, the framework is in charge of the flow. It provides some places for you to plug in code, but it calls the code you plugged in as needed.
  
**Other Frameworks besides React:**
- Angular, Ember, Backbone,Preact, Vue could be one as it blends other technologies to become a framework. Another framework is Express, it is the web application server framework for Node.js. JQuery could be called a framework and is one of the oldest ones still around.However there is some confusion still out there as to where it falls in the mix. 
  