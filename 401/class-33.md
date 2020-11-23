# Context Api and More on Hooks:

**In the previous reading I touched on hooks. I mentioned that previously in React, to add state to a component, we had to use classes. Now, we can use hooks to get the job done and we can add state to function components using hooks**

**In the previous read, I also covered what a reducer hook does. If you recall, This hook allows functional components in React access to reducer functions from state management. A reducer is a function which takes two arguments -- the current state and an action -- and returns based on both arguments a new state.**

#### Questions to be reviewed**

- **Describe use cases for useMemo() and useReducer():**
  
[medium.com](https://medium.com/@binyamin/react-hooks-usereducer-usecallback-usememo-5e5af9b0257a) says that, "useReducer is best used when you are dealing with a complex object where individual properties need to be operated on.
For example, if your app pulls in a complex data object like this, and you need to update different properties within it, you should use useReducer.

`useMemo` works like `useCallback` except that instead of memoizing a function, it memoizes a value.We can use `useMemo` when we want to save a  value to the cache, and have it NOT run again during re-renders unless the value of data is changed.

-**Why do custom hooks need the use prefix?**

*Reactjs.org* says, "When we want to share logic between two JavaScript functions, we extract it to a third function. Both components and Hooks are functions, so this works for them too! A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks."

Custom Hooks work just like regular functions. Just like we give functions proper names to tell us what they are being used for, a custom hook's name should always start with **use** so that **we can tell at a glance that the rules of Hooks apply to it.**

-**What do custom hooks usually do?**

They are used like functions and can call other hooks. They allow us to extract logic and remove duplicated logic into a separate function.

-**Using any list of custom hooks, research and name one that you think will be useful in your applications:**

I would say that below are the two hooks that will come in super handy for me first. Later hopefully I can focus on other hooks but `useState` and `useEffect` seem pretty darn important right now.

-**Describe how a hook that fetches API data might work:**

Well I would say that the `useState` and `useEffect` hook would be quite handy indeed for fetching data. If I was fetching data for the App component, this is what I would use manage the local state for the data. I am more used to using Axios to fetch data, but we could also used our recently learned fetch().

I could use the `useEffect` hook to fetch the data with axios from the API and to set the data in the local state of the component with the state hook's update function. I would prefer to resolve any promises with async/await. 

As I noted in the previous reading, to avoid infinite loop-like behavior in our `useEffect` hook, I have to remember that I ONLY WANT TO fetch data when the component mounts. 

I would need to provide an empty array as second argument to the effect hook to avoid activating it on component updates but only for the mounting of the component.

