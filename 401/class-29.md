# React Routing

![going deeper](https://media.giphy.com/media/iFxXouCf76ZencqIRP/giphy.gif)

**Questions that need answering**

1. **Do child components have direct access to props/state from the parent?** 
Passing props is how parents and children can communicate typically so I would say no. If two components that don't have a child parent relationship, we can use  `compononentDidMount() componentWillUnMount() and setState()`. We can also expose a method on the child component for the parent to call. I can pass a child component data in my parent component as a prop to the child when I instantiate it within the parent.
1. **When a component “wraps” another component, how does the child component’s output get rendered?**
Well it seems like we are speaking about Higher Order Components here. According to [CSS tricks](https://css-tricks.com/what-are-higher-order-components-in-react/), "The components that receive state from the higher-order component will function as presentational components. State gets passed to them and they conditionally render UI based on it. They do not bother with the management of state."

**With the sample code below...**

```
<Main>
<Content />
</Main>
```

1. **Can a component, such as `<Content />`, which is a child, also be used as a standalone component elsewhere in the application?**
For this question I could go two ways. There are standalone web components and we can also break components down into smaller components. It also seems like props and composition provide all that we need when it comes to behavior so it seems as though a child component could be a standalone. 

1. **What trick can a parent use to share all props with it’s children**
We can use the spread operator, or rest operator or even destructuring to share all props!


**Vocab to remember**

- `props.children`: This is how we access all of the children instances inside of a parent component. Given that `this.props.children` can contain a wide set of nodes and components, React provides a set of utilities to deal with this data structure like map() forEach() count() etc.
- `composition`: [reactjs.org](https://reactjs.org/docs/composition-vs-inheritance.html) says, "Sometimes we think about components as being “special cases” of other components. For example, we might say that a WelcomeDialog is a special case of Dialog. **In React, this is also achieved by composition, where a more “specific” component renders a more “generic” one and configures it with props**
