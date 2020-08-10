# FLEXBOX AND TEMPLATING FOR FLUID LAYOUTS
### You've built your website but your finding that it looks a little flat and it really isn't responsive...kinda like Grampa Simpson's website below.
![website](https://media.giphy.com/media/l2JdTkHW1KZPdvdS0/giphy.gif)
### Flexbox and Grid provide us with a way to create dynamic layouts and align content within containers effortlessly. Let's dive in deeper!
----------------
### What is Flexbox and what exactly does it really do?
* CSS Flexible Box Layout (Flexbox) allows us to position responsive elements appropriately for screens of different sizes
* Items are held in a **container** and the container has the ability to change the items' height, width, and order
* Think about different screen sizes, each screen will require that items be in different orders or maybe even require wrapping of some kind. Flexbox really helps us achieve a fluid layout.
* Flex containers can flex (hence the name Flexbox), expanding or shrinking, or preventing overflow
* For larger applications, changing the orientation of items, or the size for instance is made easier using Flexbox


### FLEXBOX PROPERTIES YOU SHOULD KNOW:
1. `Display:flex;`
1. `flex-direction`
1. `flex-wrap`
1. `flex-flow`
1. `order (Keep in mind the default here is source order)`
1. `flex-grow`
1. `flex=shrink`
1. `flex-basis`
1. `flex`
1. `align-self`
1. `align-items`
1. `align-content`

**Flexbox is one-dimensional as it processes layouts as a row or column. CSS Grid Layout gets into the 2D. I'll cover more on Grid Later. For now, check out my other page on [responsive design](https://rivad2.github.io/reading-notes/301/class-01.html).**

--------------------


## JAVASCRIPT TEMPLATING LANGUAGE AND ENGINE | MUSTACHE.js WITH NODE & EXPRESS
![Mustache](https://media.giphy.com/media/tlmYAgQZZkZuU/giphy.gif)

### What is JavaScript Templating and what does it do?
* JS templating basically level-up simple web apps 
* As JS use increased, client processing capability increased as well
* Templating renders [client-side view templates](https://www.smashingmagazine.com/2012/12/client-side-templating/)
* Templates move the application logic from the server to the client--what does this mean? It means that code becomes resusable and is easily maintained
* Templating involves template engines and that is where **Mustache.js** comes into play
* The syntax of this engine looks like this `{}` (kinda like a mustache right?)
* Mustache.js is referred to as ["logic-less"](https://stackoverflow.com/questions/8906036/what-is-logic-less-template/21833090) because there are no if statements, conditionals or loops
* It is implemented by the mustache template system in JS and it is typically the base for JS templating
* Here is some more on the syntax: 
```
Mustache.render("Hello, {{name}}" , {name: "Homer" });
//This will return Hello, Homer
```
* Mustache is NOT a templating engine but it is a specification of a templating language

**You want to know more? Click [here](https://github.com/janl/mustache.js/) to read more about why Mustache.js is used.**

