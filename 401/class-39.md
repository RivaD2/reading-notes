# Redux - Additional Topics

**Questions for Review**

1.**What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?**

Well after learning about Thunk, and allow it allows us to perform asynchronous actions, I would say the best practice for preloading data is to fire off an asynchronous action. We could then `mapStateToProps` to simply pass it down the results to the component that renders the data.

2. **When using a thunk/async action that dispatches the actual action, which do you export from your reducer?**

From my understanding, we would still export reducers separately, and any action that is async would return a function to be exported.

**Terms for review related to Redux Thunk:**

1. **middleware:** 

Middleware allows us to use different kinds of async logic to interact with the store. We can then dispatch actions and check the store state while keeping the logic all separate from our UI logic. Just like middleware works in other applications, it allows us to have a separation of concerns.

2. **thunk:** 

Thunk is a type of Redux Middleware that allows us to have async logic interact with the store by dispatching or checking the current store state. It allows us to write functions that contain async logic directly.