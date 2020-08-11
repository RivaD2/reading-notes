# RESPONSIVE WEB DESIGN WITH CSS GRID & REGULAR EXPRESSIONS
#### We moved away from float-based layouts, using Flexbox to tackle some of our most challenging layout tasks. Now I want to introduce Grid one of the most powerful systems in CSS.
----------
## Combining Flexbox and Grid provides us with the power to execute our layouts just as planned.

![power](https://media.giphy.com/media/B6Jr28VwfxUFa/giphy.gif)

## WHAT IS GRID?

* It is a two-dimensional system, handling columns and rows (unlike Flexbox which is primarily one-dimensional)
* Grid layouts work by applying CSS rules to both the parent and child elements
* Grid allows us to tackle most tasks involving layout and allows us to move away from tables and floats to position elements

## GRID TERMINOLOGY

1. We have a **grid-container**: The element on which `display: grid` is applied. 
* It is the parent of ALL the grid items
2. Next, we have the **grid-item**: These are the children of the grid container
3. There is a **grid-line**: These are the dividing lines that make up the structure of the grid. They are vertical (“column grid lines”) or horizontal (“row grid lines”).
3. There is a **grid-cell**: The space between two adjacent row and two adjacent column grid lines. It’s a single “unit” of the grid.
4.  There is a **grid-track**:The space between two adjacent grid lines. They are like the columns or rows of the grid. 
5. There is a **grid-area**: The total space surrounded by four grid lines. A grid area is made up of any number of grid cells. 

## GRID PROPERTIES

![Many](https://media.giphy.com/media/U2MJe73aFlhMElLNnn/giphy.gif)
### There are so MANY properties for the both the parent grid containers and the children grid items, it's a little much to cover here. So I'll go over some of the basics:

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

