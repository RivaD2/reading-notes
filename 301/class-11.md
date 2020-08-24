# TEMPLATING WITH EJS & USING THE API
![yes](https://media.giphy.com/media/35J3oyRx7fGBEqLQQy/giphy.gif)
**Let's talk about what EJS is and how it's used to build node applications**

## What is EJS
* EJS is a simple templating language that lets you generate HTML markup with plain JavaScript.
* With EJS we are still using Javascript, it allows for a fast development time, simple syntax, quick execution and easy debugging of Javascript errors.

## How do we Install it?
1. It's easy to install EJS with NPM. Run this command:
`$ npm install ejs`
2. Pass EJS a template string and some data. Wow, now we have some HTML! Let's take a look at this example:

```
let ejs = require('ejs');
let people = ['geddy', 'neil', 'alex'];
let html = ejs.render('<%= people.join(", "); %>', {people: people});
```
3. Feed it a template file and a data file, and specify an output file.

    `ejs ./template_file.ejs -f data_file.json -o ./output.html`
4. Download a browser build from the latest release, and use it in a script tag.

```
<script src="ejs.js"></script>
<script>
  let people = ['geddy', 'neil', 'alex'];
  let html = ejs.render('<%= people.join(", "); %>', {people: people});
</script>
```

## What tags does EJS use?
* <% 'Scriptlet' tag, for control-flow, no output
* <%_ ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it
* <%= Outputs the value into the template (HTML escaped)
* <%- Outputs the unescaped value into the template
* <%# Comment tag, no execution, no output
*  <%% Outputs a literal '<%'
* %> Plain ending tag
* -%> Trim-mode ('newline slurp') tag, trims following newline
* _%> ‘Whitespace Slurping’ ending tag, removes all whitespace after it

## Using EJS with Express
1. First, install EJS:   `npm install ejs`
2. In Express v4, a very basic setup using EJS would look like the following. (This assumes a views directory containing an `index.ejs` page.

```
let express = require('express');
let app = express();

app.set('view engine', 'ejs');

app.get('/', (req, res) => {
  res.render('index', {foo: 'FOO'});
});

app.listen(4000, () => console.log('Example app listening on port 4000!'));
```
**Keep in mind that there are a number of ways to pass specific configuration values to EJS from Express**

## How does Node work with EJS?
**Let's look at the file structure. Templating would take place inside a `views` folder and these are the files needed to get started:
```
- views
----- partials
---------- footer.ejs
---------- head.ejs
---------- header.ejs
----- pages
---------- index.ejs
---------- about.ejs
- package.json
- server.js
```
**`package.json` will hold our Node application information and the dependencies we need (express and EJS). `server.js` will hold our Express server setup, configuration. We'll define our routes to our pages here.**

* Let's look at the setup in Node:
1. We would first need to go into our `package.json` and set up our project:
```
{
    "name": "node-ejs",
    "main": "server.js",
    "dependencies": {
        "ejs": "^1.0.0",
        "express": "^4.6.1"
    }
}
```
2. All that is needed is Express and EJS. Now we have to install the dependencies we just defined. Run this command:
`$ npm install`
3. Now that everything is installed, we can configure our application to use EJS and set up routes for the two pages we need. In this case, let's say we will need the index page (full width) and the about page (sidebar. We will do all of this inside our `server.js` file.

```
// server.js
// load the things we need
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page 
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page 
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');
```
4. We are ready to start our server. Run this command: `$ node server.js`

# USING THE GOOGLE BOOKS API
**What is it? The Books API is a way to search and access that content, as well as to create and view personalization around that content**

1. To acquire and use an API key, follow these steps:
* Open the Credentials page in the API Console.
* This API supports two types of credentials. Create whichever credentials are appropriate for your project:
1. **OAuth 2.0**: Whenever your application requests private user data, it must send an OAuth 2.0 token along with the request. Your application first sends a client ID and, possibly, a client secret to obtain a token. You can generate OAuth 2.0 credentials for web applications, service accounts, or installed applications.
2. **API keys**: A request that does not provide an OAuth 2.0 token must send an API key. The key identifies your project and provides API access, quota, and reports.
* The API supports several types of restrictions on API keys. If the API key that you need doesn't already exist, then create an API key in the Console by clicking Create credentials > API key. You can restrict the key before using it in production by clicking Restrict key and selecting one of the Restrictions.
* After you have an API key, your application can append the query parameter key=yourAPIKey to all request URLs.
* The API key is safe for embedding in URLs; it doesn't need any encoding.

2. Let's talk about Google Book ID's: 
**You need to specify ID fields with certain API method calls. There are three types of IDs used within Google Books:**

1. **Volume IDs** - Unique strings given to each volume that Google Books knows about. An example of a volume ID is `_LettPDhwR0C`
2. **Bookshelf IDs** - Numeric values given to a bookshelf in a user's library. Google provides some pre-defined shelves for every user with the following IDs:

- Favorites: 0
- Purchased: 1
- To Read: 2
- Reading Now: 3
- Have Read: 4
- Reviewed: 5
- Recently Viewed: 6
- My eBooks: 7

1. **User IDs** - Unique numeric values assigned to each user. These values are not necessarily the same ID value used in other Google services. Currently, the only way retrieve the user ID is to extract it from the selfLink in a Bookshelf resource retrieved with an authenticated request.

2. **ID's on Google Booksite:**
The IDs you use with the Books API are the same IDs used on the Google Books site.
* **Volume ID**:
When viewing a particular volume on the site, you can find the volume ID in the id URL parameter. Here is an example:
`https://books.google.com/ebooks?id=buc0AAAAMAAJ&dq=holmes&as_brr=4&source=webstore_bookcard`

* **Bookshelf ID**
When viewing a particular bookshelf on the site, you can find the bookshelf ID in the as_coll URL parameter. Here is an example:
`https://books.google.com/books?hl=en&as_coll=0&num=10&uid=11122233344455566778&source=gbs_slider_cls_metadata_0_mylibrary`

* **User ID**
When viewing your library on the site, you can find the user ID in the uid URL parameter. Here is an example:
`https://books.google.com/books?uid=11122233344455566778&source=gbs_lp_bookshelf_list`

## How to work with Volumes?
* Performing a search
You can perform a volumes search by sending an HTTP GET request to the following URI:

`https://www.googleapis.com/books/v1/volumes?q=search+terms`
* This request has a single required parameter:

**q** - Search for volumes that contain this text string. There are special keywords you can specify in the search terms to search in particular fields

**If you would like to learn more about EJS and how to use Google Book APIs, please click the links below. These articles were used to reference the material above:
* [Google Books APIs](https://developers.google.com/books/docs/v1/using#WorkingVolumes)
* [Templating with EJS from scotch.io](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)
* [Using EJS with Express on Github](https://github.com/mde/ejs/wiki/Using-EJS-with-Express)