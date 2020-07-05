# Let's talk more about HTML text,
## Adding style and pizazz with CSS,
### And finally, basic JavaScript Instructions
![Let's Go](https://media.giphy.com/media/h86Krb9r57FGfgRULu/giphy.gif)

---------------
### More on HTML TEXT
#### We've talked about how HTML add structure to a page and why it matters. But did you know that 
there are two types of markup within HTML? I didn't think so. Read on to find out more:

##### **Structural markup** are the elements that describe headings and paragraphs:
```
<h1> The Main Heading
<h2> The second level heading
<h3> the third level heading
<p>  The paragraph tag
<b>  This element makes text bold
```
##### Are you seeing how this works? There is more to structural markup like [whitespace](https://medium.com/@patrickbrosset/when-does-white-space-matter-in-html-b90e8a7cdd33), [horizontal rule](https://www.w3schools.com/tags/tag_hr.asp), and [line breaks](https://www.w3schools.com/tags/tag_br.asp)

##### **Semantic Markup** provides more info to the pages but they don't change influence or change the structure of the page. Let's look at some of these:
```
<strong> adds strong emphasis to words inside it
<em> This changes the meaning of a sentence and is shown in italic
<blockquote> This is used for longer quotes that take up a paragraph
```
### Let's Add Some Style: CSS
 ![CSS](https://media.giphy.com/media/13FrpeVH09Zrb2/giphy.gif)

#### CSS is fun, exciting and pretty darn cool! However, sometimes, you change one style rule only to find out that things are now a bit more complicated. Let's put on our best attire and learn about CSS:

* CSS is all about design and adding styles, colors, sizes, positions, borders and countless other style rules to our html elements
* Think about this...Boxes, boxes and you guessed it, MORE BOXES! Imagine that there is a box around each HTML element...

* CSS allows you to create rules that change the way that box appears, or is presented
* CSS associates style rules with HTML elements and contains **two** parts: 
1. A Selector: The selector indicates which element the style rule applies to
1. A Declaration: Declarations indicated how the selectors should be styled.

##### See my other page on [CSS](https://rivad2.github.io/reading-notes/structure-css.html) and check out this [link](https://www.codecademy.com/learn/learn-css) to learn more
----------------------------------

### It's time to talk JavaScript
#### Where do we start with JS? Well, we talked earlier about how computers follow precise instructions, step by step. Let's start there:
* Each individual instruction that is given is called a **statement**
* Just like in our HTML documents, we should comment on our code and in JS in looks a a bit different:
``` 
/* This is a multiline comment, where I can write more than one line of text... */
// This is a single line comment 
```
* **Variables** are how data is stored in JS, and the data is made of up of values
* You must declare the variable and assign them a value like this:
```
var today = "Sunday";
```
* Variables can hold different data types such as: numeric data types, strings (like the word Sunday), and Boolean data types

##### Click [here](https://rivad2.github.io/reading-notes/javascript.html) to learn about JavaScript Expressions and don't forget [arrays](https://javascript.info/array)
---------------

### DECISIONS AND LOOPS
![Loop](https://media.giphy.com/media/3h4EggeNZr5WUaPvtO/giphy.gif)
##### 
Sometimes, they make ya feel like you're drowning in a sea of Cheerios 

* With code, you will **analyze** values to see if they match expected results
* Using results of your evaluations, you can **decide** which way the script should go
* Often, you will want to perform the same task repeatedly, this is where **loops** come into play

### What about LOOPS and COMPARISON OPERATORS?
##### First, read my page on comparison operators and loops [here](https://rivad2.github.io/reading-notes/opsandloops.html), then read below:

### IF ELSE STATEMENTS

* If else statements are used VERY OFTEN in JS and they allow us to run one set of code if a condition is true, and if another is FALSe
* If else statements rely on conditionals, basically saying, if "A" is true, then do "B":
``` 
if (name = "Riva) {
    return "hi Riva";
} else {
    return "hello stranger!"
}
```
### HAD ENOUGH? I didn't think so.
Next I'll cover html lists, boxes, and JS Control Flow!