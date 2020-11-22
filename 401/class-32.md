# React Components and Hooks:

**Questions for Review:**

**What does a component’s lifecycle refer to?**

It refers to the three phases in which we can manipulate and monitor a component: Mounting, Updating, and Unmounting.

**Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect**

 Well, the `useEffect` hook by default runs on every re-render. So, a way to handle this is to have helper functions that we call within `useEffect`. In order to have access to props, state or other derived values, these helper functions are defined as inner functions within the component itself.
 
 [benmvo.com](https://www.benmvp.com/blog/helper-functions-react-useeffect-hook/) says, "..the `useCallback` hook returns a “memorized” callback. It basically returns a cached version of the function based on the value of the parameters. If the parameters stay the same, we'll get back the exact same function reference every time."

`useCallback` helps us get around the problem of the helper function being redeclared with every re-render because now we’ll get back the same function reference. It will ONLY change if and when its parameters change.

**Why are functional components preferred over class components?**
According to [medium.com](https://medium.com/wesionary-team/react-functional-components-vs-class-components-86a2d2821a22), we should use functional components over class components because:

"1.Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks
2.They has less code which makes it more readable
3.They will get easier to separate container and presentational components because you need to think more about your component’s state if you don’t have access to setState() in your component"

*Medium.com* also says,*

**If you are writing a presentational component which doesn’t have its own state or needs to access a lifecycle hook,use functional component as much as possible. For state management you can use class component.**

**What is wrong with the following code?**

```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

**What looks wrong to me is that `useEffect` will run after every render and there also seems to be some infinite loop behavior here because of that. From what I can see, it seems as though the component will reload repeatedly. It looks like closures are not handled properly here.**

**New Vocab to Learn:**

**Previously in React, to add state to a component, we had to use classes. Now, we can use hooks to get the job done and we can add state to function components using hooks**

**state hook:**

The `useState` is a Hook that lets us add React state to function components.

**effect hook:**

The Effect Hook lets us perform side effects in function components. Effect is fo side effects and some of these include:Data fetching, setting up a subscription, and manually changing the DOM in React components. The `useEffect` hook is like using `componentDidMount, componentDidUpdate, and componentWillUnmount` combined.

**reducer hook:** 

This hook allows functional components in React access to reducer functions from state management.[robinwieruch.de](robinwieruch.de/javascript-reducer) says, "In essence, a reducer is a function which takes two arguments -- the current state and an action -- and returns based on both arguments a new state."

