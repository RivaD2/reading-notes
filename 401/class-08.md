# Express Routing & Connected API

**In the previous reading, I touched on Express, REST, SOAP and covered vocabulary related to CRUD and API's. Now it's time to talk a bit more about this thing called middleware**


### What is middleware?

- According to [freecodecamp.org](https://www.freecodecamp.org/news/what-is-middleware-with-example-use-cases/), a middleware is software that acts as the intermediary between two applications and faciliates communication and aids in data management
- Remember, middleware functions have access to the request object (req), the response object (res), and the next middleware function in the applications req/res cycle.
- They are used to modify the req/res objects for tasks like parsing request bodies, adding headers etc.
- We can create our own middleware functions or use third party middleware. There is also built in middleware that Express allows us to use.
- Middleware functions do the following:
    - Execute any code
    - Make changes to the req/res object
    - End the req/res cycle
    - Call the `next()` middleware function

**An Expres application is essentially a series of middleware function calls**

### REVIEW:


1. **Name 3 real world use cases where you’d want to change the request with custom middleware:**

Parsing the body of the request, adding headers, accumulating data

1. **True or false: The route handler is middleware?**

**TRUE** According to [masteringjs.io](https://www.google.com/search?q=is+the+route+handler+middleware%3F&oq=is+the+route+handler+middleware%3F&aqs=chrome..69i57j33.4799j0j4&sourceid=chrome&ie=UTF-8), the route handler is a middleware that never calls `next()`

1. **In what ways can a middleware function end the process and send data to the browser?**

If the current middleware does not end the request-response cycle, it must call next() to pass control to the next middleware, otherwise the request will be left hanging. Error handling is a great example of how middleware ends a process! There is also built in middleware and third party middleware, these can typically end a process and send data.

1. **At what point in the request lifecycle can you “inject” middleware?**

After we have req/res objects and the data has been used to generate and send back a meaningful response, then we can process the data using middleware.

1. **What can cause express to error with “Request headers sent twice, cannot start a second response”?**

Only one response can be sent per request, so this error happens typically when we two responses are sent.


### New Vocabulary to Learn:

- Middleware: A middleware function takes a request obj and either returns response to client or passes control to another middleware function. It acts as the middleman between software, facilitating communication.

- Request Object: According to [express.js](https://expressjs.com/th/4x/api.html#req), the `req` object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on.

- Response Object:According to [express.js](https://expressjs.com/th/4x/api.html#req), the `res` object represents the HTTP response that an Express app sends when it gets an HTTP request.

- Application Middleware: Application level middleware are bound to an instance of express, using app.use() and app.VERB(). It is when we use `app.use()` or `app.METHOD()` to bind the app instance to the application middleware.

For example:

```

// this middleware will run for every request but it doesn't serve a URL
var app = express()

app.use(function (req, res, next) {
  console.log(' Hello, I come in peace!')
  next()
})


// This handles request for the route categories
app.use('/categories', function (req, res, next) {
  console.log('This middleware handles the data route')
  next()
})

```

- Routing Middleware:

Very similar to application middleware but is handled differently. Modularity is the key here. Router level middleware work just like application level middleware except they are bound to an instance of express.Router(). Routing middleware is ideal for larger code bases when compared to routing middleware.

```
// This middleware executes for every request to the router.
var app = express()
var router = express.Router();
router.use(req, res, next) => {
  console.log('This is a Router middleware');
  next();

}

```