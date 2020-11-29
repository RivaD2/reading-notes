# More about Redux: `combineReducers()`

[read.reduxbook.com](https://read.reduxbook.com/markdown/part1/03-updating-state.html) says that the `combinedReducers` function is:
>" ... a helper included with the Redux library. It takes an object where each key is a name, each value is a reducer function, and it returns a single reducer that combines them all into a single reducer. So the resulting function takes the whole starting application state, the action to be processed, and returns the new application state. But it does this by splitting up the state object by keys and passing only that slice of the state to the individual reducers."

**Questions for Review**

1. **Why choose Redux instead of the Context API for global state?**
   
There are many reasons why Redux becomes a popular choice over Context API once an application gets large enough. Perhaps one of the main reasons is to avoid prop drilling and overall is a better choice when it comes to state management because it is built to handle high-frequency updates (Context API is built in such a way that every time the value of the context changes, the component consumer re-renders)

2. **What is the purpose of a reducer?**
   
The reducer is a function that determines changes to an application’s state. It uses the action it receives to determine the change. Its purpose is to take the previous state and an action and then execute the NEXT state. Basically it's the place where changes to state happen.

[css-tricks.com](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,so%20that%20they%20behave%20consistently.) says if we were in math class, it would look like this: `initial state + action = new state`

A real reducer function however, looks like this:

```
    const contactReducer = (state = initialState, action) => {
  // Do something
}
```

3. **What does an action contain?**

An action is an object that contains two keys and their values. The state update that happens in the reducer is always dependent on the value of `action.type`. Actions are plain JavaScript objects that have a type field. We need to think of actions as an event that describes something that happened in the app.


4. **Why do we need to copy the state in a reducer?** 

As an application grows, we can no longer track differences in objects the same way...bye bye easy loops! We also use comparison functions to check whether they have the same reference. We can do this by using `Object.assign()` and the spread operator. We need to remember that if we are updating state in Redux, we need to follow the immutability rule which says, if we change objects, we replace them.


**New Vocabulary to Learn**

- **Immutable state:** Immutable state means state that shouldn't be changed directly.
- **Time travel in Redux:** This is a utility of ReduxDevTools. Basically, this tool makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app. It is a way to debug basically.
- **Action creator:** This is a function that returns an action object.
- **Reducer:** A reducer is a function that determines changes to an application’s state. It does this by taking the current state, and the action to be processed, and returning the state as it should be, based on the action occurring. **It RETURNS A NEW STATE.**
- **Dispatch:** In Redux we can say that actions are "dispatched" and dispatch is also a method. It is a way to trigger state change.
