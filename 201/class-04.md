# HTML's Two L's | Links and Layout
![Link](https://media.giphy.com/media/26BRuuMVNwGyT0KiY/giphy.gif) 
### Ok, ok, so so I'm not talking about *the* Link, but rather links in html that take us to far off distant lands (other pages) and allow us to surf our way through our own pages or the web

### Think about how you surf from site to site on the web...you use links. There are:
* links that take us from one site to the next
* links from one page to the next on the same site
* links from one part on a page to a different part of a page
* Links that open browser windows
* Heck, **here's a** [link](https://www.w3schools.com/html/html_links.asp) **about** **HOW TO LINK** in HTML
* Links are created using the ```<a>``` element and users can click on anything in between the opening and closing a tags
* The *href* attribute (as you will see in the link I provided) specifes which page will be linked

### There are 2 types of LINKS:
> **Absolute Links or URL's**: 
Every page has one and it starts with the domain name

> **Relative URL's**: 
We use these when we link to other pages within the same site and a domain name does NOT need to be specified. These are best used when linking within one site
-----------------------
### LET'S LAY IT ALL OUT! | LAYOUT IN HTML
![Layout](https://mobile.developer.com/imagesvr_ce/3977/Figure01.png)

#### Layout in HTML involves controlling where elements sit on a page and how to make a page more appealing

### Let's face it, different devices and screens (and we've got plenty of them around) impact the design process as sizes and resolution vary

**Some key takeaways:**
* Remember that each HTML element is in its own box
* Each box will be block level or inline

* Block level elements start on a new line and include the tags:

``` 
<h1> <p> <ul> <li>
```

* Inline elements flow in between the text around them and include the tags:

```
<img> <b> <i>

```

* It is common to group a number of elements inside a `<div>` element which is also a block-level element but also a **CONTAINING ELEMENT**
* Pages can be **fixed** or **liquid** 
* Fixed layouts will stay the same size width no matter the size of the browser window and liquid uses percentages to specify size so that it can change depending on the size of the screen

### Controlling the layout of a page involves controlling the position of elements. HTML has the following position schemes:

* Normal Flow
* Relative Positioning
* Absolute Positioning
* Fixed Positioning
* Floating Elements

**See this [link](https://www.w3schools.com/html/html_layout.asp) to go deeper and learn more about changing the layout of your page using HTML**

-------------------------
### GOING DEEPER INTO JAVASCRIPT | FUNCTIONS OBJECTS & METHODS
#### I know how you're feelin', going deeper into JavaScript makes you feel like this:
![Functions](https://media.giphy.com/media/RTk88bfDvFz5S/giphy.gif)
#### Fear not, let's keep movin. Let's talk  about JavaScript Functions

* Functions let us group a series of statements together to complete a task
* Functions allow us to reuse portions of code to repeat a previous task
* There are a couple of **key** parts to a function and they are as follows:

1. **Function Declaration**: You must declare the function using the *function* keyword
* You then give your function a name followed by parenthesis like so:

```
function myName
```

* The statements that perform each task sit in curly braces

2. **Calling the Function**: This is the second step, you can execute the statements in the curly braces by calling the function like so:

```
function myName() {
    document.write("Riva");
}
//This is calling the function
myName(); 
```

* Functions take **parameters** or specific pieces of information that sit inside the parenthesis. These act like variables within in the function
* Functions will also have **arguments** and these are specified values given at the time the function is called

### OBJECTS
In JS, Objects group together a set of variables and functions to create a model of something in the real world
* In objects, variables become **properties** and functions become **methods**
* Properties tell us about the object, as the name, its size, etc.
* Methods represent tasks that are associated with the object

There are 2 ways to create an Object:

* [Object Literal Notation](http://www.standardista.com/javascript/javascript-object-literals-simplified/#:~:text=The%20Object%20literal%20notation%20is,Simple%20values%20are%20properties.)- It is the easiest and most popular way to create an object
* [Constructor Notation](https://www.w3schools.com/js/js_object_constructors.asp)- This way uses the *new* keyword and teh object constructor to create an object
* The constructor notation works as a blueprint and is best used when you have **MANY** object to create

There are 2 ways to access an Object's properties:

* **Dot Notation**: You use the name of the object followed by a period (called the member operator) then the name of the property or method you want to access
* **Bracket Notation**: Using this way to access properties of an object, the object name is followed by square brackets with the property or method inside them
* You can **ADD** or **DELETE** properties as well, just like you create them, you can taketh them away

To learn more about removing objects, click [here](https://www.w3schools.com/howto/howto_js_remove_property_object.asp)