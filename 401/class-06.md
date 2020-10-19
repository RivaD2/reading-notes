# ORM's and NoSQL Databases 

**Now that you've learned a little bit about NoSQL databases like MongoDB, let's cover a bit more on this topic**

![fun](https://media.giphy.com/media/FltCW7GUbF5iE/giphy.gif)

#### Review:

1. **Define three related pieces of data in a possible application:** In Netflix for example, there is the user, the movie, and the watchlist.
1. **Describe the constraints and rules on each piece of data and how you would relate these pieces to each other:**
    - For the user, a constraint would be the profile, and some rules that could apply would be how many profiles can they have?Only one? How many profiles can one user have? Two or more? A rule obviously could be increased costs based off each profile addition.
    -  A rule  for the watchlist would be can a user add the same movie the watchist? Can they share their watchlist with someone else? 
    - Rules for the movies themselves could be a limited number on the layers of personalization? Can the user sort movies by genre, rating, title, etc and if so, rules would apply to how these movies are displayed to user and organized.
- **What is the advantage of an ORM, like Mongoose?** One of the biggest advantages of using Mongoose is its flexiblity! Code is easier to resuse, update and maintain as we usually only make our model once. We can also extend and inherit methods from models.
- **How does the repository pattern compare with an ORM?** According to *docs.microsoft.com*, "Repositories are classes or components that encapsulate the logic required to access data sources." The Repository allows the rest of the application to ignore persistence details, then we can test an app via mocking or stubbing. Object Relational Mapping are useful as they allow us to separate concerns in our application with reusable methods for database queries. We can also easily use other SQL databases without needing to rewrite the entire code-base.
- **When making a repository/facade, what flexibility do you gain?** Flexibility comes from testing and refactoring. [Cubetech.com](https://cubettech.com/resources/blog/introduction-to-repository-design-pattern/) says that making a repository allows for:
    - "Centralization of the data access logic makes code easier to maintain
    - Business and data access logic can be tested separately
    - Reduces duplication of code
    - A lower chance for making programming errors
- **Name 3 cloud based NoSQL Databases:** MongoDB, Microsoft Azure SQL Database,Amazon Relational Database

### New Vocabulary to Learn:

1. **collections**: Collections are just a grouping of MongoDB documents
1. **Repository design pattern**: The [Repository pattern](https://deviq.com/repository-pattern/) implements separation of concerns by abstracting the data persistence logic in your applications
1. **mongoose middleware**: A middleware function takes a request obj and either returns response to client or passes control to another middleware function.
    - In express, every route handler function we have `(app.get())` is technically a middleware function
    - Middleware functions terminate the request/response cycle
    - For example, `app.use(express.json())` reads request when it is called
    - The job of this middleware function is to read request and if json obj is in body of request, it will parse the body of the req into json obj, and set request.body property
1. **Object Relation Mapping (ORM)**: Object-relational-mapping is the idea of being able to write queries using the object-oriented paradigm of your preferred programming language.
