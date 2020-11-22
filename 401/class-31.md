# Hooks and Browser Router

**BrowserRouter is used for doing client side routing with URL segments. Using it we can load a top level component for each route. This helps separate concerns in applications and makes the logic/data flow more clear.**
**So, Why do we not need more .html pages in a multi-page React app?**

- Because React is not designed to develop multi-page websites and if we need to create a multi-page app, we can implement multiple routes instead of multiple pages. Multiple routes are used to handle multiple views, much like html pages would.

For example, let's say we have an app and its corresponding views are described below:

```
/Homepage
/About
/Contact
```
We could do the following to set up a multi-page app:

- `npx create-react-app react-multi-page-website`
- `npm i react-router-dom`
- From there, depending on how you've set up your application, you can import them all to `App.js` and switch the routes with each corresponding path:

```
function App() {
  return (
    <div className="App">
      <Router>
        <Navigation />
        <Switch>
          <Route path="/" exact component={() => <Home />} />
          <Route path="/about" exact component={() => <About />} />
          <Route path="/contact" exact component={() => <Contact />} />
        </Switch>
```

**If we wanted a component to show up on every page, where would we put it and why?**

I would choose the following and here's why:

```
Outside the <BrowserRouter/>
Inside the <BrowserRouter />, outside a <Route />
```

- If I put it in `App.js` outside of the routing switch from BrowserRouter, it should be on every page. I would do this because in the switch statement, there is one option inside each switch. If it outside, it is not effected by the router.
- The BrowserRouter is just a wrapper that holds different routes/entire apps sometimes. So as long as a component is outside of a route, then it would still be rendered on every page.


**What does props.children contain?**
`props.children can really contain anything! *Codeburst.io* says, "My simple explanation of what `this.props.children` does is that it is used to display whatever you include between the opening and closing tags when invoking a component...

```
// Since this is a stateless function, there is no 'this' keyword so just use props.children

const Picture = (props) => {
  return (
    <div>
      <img src={props.src}/>
      {props.children}
    </div>
  )
}
```

**Whenever this component is invoked {props.children} will also be displayed and this is just a reference to what is between the opening and closing tags of the component:**

```
//App.js
render () {
  return (
    <div className='container'>
      <Picture key={picture.id} src={picture.src}>
          **//what is placed here is passed as props.children**
      </Picture>
    </div>
  )
}
```

## New Vocab to learn:

**Children / Child Components:** 
[buildwithreact.com](https://buildwithreact.com/article/component-children) explains that, "Children allow you to pass components as data to other components, just like any other prop you use."

Once again, children don't have to be components, they could be many things in React. Even if we wanted to fetch data from a server, we can do it by using a function-as-a-child pattern. After all, we can pass any JavaScript expression as children.

**Hash Routing:** 
This type of routing is considered to be server side and uses the anchor part of the URL to simulate different content. This router is mainly used for static websites with a server that only responds to requests for files that it knows about.

[stackoverflow.com](https://stackoverflow.com/questions/51974369/hashrouter-vs-browserrouter#:~:text=HashRouter%20basically%20it%20uses%20the,modified%20via%20pushState%20and%20replaceState.) says, "HashRouter uses a hash symbol in the URL, which has the effect of all subsequent URL path content being ignored in the server request."

**Link Routing:** 
Link routing utilizes the `<Link>` component. This is a wrapper around anchor tags, but has the added benefit that it automatically knows where our components are and it can adjust the style of a link to make it look active when it's the page the user is currently browsing. 

Basically this type of routing navigates different parts of an application with hyperlinks. This component is able to change the UI and update the URL.
