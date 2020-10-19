# Let's hop on the EXPRESS train!

![train](https://media.giphy.com/media/zUTQ7vmg3boME/giphy.gif)

** What is express?**
- Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications. 

**If you're feeling rusty on terminolgy related to building ReSTFUL services, check out my other doc on [REST](https://github.com/RivaD2/reading-notes/blob/master/301/class-07.md)

1. **What’s the difference between PUT and PATCH?**: According to [rapidApi.com](https://rapidapi.com/blog/put-vs-patch/):
    - **PUT** is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PUT is similar to POST in that it can create resources, but it does so when there is a defined URI. PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn’t exist.
    - **PATCH** applies a partial update to the resource. In this case, we would only send the data that we want to update.
1. **Provide links to 3 services or tools that allow you to “mock” an API for development like json-server**: Mirage.js, Jest,Cypress
1. **Compare and contrast Swagger and APIDoc.js**: Ok, there was a lot to cover here. To get more details, visit [npmcompare.com](https://npmcompare.com/compare/apidoc,documentation,esdoc,jsdoc,swagger)
1. **Which HTTP status codes should be sent with each type of (un)successful API call?**
    - Client errors (400–499),
    - Server errors (500–599).
1. **Compare and contrast SOAP and ReST**: According to [restfulapi.net](https://restfulapi.net/soap-vs-rest-apis/), **RESTful Web services** are completely stateless. Managing the state of conversation is the complete responsibility of the client itself. The server does not help you with this. Normally, a **SOAP Web services** are stateless – but you can easily make SOAP API stateful by changing the code on the server.
     **REST** -REpresentational State Transfer – is an architectural style that makes use of existing and widely adopted technologies, specifically HTTP, and does not create any new standards.
    - Overall, **REST is simpler to develop** because it leverages the web, which is already in place, and the degree of freedom is limited (fewer choices to make, so simpler). SOAP offers several alternatives and is also slightly more difficult to develop, but offers more alternatives and areas to work.

### New Vocabulary to Learn:

- **SOAP**: Simple Object Access Protocol** defines a very strongly typed messaging framework that relies heavily on XML and schemas.
- **ReST Verbs**: GET(read), PUT(update/replace), PATCH(update/modify), DELETE
- **CRUD Verbs**: CREATE, READ, UPDATE, DELETE
- **Swagger**: [Swagger.io](https://swagger.io/docs/specification/2-0/what-is-swagger/) says that, "Swagger allows you to describe the structure of your APIs so that machines can read them."
    - By reading your API’s structure, Swagger can:
        1. Automatically build beautiful and interactive API documentation.
        2. Automatically generate client libraries for your API in many languages and explore other possibilities like automated testing.
        3. Swagger does this by asking your API to return a YAML or JSON that contains a detailed description of your entire API.