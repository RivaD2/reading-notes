# Let's Focus On REST

![http](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Internet1.svg/2000px-Internet1.svg.png)

## What is REST?
**REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other.**
>REST was defined by Roy Fielding, a computer scientist. He presented the REST principles in his PhD dissertation in 2000.
>
* A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data. An API for a website is code that allows two software programs to communicate with each other.
* The whole world wide web is built on this architectural style (pretty crazy to think about right?)
* REST is resource based which means that in a RESTful API we are talking about resources like a person resource, a user resource or an address resource
* For example: In a RESTful sense, we would call a URI or resource using an HTTP verb to say which operation we want to perform
* Multiple UR's may point to the same resource
* Representation IS NOT the resource, that is a good thing to keep in mind

## What is a client and what is a resource? 
* A **client** is the person or software who uses the API.
* A **resource** can be any object the API can provide information about. In Instagram’s API, for example, a resource can be a user, a photo, a hashtag. Each resource has a unique identifier. The identifier can be a name or a number.

## What about URL's?
* URLs tell the browser that there's a concept somewhere. A browser can then go ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept.
* URL = Uniform Resource Locator
* Think of this as what tells machines where things are. Everything that machines talk about have a URL.
* When you go to a web page, the browser does an **HTTP GET** on the **URL** you type in and back comes a web page.

**Ok, so again, A RESTful web application exposes information about itself in the form of information about its resources. It also enables the client to take actions on those resources, such as create new resources (i.e. create a new user) or change existing resources (i.e. edit a post).**

## So how are API's RESTful anyway?
* In order for your APIs to be RESTful, you have to follow a set of constraints when you write them. 
* These constraints will make the API easier to use

## What the server does when you, the client, call one of its APIs depends on 2 things that you need to provide to the server:
1. An identifier for the resource you are interested in. This is the URL for the resource, also known as the **endpoint.** 

2. The operation you want the server to perform on that resource, in the form of an HTTP method, or verb. The common HTTP methods are GET, POST, PUT, and DELETE.

## Ok, so now that we know the above let's cover a bit on HTTP requests
* This part tells the browser what protocol to use 
* HTTP is able to describe the location of something anywhere in the world from anywhere in the world. **It's the foundation of the web.** You can think of it like GPS coordinates for knowledge and information.
* Let's look at some of the **HTTP methods:**
1. **GET**: This method requests a representation of the specified resource. Requests using GET should only retrieve data. A GET request retrieves data from a web server by specifying parameters in the URL portion of the request.
1. **POST**: This method is used to submit an entity to the specified resource, often causing a change in state or side effects on the server. In simple terms, post is our way to send data to the server.
1. **PUT**: This method replaces all current representations of the target resource with the request payload. In simple terms, this method is used for requesting that the server save data at a location specified by the server.
1. **DELETE**: This method deletes the specified resource. In simple terms, this method is what request that the server delete a file at a location specified by the server.

**After all is said and done, remember that we as humans speak to one anotherin a specific way. We gather information about one another and share information**

**Computers do the same thing, they share messages with one another. We use nouns, verbs, adjectives etc. to communicate. Keep in mind always that machines don't have a universal noun** :)

**If you'd like to learn more, please click on the links I used to reference the material above:
1. [Github Gist](https://gist.github.com/brookr/5977550)
1. [MDN web docs HTTP methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
1. [REST API tutorial](https://www.restapitutorial.com/lessons/whatisrest.html)
