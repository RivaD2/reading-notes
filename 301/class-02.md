# jQuery | JS Tasks Done Quickly

![Faster](https://media.giphy.com/media/7XsFGzfP6WmC4/giphy.gif)
> As a new coder, I can certainly say that there are times where I wish I could code a bit faster. jQuery serves as a way to approach JS tasks quickly and provides some consistency.
----------
## What is jQuery?
* It is a JS file that you can include in your webpages, just think of it as an extension of JS. Really it is a JavaScript library.
* Using jQuery, we can find CSS selectors and use methods on those selectors
* Once we have added the jQuery script into our page, we can use it.
* To access jQuery we start with `$()` This is a shortcut version of using `jQuery()`
* The above function allows us to find elements in the page and creates an object called jQuery which holds references to those elements.
* The jQuery object has many methods that can work with the selected elements.

## Breaking Down the format:

1. First, find elements using [CSS selectors](https://www.w3schools.com/cssref/css_selectors.asp). It looks like this:

``` 
$('ul.recipe')
// The jQuery function holds one parameter which is a CSS selector
// This selector finds all elements with the class of recipe
```
2. Use methods to do something with the selected elements:
```
$('ul.recipe').addClass('sweet');
// The first set of parenthesis holds the jQuery object
// After the member operator is the method
// Each method will then have parameter(s) which in this case is 'sweet'. These parameters tell us what is being updated and in this case we are updated the class attribute.
```
## What makes jQuery Faster?
 **Look, we can achieve our goals using pure JS, but jQuery merely simplifes our code:**
1. jQuery makes it easier to find elements especially across all major browsers.
1. jQuery uses CSS selectors which are faster at selecting elements and require less code than DOM elements.
1. CSS selectors are already used by front-end developers so there is no need to learn an entirely new language.
1. Provides easier ways to run through commonly performed tasks such as loops, handle events, handeling Ajax requests etc.
1. jQuery allows us to chain methods together so once we select some elements we can apply multiple methods at once.
1. It has cross-browser compatibility 

**What are some common jQuery Methods? Look, there are a lot to choose from. Take a look [here](https://www.tutorialsteacher.com/jquery/jquery-methods) for more information.**

## Learning more about selecting elements:
* When we select more than one element, a jQuery object is returned. This is also known as a *matched set* or a *jQuery selection*
* If a selector returns only one element, the jQuery object has a reference to one element node
* If MORE than one element is selected, the jQuery object will of course have references to each element
* Some jQuery methods **retrieve** information and others **set** information
* jQuery has a method called `.ready()`: This method checks that the page is ready for your code to work with
* The `.ready()` method is pretty cool because it can make the page appear to load faster (Read more on this method [here](https://api.jquery.com/ready/))


**Look there is a ton to read about jQuery. If you want to know more, take a page out of *Jon Duckett's JavaScript & jQuery* book. All my references come from this book.**

-----------------------------------
## PAIRED PROGRAMMING | WORKING CODE WITH DOUBLE THE POWER
![Two](https://media.giphy.com/media/QVJDkcR6wBQgG0OiLM/giphy.gif)
### Ok, seriously though, we all know that Storm and Rogue are pretty powerful on their own BUT, when they team up, I think we can agree that they are much stronger.

### What is Paired Programming and why do it at all?
* Paired programming is now common in many agile work environments (Read about [agile work environments](https://www.forbes.com/sites/larryalton/2017/10/17/why-agile-work-cultures-are-so-important-to-millennials/#14fbdd892fd2))
* What it really is, is two devs sharing a workstation to tackle a coding problem or task together
* When pair programming, there is a **DRIVER** and a **NAVIGATOR**
* The driver is the one who types, manages the code editor etc. Think of the driver as the person physically moving the mouse, the keys on the keyboard etc. 
* The navigator navigates, yes, they guide the driver using words and they think about what code comes next. They shouldn't be the ones typing the code.

**Paired programming allows us to touch on all four skills that are necessary to learning any language and these are:**
1. Reading
1. Writing
1. Speaking
1. Listening

## WHAT ARE THE BENEFITS OF PAIRED PROGRAMMING?
* **Greater efficiency:** Mistakes are caught faster and in the long run, the code that is produced is higher quality. Two minds can find solutions to problems that arise much faster than one.
* **There is more collaboration:** When working as a pair, each person relies on the other and can ask for help, not to mention that there is higher focus and distractions are less likely.
* **You learn new skills:** We should all know that everyone has different skill sets and so when we pair program, we learn from one another. There is a sharing of information and this helps us to become dynamic and ultimately knowledge is solidfied for each party. Whether one is more advanced or not doesn't matter as both parties benefit.
* **Social skills improve:** As we work with one another, we have to communicate. Our coding skills improve but so do our communication skills, our patience, and our interpersonal skills.
* **It prepares us for the job interview:** Many interviews will be in a paired programming format, as a current employee may navigate while the applicant drives. Practicing this skill early gives us a taste of what is to come.
* **It prepares us for the workplace:** Because paired programming is very common, wouldn't it kinda suck to go into a new job and have to learn this skill then? Why not master it now so we can be ready to solve those coding tasks!

**Long story short though, paired programming may take a little time to get used to but it is a necessary skill and one you'll be thankful you have,**
