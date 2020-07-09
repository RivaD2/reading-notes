![tables](https://media.giphy.com/media/vXCnjyyQTzAFG/giphy.gif)
# LET'S HAVE SOME FUN! 
## Tables | JS Constructor Functions & DOMAIN MODELING
-------------------------

### In real life we use tables for many reasons. Well, in JavaScript they come in handy too. 
* So, WHAT is a table and WHEN is it used?
  * A table represents information in a grid and each block in the grid is called a *table cell
  * Remember Excel? (Yeah, I don't want to think about it either), but really, a table in HTML is quite similar to a spreadsheet
  * You will find that you may need to organize information that needs to be displayed in a grid (which is then made of of rows and columns)
  * Here's a very simple example of how a table is structured:

  ```
  <table> <!-- This element is used to create a table -->
    <tr> <!--The start of each row begins with this tag-->
      <td>$20.00</td> <!-- Each td represents the cell, and stands for table data -->
      <td>$15.00</td>
      <td>$10.00</td>
    </tr>
  </table>
  ```
* Now that you know the basic structure of a table and understand what a table does, you should know a couple more important things:
  * Often, the `<th></th>` element is used and it stand for table heading 
  * The purpose of the `<th>` tag improves SEO and makes it easier to change the style of a table when you use CSS
  * Using this tag also helps those who use screen readers so it is a handy tag to incorporate into your tables 

  --------------------
  ### I know you have some questions...

 ![Nathan](https://media.giphy.com/media/UvwI1X7XkbXq0/giphy.gif)

 ####  Much like our friend Captain Malcom Reynolds in *Firefly* we may not have all the answers, but we must change course. 
 ### LET'S LEARN MORE ABOUT JS CONSTRUCTOR FUNCTIONS!

 First, check out my other page on [Links and Layouts](https://rivad2.github.io/reading-notes/201/class-04.html) as it covers the very basics of JS functions and creating JS Objects. NOW my friend, continue on:

 * Using the **New** keyword first with the object constructor create a **BLANK  OBJECT**
 * After the blank object is created we can then add our properties and methods to it
 * Remember, just like with literal notation, we can access an objects properties and methods using dot notation or bracket notation
 * If there is **ONE** thing to pull from this section, it is that using the constructor notation allows us to **CREATE MANY OBJECTS**
 * Why would we want to do this? Well, sometimes we may want objects to represent similar things. 
 * Using constructor notation creates a template and then we can create *instances* of the object using the constructor function. 
 * It should be noted that using the **THIS** keyword is commonly used inside functions and Objects

 Take a look at some examples of Objects [here!](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

---------------------------------
 ### DOMAIN MODELING 

 ![wow](https://media.giphy.com/media/Wyt6sLEjKjaFjzybth/giphy.gif)

 ####  Now that you know about constructor notation, and how to create many objects, let's talk a bit more about constructor functions. I promise that by the of it you'll be quite impressed!

 Earlier I said that after we create our object, we create *instances* of the object using the constructor function. Let's see what that's all about:

 * Constructor functions allow us to define the same  properties of many objects
 * First we declare our variable and then assign it a function (most likely with parameters)
 * Since we've defined our function, next we use the **NEW** keyword I mentioned earlier to create the object
 * After those steps, we **INITIALIZE** our object(s) by calling the constructor function we defined
 * NOW, the object(s) are stored inside the variable(s) we first defined

 ### Object Oriented Programming has many benefits AND in many ways reminds me of what we learned about RECYCLING as kids:

 * It allows us to **REDUCE COMPLEXITY** as the structure is cleaner. 
 * It allows us to **REUSE** code 
 * It allows us to **RECYCLE** the functions and data within in an object (we can use these over and over again anywhere or in other programs)



 


  