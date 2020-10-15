# Advanced Mongo/Mongoose | CRUD

![fun](https://media.giphy.com/media/8PE8pJnBRKG1OCRUDi/giphy.gif)

**Answers to questions related to CRUD and data modeling:**

1. Why would a developer choose to make data models?

Data modeling shows the connection between a real problem and what the computer cares about/what it needs to solve that problem. I think about it this way, a tech savvy person can't speak the same way to a person who isn't so tech savvy. They have to break their terminology apart and standardize it. Data Models do the same thing as they organize data and help communicate to business people the requirements for computer system.

2. What purpose do CRUD operations serve?

When  building APIs, we want our models to provide four basic types of functionality: Create, Read, Update and Delete. In a REST environment, CRUD often corresponds to the HTTP methods POST, GET, PUT, and DELETE, respectively. These are the fundamental elements of a persistent storage system. The CRUD paradigm helps developers construct full, usable models.

3. What kind of database is Postgres? What kind of database is MongoDB?

The main difference between these two is that SQL databases, also called Relational Databases (RDBMS), have relational structure and NoSQL doesn’t use relations. PostgreSQL is also an open-source, relational database management system and MongoDB is a general purpose, document-based, distributed database. It is another example of a NoSQL database.

4. What is Mongoose and why do we need it?

Mongoose is a Node.js based Object Data Modeling (ODM) library for MongoDB. Mongoose allows developers to enforce a specific schema at the application layer. In addition to enforcing a schema, Mongoose also offers a variety of hooks, model validation, and other features aimed at making it easier to work with MongoDB. In simple terms, using Mongoose/MongoDB allows us to not have to stick to a rigid data model. Read more [here](https://developer.mongodb.com/article/mongoose-versus-nodejs-driver)

___________________________

TIME TO LEARN NEW VOCABULARLY!

- database:

A database is an organized collection of data stored and accessed on a computer.

- data model:

A data model organizes data elements and standardizes how the data elements relate to one another. As data represents real world things, the data model represents reality.

- CRUD: Four types of functionality needed when building APIs. The models that are created must be able to Create, Read, Update, and Delete resources. In order for a model to be complete, these four operations must exist.

- schema: A schema is just a blueprint how the database is constructed and shows the outline of a model.

- sanitize: According to [medium.com](https://medium.com/@abderrahman.hamila/what-sanitize-mean-and-why-sanitize-in-code-data-5c68c9f76164), in real world sanitize is to “clean” anything from “bad things”. In computer sciences it means the same thing. Mostly for security purposes, we protect the system from malicious data by removing any illegal character.

- Structured Query Language (SQL):

It is a standard Database language which is used to create, maintain and retrieve the relational database. FOr example in SQL databases, we use words like SELECT, UPDATE, and CREATE.

- Non SQL (NoSQL):
No SQl databases are not tabular and they have flexible schemas. Important to note here that in NoSQL databases relationships are NOT defined by primary and foreign keys

- MongoDB:

It is a type of NoSQL database and by MongoDB.com's definition, ..."is a cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas."

- Mongoose: Mongoose is a Node.js based Object Data Modeling (ODM) library for MongoDB

- record:
A database record is collection of fields about the same person, item, or object in a database. It is sometimes called a row.

- document:
A document database is a type of nonrelational database that is designed to store and query data as JSON-like documents. **So with MongoDB, A document in MongoDB is like a row in a relational database and a collection is like a table in a relational database**

- Object Relation Mapping (ORM): A simple definition is that ORM is the technique of accessing a relational database using an object-oriented programming language.
