![showoff](https://media.giphy.com/media/3oI9JxRfYNSAK1pCEM/giphy.gif)
# Let's Get Fancy | CSS3 Animations, Transforms, and Transitions 
---
## TRANSFORMS WITH CSS3

* With CSS3, we can position and change elements in a new way
* To do this, we can use the **transform* property**
* This property has two settings: 2D and 3D
* Be careful with transations as browser support isn't always the best, but...overall you should be fine as things are improving
* To use it, you'll just need the property(**transform**) and the value which specifies a type
* With 2D, transforms will work on x and y axes, or horizontal and vertical axes
* With 3D, transforms work on both axes and on a Z axis (Z being depth of course)

**Working on a 2D plane, we can transform elements in multiple ways:**

* 2D Rotate
* 2D Scale
* 2D Translate
* 2D Skew
* 2D Cube

### Tip: If you really want to show off, you can COMBINE multiple transforms!

** If you've ever taken a drawing class, you surely learned about [PERSPECTIVE](https://mymodernmet.com/perspective-drawing/). Well, working on a 3D plane, we can transform elements that have perspective and can do this in multiple ways:

* The perspective of each element can be thought off as a vanishing point and within that are the:
  * Perspective Depth Value
  * Perspective Origin
* We can transform elements on a 3D plane using much of the same as if we were working with a 2D plane: 
  * 3D Rotate
  * 3D Scale
  * 3D Translate
  * 3D Skew
-----
## LET'S DO THIS! | TRANSITIONS AND ANIMATIONS WITH CSS3
![plava](https://media.giphy.com/media/pwvrJtQkm8NgY/giphy.gif)

### Imagine this scenario: You're sitting at your computer, you click on a link to take you to a site, and boom! After you hovered over an image, movement occured. What was that? "How could this be?" you might be saying. Well, you can thank CSS3 for those lovely animations. Let's cover some more ground:

* With CSS3, you can change how an element looks and behaves whenever a change occurs (a mouse hover, a click, etc.)
* These changes occur in multiple keyframes
* For a transition to take place, an element must have a [change in state](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions) and different styles **MUST**be indentified for **EACH** state
* There are 4 transition properties:
    * transition-Property
    * transition-Duration
    * transition-Timing-Function
    * transition-Delay

**NOTE: Animations pick up where transitions left off as they assist with transitions needing multiple states**

* We must use the **@keyframes** rule to set multiple points where an element must undergo a transition
* The @keyframes rule includes the animation name, animation breakpoints and properties to be animated
* The @keyframes rule must be [VENDOR PREFIXED](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix)
* Once you have declared the @keyframes, you have to assign them to an element and to do this, you will use the **animation-name** property
* In addition to declaring the @keyframes and assigning them a name, you will also have to declate an **animation-duration** property and value
* A timing function delay can also be declared using **animation-timing-function**

**LET'S LOOK AT 8 TRANSITIONS THAT WILL KNOCK YOUR SOCKS OFF**
1. Fade in
2. Change Color
3. Grow & Shrink
4. Rotate Elements
5. Square to Circle
6. 3D Shadow
7. Swing
8. Inset Border

### Now you have a pretty basic understanding of how Transitions, Animations and Transforms in CSS3 work. There is much more to learn my friend, so check out some of the sources I used to write these notes here:

Credit goes to:
[Learn to Code Advanced, HTML & CSS| Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)
[CSS3 Transform](https://www.w3schools.com/cssref/css3_pr_transform.asp)



