# API Server | Routes and Requests



**Today I want to briefly talk about routing using Express's routing module. As a project grows, we need to add modularity(for many reasons this is important)and the routing module is the perfect tool for accomplishing this task. Click [here](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes) if you are unfamiliar with defining and using separate route modules**

**Away we go!**
![away](https://media.giphy.com/media/hMOUzHtFPtsru/giphy.gif)

### Review

1. **How does route prefixing work with an external routing module?**
With route prefixing, we replace all of our routes with a route definition (assigning our route directory to a variable). This definition essentially tells our entry point file where to look for the routes.

We create a module function inside our external routes file, add our variable that holds our definition to the exports body, and then add the routes! Take a look [here](https://dev.to/ryhenness/external-routes-with-nodejs-1ni)

1. **When routing, what’s the difference between app.get('/data/:id') and app.get('/data/:name')?**

The difference between the two are the route parameters. In this example, we are passing in and name vs the id. So the application will get us different data for each one of these routes. The "name" from the URL path will be available as `req.params.name` vs `req.params.id`.

1. **Explain how Express handles routing conflicts?**

There is an order that is maintained when routing. Each route can have one or more handler functions, which are executed when the route is matched. So if there is a conflict, then the one that matches will be executed.


1. **What are the ways that a browser can send “data” or request variables to an HTTP server**

Well, one way is through the the HTTP POST method. However, other ways such as when the user submits a form as the browser then makes a request, either GET or POST perhaps. Using cookies and AJAX calls also send data.



### New Vocab:

- **Routing**: *expressjs.com* says routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method.

- **Route Prefixing**: *dotnettutorials** explaines that this involves giving routes attributes and when using controllers, sometimes we have the same prefixes. With prefixing we can eliminates the need to repeat the common prefixes on each and every controller action method.

- **Request “Body”**:
- **Request “Query”**:
- **Request “Params”**: