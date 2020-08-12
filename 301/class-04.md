# RESPONSIVE WEB DESIGN WITH CSS GRID | REGEX TUTORIAL AND CHEAT SHEET
#### We moved away from float-based layouts, using Flexbox to tackle some of our most challenging layout tasks. Now I want to introduce Grid, which is one of the most powerful systems in CSS.
----------
## Combining Flexbox and Grid provides us with the power to execute our layouts just as planned.

![power](https://media.giphy.com/media/B6Jr28VwfxUFa/giphy.gif)

## WHAT IS GRID?

* It is a two-dimensional system, handling columns and rows (unlike Flexbox which is primarily one-dimensional)
* Grid layouts work by applying CSS rules to both the parent and child elements
* Grid allows us to tackle most tasks involving layout and allows us to move away from tables and floats to position elements

## GRID TERMINOLOGY

1. We have a **grid-container**: The element on which `display: grid` is applied. It is the parent of ALL the grid items
2. Next, we have the **grid-item**: These are the children of the grid container
3. There is a **grid-line**: These are the dividing lines that make up the structure of the grid. They are vertical (“column grid lines”) or horizontal (“row grid lines”).
4. There is a **grid-cell**: The space between two adjacent row and two adjacent column grid lines. It’s a single “unit” of the grid.
5.  There is a **grid-track**:The space between two adjacent grid lines. They are like the columns or rows of the grid. 
6. There is a **grid-area**: The total space surrounded by four grid lines. A grid area is made up of any number of grid cells. 
7. Grid gives us control over how wide or narrow each of the ‘grid cells’ get. 

## GRID PROPERTIES

![Many](https://media.giphy.com/media/U2MJe73aFlhMElLNnn/giphy.gif)
### There are so MANY properties for the both the parent grid containers and the children grid items and it's a little much to cover here. So I'll go over some of the basics:

**Properties of the parent elements (the grid container)**:
* display
* grid-template-columns
* grid-template-rows
* grid-template-areas
* grid-template
* column-gap
* row-gap
* grid-column-gap
* grid-row-gap
* gap
* grid-gap
* justify-items
* align-items

**Properties for the children (the grid items inside the container)**:
* grid-column-start
* grid-column-end
* grid-row-start
* grid-row-end
* grid-column
* grid-row
* grid-area
* justify-self
* align-self
* place-self

**To see in more detail how each one of the above properties works, go to [css-tricks.com](https://css-tricks.com/snippets/css/complete-guide-grid/)**
**Also check out my other page that covers basic properties of [Flexbox](https://rivad2.github.io/reading-notes/301/class-03.html)**

# REGEX (REGULAR EXPRESSIONS)
## WHAT ARE REGULAR EXPRESSIONS?

* A regex is a string of text that allows us to create patterns that help match, locate, and manage text. 
* Regular expressions can be used from the command line and in text editors to find text within a file.
* Regular expressions can save us many hours if we are working with text or need to parse large amounts of data.

### BASIC SYNTAX

```
Anchors — ^ and $
^The        matches any string that starts with The -> Try it!
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it
```

```
Quantifiers — * + ? and {}
abc*        matches a string that has ab followed by zero or more c -> Try it!
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc
```

```
OR operator — | or []
a(b|c)     matches a string that has a followed by b or c (and captures b or c) -> Try it!
a[bc]      same as previous, but without capturing b or c
```
```
Character classes — \d \w \s and .
\d         matches a single character that is a digit -> Try it!
\w         matches a word character (alphanumeric character plus underscore) -> Try it!
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character -> Try it!
Use the . operator carefully since often class or negated character class (which we’ll cover next) are faster and more precise.
```

**References are credited to [Medium.com](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)**

**There is so much more to learn regarding REGEX. I suggest you read more on flags [here](https://www.codeguage.com/courses/regexp/flags)**