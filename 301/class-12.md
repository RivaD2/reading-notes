# Intro To EJS Partials
![EJS](https://miro.medium.com/max/3920/1*5xR5P6dzu4LpyMaR2QMphA.jpeg)

**Partials are native to EJS and we want to use them on reusuable pieces of text that stay static**

## What are Partials?
* Partials are kinda like functions, they make large websites easier to maintain because they allow us to avoid having to change a piece of text in every page it appears in. 
* When using partials, you define that reusable bundle of code in a file and include it wherever you need it.

# Perfect Candidates for Partials
* nav bars
* footers
* Anything that you would like to create a template for keep your code dry

---------

# How they work

1. Because partials are still templates, we are going to include them in the `views` folder, in their own sub-directory.
2. We create EJS template files in the partials directory and then we just add our basic HTML boilerplate into each so that we can focus on the body content in our other template files.
3. Next, we have to link our partials into the templates so we will use this formatting:
` <%- include("partials/header.ejs") %>`
4. This new command include is telling Express to pull the contents of the named template and place it in place of this command.

**Express is already looking in the views directory for our templates, so when we give the name of the template to be included we consider that to be the root directory, but we still have to tell it to look in the partials folder that we made**

5. Our template for a header would look like this.
`<% include partials/header.ejs %>`

6. In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters
7. Including a partial in EJS is quite straightforward. You use `<%- include( PARTIAL_FILE ) %>` where the partial file is relative to the template you use it in.

If you want to learn more about partials, click on some of the links below as I used them to reference the information above:

* [WalkThroughCode on Youtube | Intro to EJS-Partials-7](https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)
* [medium.com | EJS Partials](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)
* [ncoughlin.com | Express + EJS:Styles & Partials](https://ncoughlin.com/posts/express-ejs-styles-and-partials/)

