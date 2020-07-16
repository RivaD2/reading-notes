
# FORMS & JAVASCRIPT EVENTS
#### What are they? Let's investigate!
![Ace](https://media.giphy.com/media/B7aksBgcJzFDO/giphy.gif) 

----
### I don't know about you, but my experience with most forms in the real world is not a pleasant one. In most cases, they usually mean you better be patient, take a seat, get comfy and wait for an unknown amount of time. Let's see what they mean in HTML land:

* Different HTML elements allow us to collect information from a user
* On your computer, you **CAN'T** escape forms as the most popular are search bars-- ***(Hmm...USED THE GOOGLE SEARCH BAR LATELY?)***
* Forms are all around you. They are present when registering on a website, online shopping, and if you sign up for newsletters or online subscriptions

#### [Forms](https://www.w3schools.com/html/html_forms.asp) collect information from user in several ways:

* Adding Text: These include entering a password or any kind of text
* Making Choices: These include radio buttons, checkboxes and drop-down boxes
* Submitting Forms: These types of forms allow the user to submit data (like a subscribe button), to use photos, or the very popular **the file upload form**

**SO, how does it all work? You want a technical description? Ok, ok...**

1. A user fills in a form and submits that information
2. The name of the form control and the data the user enters travels to the server, and the server then processes that information 
3. The server then sends a brand new page back over based on the data it received previously
4. Forms also live inside the `<form></form>` tags and every form tag requires an *action attribute*
5. Forms can be sent using [*get* or *post*](ref_httpmethods) methods
6. Information from a form is sent in **name/value** pairs

---------------------------------------

![Stimpy](https://media.giphy.com/media/GwRBmXyEOvFtK/giphy.gif)

### SOMETHING JUST HAPPENED! JAVASCRIPT EVENTS

#### What is an event? What causes one? And how do events link into our code?
* Events happen for all sorts of reasons (when a user clicks on a link, overs over elements on the page or even types on their keyboard)
* An event is the browsers way of letting us know that an interaction of some kind just happened
* Scripts respond to events and events trigger code
* As users interact with a page, and events fired, different functions in code can be triggered 
* Events impact the DOM by triggering it to update pages 
* There are so many different types of [events](https://www.w3schools.com/jsref/dom_obj_event.asp)

### Long story short, there's a lot to know about JS events. Just think of all the possible events that are being fired in every browser window out there! The clicks of buttons and links, typing, opening windows, submitting forms...
Everything we do on the internet is tied to code and certain code will trigger once we start interacting with any page or window. If you want to learn more about JavaScript events (and I know you do) click [here](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events).

