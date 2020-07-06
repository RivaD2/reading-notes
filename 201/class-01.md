 ![Beginning](https://media.giphy.com/media/3P0oEX5oTmrkY/giphy.gif) Introduction to HTML & JavaScript
----------------------------

## Structure of a Page: Why it Matters
-----------
#### Think about every article, every blog, every site or book you've ever read...You probably noticed something. Yeah, you got it! There is a structure to the pages, and a noticeable hierarchy of information. Let's talk about HTML:

* HTML pages are text documents
* The structure of pages helps readers to understand information
* HTML (Hypertext Markup language) describes the structure of pages and an HTML document starts with the document declaration: ```<!DOCTYPE.html>```
*  HTML uses **Elements** to describe the structure and each element has an opening and closing tag: 

* ```<html></html>```   (Tags act like containers)
* ```<body></body>``` (Tags tell us something about the info inside of them and they come in pairs)

#### Look at each element below, and you'll start to understand how you can begin to build a page:

``` 
<!DOCTYPE.html>
<html>
    <body>
        <h1>Basic html</h1>
        <p> Why structure Matters</p>
    </body>
</html>
```

#### Opening tags carry **Attributes**--These provide additional information and consist of a **name** and a **value** 
```
<p lang="en-us"> This will be a paragraph in English</p>
```

#### The attribute in the above example is "lang" and the value is inside of the tags

* Every HTML doc carries an **ID ATTRIBUTE** which identifies each element from other elements on the page. 
* Think of ID attributes (A.K.A. GLOBAL ATTRIBUTES) AS THE SOCIAL SECURITY NUMBERS OF ELEMENTS (each one is unique and be used on any element)


## Extra Markup: The Evolution of HTML
--------
#### Like all things, HTML has evolved and there are several versions out there
* Similar to the iPhone, each new version of HTML was designed to better than the last
* Evolution of HTML into different types requires that each webpage begin with the DOCTYPE declaration (which I covered above)
* This declaration tells the browser which version is being used
* It should be mentioned that commenting out your code as you work is helpful to you but ALSO EVERYONE ELSE
#### Comments are not visible to the browser and they look like this:
```<!-- I am writing a comment -->```


## Process & Design: Where do we even start when we want to build a site?
--------
#### You start by asking yourself these questions:

* Who is the site for? (the target audience)
* Why are people visiting? (Why are they coming to *your* site?)
* What are their motivations? (What do they need to accomplish or learn?)
* What info do they need? (What info is most important?)
* How often will people visit site (Will it need to be updated frequently?)

#### Have you heard of WireFraming? It is a simple sketch of vital information that needs to be added to each page of a site. Read about them [here](https://www.figma.com/blog/how-to-wireframe/).

-----------------
## Introduction to JavaScript: Say Hello to the ABC's of Learning JS
![intro](https://media.giphy.com/media/yUTmg5PbrRLXi/giphy.gif)


### A: What is a script
1. A script is a series of instructions that a computer uses to accomplish a goal
1. Scripts are precise, step-by-step instructions and scripts run code or sections of code in response to input 
1. Set the goal for your script and break down each task into steps. This is how a computer accomplishes a task--very different than how we humans do it 

### B: How do computers fit in with the world
1. Look, a computer sees the world in terms of data-programmers then make models using data
1. In computer world, each physical thing is an **OBJECT** and each object has **PROPERTIES**
1. Each property is a name/value pair--these PAIRS tell us about the object
1. **EVENTS** - They are behavior that occurs as a result of input being received. 

### C: How do I even write a script? 
1. Writing a script requires HTML, CSS, and JavaScript working together 
1. Each language is a layer and each has it's own purpose
1. Read more about JavaScript from my other page [Scripts & JavaScript Instructions](https://rivad2.github.io/reading-notes/programmingjs.html)