# The Evolution of Local Storage
##### 
![computer](https://media.giphy.com/media/l0HlNaQ6gWfllcjDO/giphy.gif)

#### Today we have many options for storing our precious data. This wasn't always the case though and the local storage game has changed...BIG-TIME. 

### You've heard of cookies right? Well, they have been a part of web applications since the beginning and they can of course store small amounts of data at a time. Sure that works ok, but there are some downsides:

* Cookies are included with every HTTP request, so they tend to slow down web applications because they transmit the same data over and over
* Because cookies are included with every HTTP request, by default they send unencrypted data over the internet (unless your entire web application is served over SSL)
* Cookies can only store about 4KB of data, which slows down web applications and isn't super helpful to boot.

(If you want to know more about HTTP requests and SSL, click [here](https://www.websecurity.digicert.com/security-topics/what-is-ssl-tls-https))

### Before HTML5 there wasn't really a way to store a lot of data, much less data that is on the client and goes beyond a page refresh. 
That didn't stop people though, they found ways to hack local storage.

-----------------------------
### Local Storage Hacks
#### Ahh yes, the start of it all, in the beginning there was Microsoft Explorer. Microsoft and Gates' label of the internet as a tidal wave was groundbreaking. They changed the way storage was used and invented userData.

* userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure. 
* Adobe jumped into the game and introduced *Flash Cookies*
* Brad Neuberg then introduced *dojox.storage*
* The major player Google joined in and in 2007 they released *Gears*, an open source browser plugin aimed at providing additional capabilities in browsers
* Most likely you can remember using some of these options for storage 

#### Ok, so we had all these different companies offering solutions for storage...what's the problem? Well...

* All of these solutions were browser specific or relied on third-party plugins
* All had different interfaces and provided users with very different user experiences
* In otherwords, **NOTHING** was standardized or consistent

__________________________________
# How HTML5 Came In To Save The Day
![HTML5](https://media.giphy.com/media/YucHVxk7WYIc8/giphy.gif)

* HTML5 storage is based on key/value pairs
* Data is stored based on a named key and then it is retrieved using that same key
* The data is stored as a a [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
*  The data stored can be any type of data that is supported by JavaScript (we talked about data types: Booleans, strings, integers, floats etc.)
* Just like other JS objects, the `localStorage' object can be treated like an associative array using square brackets
* You can actually track when the storage area changes by trapping the `storage` event
* The `storage` event is fired on the `window` object whenever `setItem()`,`removeItem()`, or `clear()` is called and changes something
* The `storage` object is supported everywhere the `localStorage` object is supported
* If you exceed the 5 megabytes of storage per [origin](https://html.spec.whatwg.org/multipage/origin.html#origin-0), and exception will be thrown
* If you are storing a lot of integers or floats, this can really add up as each digit is stored as a character
* Using HTML4, we can save progress locally using the `localStorage` object

#### Long story short, we've come a long way my friends and the storage game is ever-evolving. There are even more storage options hitting the scenes such as:

* SQL & The Web SQL Database
* The Indexed Database API

Click [here](https://dev.w3.org/html5/webdatabase/) to read more The Web SQL Database 