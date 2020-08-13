# HEROKU & HOW TO DEPLOY A BLOG USING NODE.JS

![heroku](https://spin.atomicobject.com/wp-content/uploads/20180508091741/heroku-node-1.png)

## What is Heroku?
* Heroku is a cloud platform that lets companies build, deliver, monitor and scale apps.
* Heroku is a service that enables companies to spend their time developing and deploying apps that immediately start producing value.
* Apps come from developers using tools and languages that they prefer and so Heroku really focuses on the developer experience. Heroku supports many different languages.
* Heroku is a fully managed container-based cloud platform, that makes it easy to run apps written in a variety of programming languages

## What languages does Heroku support?

1. Node
1. Ruby
1. Java
1. PHP
1. Python
1. Go
1. Scala
1. Clojure

## What is an application?
### Many of us know what an application is, but it is important to start here before we go into how Heroku works:

> An application is a collection of source code written in one of these languages, perhaps a framework, and some dependency description that instructs a build system as to which additional dependencies are needed in order to build and run the application. 

* Dependency mechanisms vary across languages: in Ruby you use a `Gemfile`, in Python a `requirements.txt`, in Node.js a `package.json`, in Java a `pom.xml` and so on.
* One requirement is informing the platform as to which parts of your application are runnable.

* If you’re using some established framework, Heroku can figure it out. For example, in Ruby on Rails, it’s typically   rails server  , in Django it’s  python <app>/manage.py runserver   and in Node.js it’s the `main` field in `package.json`.

## Remember Git?
### As we learned previously, Git is a powerful VCS
* The Heroku platform uses Git for deploying applications (there are other ways to transport your source code to Heroku, including via an API).
* When we create an application on Heroku, it associates a new Git remote, typically named heroku, with the local Git repository for your application.
* As a result, deploying code is just the familiar git push, but to the heroku remote instead:
```
git push heroku master
```
**There is more to learn about how to Heroku works. Check out the two sites I used to reference the information above as they will provide in-depth details on Heroku:**

**[How Heroku works](https://devcenter.heroku.com/articles/how-heroku-works)**
**[Heroku.com](https://www.heroku.com/)**

-------
## Node.js For Beginners. Deploy Your Blog to Heroku
![Node and Heroku](https://www.codeproject.com/KB/Nodejs/1214008/Screenshot__37_.png)

## What is Node.js?
* Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications.
* It's written in JavaScript and can be run within the Node.js runtime on any platform.
* First things first, you have to install it,
* In simple terms, Node.js is a server!

**First 10 steps to deploy a blog:**
1. Create your js file
```
ar http = require("http");

http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000);
```
2. Confirm Node.js is properly installed and can run by typing this command in Terminal:
``` node server.js```

3. Check it in your browser
4. Let's examine the server a little more. Here is an example of how Node provides you with non-blocking and event-driven behavior:
```
$.post('/some_requested_resource', function(data) {
  console.log(data);
});
```
**BUT WHAT DOES THAT MEAN EXACTLY?**
**What it means is that the code above performs a request for some resource. The response comes back an anonymous function is called. It contains the argument `data`, which is the data received from that request. So, Node allows you to use the so-called event loop, which works faster because of non-blocking behavior. Just know that it is SUPER FAST!**

5. Make it worldwide by turning your local server into a world wide server. This is where Heroku comes into play. 
* you need to create an account on the developer's site and install Heroku. 
6. So, you have installed Heroku right? Great! Now you need to login in by running ``` heroku login```
7. Create your project directory and then create the server.js file inside of it.
8. Declare some vars:
```
var http = require("http");
var fs = require("fs");
var path = require("path");
var mime = require("mime");
```
* The first one will give you the key to Node's HTTP functionality. The second one is for possibility to interact with the file system. The third one allows you to handle file paths. The last one allows you to determine a file's MIME-type. Just remember this is not part of Node.js and you will need to create a ```package.json``` file
9. Create the package.json file and follow the formatting by filling it in with the correct info:
```
{
  "name" : "blog",
  "version" : "0.0.1",
  "description" : "My minimalistic blog",
  "dependencies" : {
    "mime" : "~1.2.7"
  }
}
```
10. Now run the NPM install with the command ```npm install```. This will create ```node_modules`` folder and place all the files inside of it. So, we resolve our dependencies and can return to our code.

**Whew! That was a lot of steps. If you want to continue on and deploy your blog, check out the site [here](https://howtonode.org/deploy-blog-to-heroku) that I used to reference the steps above.**