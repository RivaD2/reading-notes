# RESPONSIVE WEB DESIGN & SMACSS 
------------
## Look around you, today everyone is attached to their mobile devices. With this in mind, building sites that work for all users is the name of the game. 
How do we do this? Responsive Web Design is the answer.
![Cool](https://media.giphy.com/media/13Tx4yM9S5NWEw/giphy.gif) 
---------------
## What is responsive web design really? 
* Responsive web design is the practice of building a website that works on all devices and every screen size.
* It focuses on providing an intuitive experience and designs should work across various devices.
* It is closely related to *adaptive* web design, but don't get them confused as there is a difference.
* Responsive designs are continually change and have fluidity
* Currently, designs that dynamically adapt to different browsers and device viewports with changing layout and content seems to work best.

### Responsive Web Design Consists of Three Main Components:
* Fexible layouts
* Media queries
* Flexible media

#### Flexible layouts do not consist of fixed measurement units, (pixels or inches). Why? The viewport height and width change too much as we move across devices. 

#### Website layouts need to adapt to changing viewports and fixed values well, they just aren't responsive.

## TOOLS USED FOR RESPONSIVE DESIGN
* [Grids](https://uxdesign.cc/responsive-grids-and-how-to-actually-use-them-970de4c16e01)
* [Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
* While using media queries, there is a design philosophy called [Mobile First](https://www.lukew.com/presos/preso.asp?26). Using mobile first, you build mobile as a default, assuming everyone is using a mobile device. Later, you add the media queries for larger screen sizes
* [Viewport Sizes](https://www.w3schools.com/css/css_rwd_viewport.asp)
* Keep a watchful eye on input types: We can't build a website assuming everyone is using a keyboard and mouse. Scroll boards, hover states, onscreen keyboards are all factors to consider when designing a page.

---------------
## SMACSS | Adding organization to our CSS
#### If you've ever jumped into the middle of a project, you know that that long line of CSS rules applied by those before you is well, slightly overwhelming. 
![Wayne](https://media.giphy.com/media/9udHO801PzozK/giphy.gif)
#### As you stare down the long list of CSS rules that have been applied by those before you, you might feel the need to get organized. That is where SMACSS comes into play. 

## What is SMACSS?
* It is a style guide and a way to examine the design process 
* It teaches us a way to approach design using CSS in a consistent fashion
* Rather than adding all CSS rules into one stylesheet, we break our CSS style rules up into different categories
* Categorization lies at the heart of SMACSS

### There are five types of categories using SMACSS:

1. **Base:** These are defaults and include single element selectors, attribute selectors, pseudo-class selectors, child selectors or sibling selectors. 

1. **Layout:** Layouts divide the page into sections, think of navs, header and footer for example
1. **Module:**: These make up the largest category as most pages have many, many modules. Modules are the reusable bits of our design. They can include callouts, sidebar sections, and product lists.
1. **State:** These are ways to describe how our modules or layouts will look when in a particular state. Think hover, hidden, expanded, active and visited links, enabled or disabled content, buttons or inputs for example.
1. **Theme:** These are similar to state rules in that they describe how modules or layouts might look.

**Usually we mix styles across all of these categories, but no more my friends, now we have a way to keep things organized**

#### By using SMACSS we have an understanding as to which category a particular style belongs to and its role within the overall scope of the page. This can be extremely helpful when working in large projects.

#### As we design webpage after webpage, using SMACSS will hopefully provide us with a way to keep our code organized and consistent. 

## Pretty cool right? 
![Cool](https://media.giphy.com/media/rSaQxzxmPAGpW/giphy.gif)

**Learn more about SMACSS [here](http://smacss.com/book/categorizing)**