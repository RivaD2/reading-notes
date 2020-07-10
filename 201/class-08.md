
![Dwight](https://media.giphy.com/media/TpePHT1Kykld6/giphy.gif)

#### Learning some key rules on positioning elements in CSS will prevent us from improvising our way through it and will make a page much more attractive.

# CSS LAYOUT CONTINUED 
-----------
### I touched on CSS [layout](https://rivad2.github.io/reading-notes/201/class-04.html) previously and hopefully you remember that in CSS, each HTML element has its very own box. I also defined inline and block- level elements. Let's expand on this:

  1. Block-level boxes start on a new line and inline boxes flow between surrounding layers of text
  1. To control how much space each box will take up, set a width (and a height too if you're feeling frisky!)
  3. IF one block-level element sits inside another, then the outer box is called the **CONTAINING/PARENT** element
  4. Using a`<div>` to hold a bunch  of similar elements together will help keep you nice and organized---just remember in that case, the div would be a **CONTAINING** element

  ** You now know that CSS has several positioning schemes that can change the layout of the page: normal, relative, and absolute: 
  * To change positioning use the **position** property and to change float elements, use the **float** property
    * The float property is worth calling out here as it allows you to place an element left or right of the containing element. The float property has proved itself to be quite handy indeed!
  * **Normal flow** is the default way browsers read HTML elements
  ---------------------------------- 

  ### DESIGN | KNOWING YOUR SCREEN SIZES

  ![Screens](https://media.giphy.com/media/3o85xnHXDgKM21daPm/giphy.gif)

  #### We learned previously that planning the design of your page matters. Think of all the people you know...how many screens does each person use? Their phone, their watch, their computer, their tv right? KEEPING THIS MIND, let's learn about screen sizes:
  
  * No matter what size screen, your design should work across various devices
  * The size of a user's screen will greatly impact how much of the page they will actually see (think phone vs computer...)
  * Some devices have a higher resolution than others and resolution can often be changed by the user 
  * The **HIGHER** resolution, the **SMALLER** the text will appear
  * The sweet spot for page size is 960-1000px wide--due to the variety of screen sizes, this is a safe place to start

  ---------------------
 ### FIXED WIDTH LAYOUTS AND LIQUID LAYOUTS

 ![Neo](https://media.giphy.com/media/rvsIuQkF1iL3G/giphy.gif)

#### Much like our friend Neo from *The Matrix* we can fight the unpredictability of various screen sizes with fixed width and liquid layouts:

  * A fixed width layout allows the design to remain the same size as the user increases or decreases the size of their browser window
  * With this type of the layout, the designer has more control  pver the items on a page and where they sit
  * What is awesome about this layout is image sizes will stay the same and keep form with the rest of the page
  
  #### Nothing is perfect so they say, so with advantages there are always some disadvantages. Just make sure you keep resolution in mind when going this fixed width route.

  * Liquid layouts expand and contract as the user increases or decreases the size of their browser window.
  * What this means is that even if the user has a small window, the page will contract to fit it. Pretty cool huh?
  
  #### We talked about the good stuff, now let's get to the bad...If the user has a very skinny or wide window, lines of text may become too long or too short. For this layout, keep images in mind as they might overflow over text.