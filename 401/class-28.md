# Component Composition

![Let's Do This](https://media.giphy.com/media/zaezT79s3Ng7C/giphy.gif)

**Let me answer some questions you may have**

1. **Can a parent component access the state of a child component?**
Indeed it can. [linguinecode.com](https://linguinecode.com/post/get-child-component-state-from-parent-component) says, "the most common method is to make a callback function that the child component will trigger and toss the state values upward". So, yes, a parent component can access the state of the child component through callback functions. Some of the ways we do this can be through **Get state value onClick event and Get state value on change event**. We can also use React hooks to accomplish this task. 

2. **What can be passed along in a prop variable?**
Props are received in the function signature as arguments in a functional stateless component. According to [medium.com](https://medium.com/@cristi.nord/props-and-how-to-pass-props-to-components-in-react-part-1-b4c257381654#:~:text=The%20term%20%E2%80%9Crender%20prop%E2%80%9D%20refers,implementing%20its%20own%20render%20logic.), "props enable you to pass variables from one to another component down the component tree. But props can be anything from integers over objects to arrays. Even React components..." There are also inline props in which we can pass other data structures.

1. **How can a child component “know” the state of another component?**
Through props. If another component has state, that state needs to be passed through props. The parent component has to do its job of passing data to the child via props and the child has to do its work by using `this.props`. The child can then use those props, for example a function, by calling the function, passing the parent a value that it is supposed to react to.



**New Vocabulary to Learn:**

- **Component props:** Props are used to pass information to components. Props make it possible to share the same data across the components and props data can come in different forms: numbers, strings, arrays, functions, objects, etc. AND we can pass props to any component
- **component state:** The state object is where we can store property values that belong to a component. When the state object changes, the component re-renders.
- **application state:** To make our UI interactive, we trigger changes to the underlying data model by using state.The State of a component is an object that holds some information that may change over the lifetime of the component(unlike props which are immutable, therefore are unable to change after they have been set)
