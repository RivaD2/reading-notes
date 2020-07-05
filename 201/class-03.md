![Boxes](https://media.giphy.com/media/XeTppBMQjo9Xy/giphy.gif)
# LET'S GET ORGANIZED| HTML LISTS & CSS BOXES 
### Oh! And Let's take our JS skills further with SWITCH STATEMENTS
--------------
### We make lists in our day-to-day lives so you're familiar with how they work. There are times that we will want to organize information in an HTML file using lists

#### There are 3 different types:
1. **Ordered Lists**- each item is numbered (just like the current lists you are reading NOW), and steps are identified using numbers
```
Ordered lists start with the tag <ol> and have list items nested inside that start with a <li> tag
```
2. **Unordered Lists**- They are unordered, and do not use numbers. These begin like so, without a number but instead begin with a bullet point
```
Unordered lists start with a <ul> tag and have list items nested inside that start with a <li> tag as well
```
3. **Definition Lists**- These are made with set terms and provide definitions (Hello, read a dictionary much?)
```
These lists are started with the <dl> tag and nested inside are <dt> tags which set the term being defined, and then <dd> tags provide the definitions
```
**Lists can be nested inside one another as well, so go out there and get organized!**

------------------------------------

### CSS BOXES | BOXES INSIDE BOXES INSIDE BOXES
#### Using different style elements we can control dimensions, create borders, set margins and contain space around boxes changing padding, and hide boxes
Let's take a look:
* Box default sizes are big enough to hold content
* To change sizing of a box, we use pixes (px), percentages (%) or ems.
* To set different dimensions for boxes, we will change **height** and **width** properties

#### EVERY box has 3 available properties that when adjusted, will control it's appearance:
1. BORDER: Every box has a border 
2. MARGIN: Margins sit outside of the border and setting a width of a margin creates gaps between two boxes that sit beside one another
3. PADDING: Padding is just like it sounds, it's the space between the border and content inside it
#### There are so many ways to style borders and boxes so click [here](https://www.w3schools.com/cssref/css3_pr_box-sizing.asp) to take a deeper look!
--------------------
### YOU GOT THIS! 
![Dean](https://media.giphy.com/media/9U8vFgk0fD1OE/giphy.gif)
### LET'S SWITCH IT UP | SWITCH STATEMENTS IN JavaScript

### Earlier I touched on if else statements and how they check conditions, ya know, if "A" is true then do "B"...you remember right?

### Well, switch statements work better with fixed data values and they start with the **switch value**
* Each switch statement includes cases, each one indicating a possible value for the variable and code that should run if the variable matches that value

 Confused?

### Look, switch statements still test multiple conditions and CAN be more efficient than a bunch of if else statements. They compare a value against possible outcomes (and provide a default option if none match)
Click [here](https://javascript.info/switch) to see examples of Switch Statements

### Let's talk about Type Coercion
* JS can convert data types to complete an operation and this is called **TYPE COERCION**
* JavaScript, unlike other programming languages,can change data types for values
* Because of this, when we compare two values and check to see if they are equal (to get a Boolean result), it is better to use the strict equality operator as follows:

```
'hello' === 'hello' - will return true
'1' !== 1 - will return true

###  Checking two values this way will help us to avoid errors in our code since JS type coercion can lead to unexpected values


