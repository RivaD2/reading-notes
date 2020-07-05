# HTML's Two L's | Links and Layout
![Link](https://media.giphy.com/media/26BRuuMVNwGyT0KiY/giphy.gif) 
### Ok, ok, so so I'm not talking about *that* link, but rather links in html that take us to far off distant lands (other pages) and allow us to surf our way through our own pages or the web

#### Think about how you surf from site to site on the web...you use links. There are:
* links that take us from one site to the next
* links from one page to the next on the same site
* links from one part on a page to a different part of a page
* Links that open browser windows
* Heck, **here's a** [link](https://www.w3schools.com/html/html_links.asp) **about** **HOW TO LINK** in HTML
* Links are created using the ```<a>``` element and users can click on anything in between the opening and closing a tags
* The *href* attribute (as you will see in the link I provided) specifes which page will be linked

#### There are 2 types of LINKS:
> **Absolute Links or URL's**: 
Every page has one and it starts with the domain name

> **Relative URL's**: 
We use these when we link to other pages within the same site and a domain name does NOT need to be specified. These are best used when linking within one site
-----------------------
### LET'S LAY IT ALL OUT! | LAYOUT IN HTML
![Layout](https://mobile.developer.com/imagesvr_ce/3977/Figure01.png)

#### Layout in HTML involves controlling where elements sit on a page and how to make a page more appealing

#### Let's face it, different devices and screens (and we've got plenty of them around) impact the design process as sizes and resolution vary

**Some key takeaways:**
* Remember that each HTML element is in its own box
* Each box will be block level or inline
* Block level elements start on a new line and include the tags:
``` <h1> <p> <ul> <li>```

* Inline elements flow in between the text around them and include the tags:
```<img> <b> <i>```
* It is common to group a number of elements inside a ```<div>``` element which is also a block-level element but also a **CONTAINING ELEMENT**
* Pages can be **fixed** or **liquid** 
* Fixed layouts will stay the same size width no matter the size of the browser window and liquid uses percentages to specify size so that it can change depending on the size of the screen

#### Controlling the layout of a page involves controlling the position of elements. HTML has the following position schemes:

* Normal Flow
* Relative Positioning
* Absolute Positioning
* Fixed Positioning
* Floating Elements

**See this [link](https://www.w3schools.com/html/html_layout.asp) to go deeper and learn more about changing the layout of your page using HTML**