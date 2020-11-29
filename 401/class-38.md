# Redux Continued: Asynchronous Actions

**Questions for Review**

1. **How granular should your reducers be?**
I would say pretty granular as it seems as though we should try to put as much of the logic for calculating a new state into the appropriate reducer, rather than in the code that prepares and dispatches the action (like a click handler). 
Also after reading about Redux and reducer functions, it is clear that reducer logic was made to be split and that we SHOULD have many reducer functions all handle the same action separately.Allowing many reducers to respond to actions will typically allow our app to scale better, and minimize the number of dispatches.

   
2. **Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched**
This is a Con.
   
3. **Name a strategy for preventing the above**
We should avoid **dispatching many actions in a row** to accomplish a larger conceptual "transaction". What happens when multiple reducers "fire" based off a commonly named action is multiple UI updates, making other states invalid.
Instead, we should dispatch a single "event"-type action that results in all of the appropriate state updates at once, or consider the use of action batching addons to dispatch multiple actions with only a single UI update at the end.
   
**Vocabulary Review:**

**Store:** 
  
[redux.js.org](https://redux.js.org/tutorials/fundamentals/part-4-store) says a store, "brings together the state, actions, and reducers that make up your app. The store has several responsibilities:

1. Holds the current application state inside
2. Allows access to the current state via store.getState();
3. Allows state to be updated via store.dispatch(action);
4. Registers listener callbacks via store.subscribe(listener);
5. Handles unregistering of listeners via the unsubscribe function returned by store.subscribe(listener)

**There is only a single store in a Redux application**

**Combined reducers:**
  
They are helper functions included with the Redux library. They take an object where each key is a name, each value is a reducer function, and return a single reducer that combines them all into a single reducer. They are used to spread out state.