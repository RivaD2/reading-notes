# React Native

React Native is a framework that allows developers to build mobile applications quickly and allows for more efficient code sharing

**Before learning more about React Native, let's answer some questions related to Redux Toolkit**

1. **Compare and Contrast Redux Toolkit with Redux “Ducks”**

As you might have learned previously, Redux is a state container for JavaScript applications. The Redux Ducks pattern allows us to simply Redux's boilerplate set up. However, when we use the Redux Toolkit, we only have ONE dependency to worry about. Installing `redux-toolkit` allows us to set up a Redux app quickly and eliminates the extra steps of installing `redux thunk` and `redux-devtools-extension`. Redux Toolkit is:

1. Easier to set up (less dependencies)
2. Provides a reduction of boilerplate code (one slice vs. many files for actions and reducers)
3. Provides us with Redux Thunk and Redux DevTools built-in
4. The ability to use direct state mutation, meaning we no longer have to return `{ ...state }` with every reducer.
   
The Ducks design pattern, while providing modularity and a better way to organize actions, action types, reducers, and a structured way to add new features to our apps, it was still somewhat verbose when compared to Redux-Toolkit.

2. **What is the principle advantage of Redux Toolkit**

I would say that the principle advantage is that Redux Toolkit allows us to easily manage global state in a React application. We can access and update the state from anywhere.

**New Vocab To Review**

**Redux toolkit slices:** 
To create these, we use `createSlice()`. A slice is a function that accepts an initial state, an object full of reducer functions, and a "slice name", and then it automatically generates action creators and action types that correspond to the reducers and state.
**Namespace:**
Refers to when a variable is declared, how broadly can it be accessed...what is the space that the name is in. Is it in a function, an object, a module, is it global?