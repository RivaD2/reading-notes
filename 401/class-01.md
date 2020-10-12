# Today's topics: Array methods, fetching data with superagent and asynchronous JS

![begin](https://media.giphy.com/media/5zf2M4HgjjWszLd4a5/giphy.gif)

-----------------------------

### In JS, as you might know, there are mutating methods and non mutating array methods. Learn more [here](https://lorenstewart.me/2017/01/22/javascript-array-methods-mutating-vs-non-mutating/) about the differences between the two.


**Array methods can be useful for so many wonderful things, like adding or removing items, iterating over any iterable object and for transforming given arrays.**

---------------------------

**Let's look at what we can work with here. Pay special attention to map() and reduce() as these two methods are MY FAVORITE!:**


**To add/remove elements:**

- push(...items) – adds items to the end
- pop() – extracts an item from the end
- shift() – extracts an item from the beginning
- unshift(...items) – adds items to the beginning.
- splice(pos, deleteCount, ...items) – at index pos deletes - deleteCount elements and inserts items.
- slice(start, end) – creates a new array, copies elements from - index start till end (not inclusive) into it.
- concat(...items) – returns a new array: copies all members of the current one and adds items to it. If any of items is an - array, then its elements are taken.

**To search among elements:**

- indexOf/lastIndexOf(item, pos) – look for item starting from position pos, return the index or -1 if not found.
includes(value) – returns true if the array has value, otherwise false.
- find/filter(func) – filter elements through the function, return first/all values that make it return true.
- findIndex() is like find, but returns the index instead of a value.

**To iterate over elements:**

- forEach(func) – calls func for every element, does not return anything.ALWAYS REMEMBER TO RETURN :)

**To transform the array:**

- **map(func) – map() is also an iterator! It creates a new array of the same length from results of calling a func for every element. Essentially it transforms an array of one thing to an array of a different thing.**
- sort(func) – sorts the array in-place, then returns it.
- reverse() – reverses the array in-place, then returns it.
- split/join – convert a string to array and back

- **reduce/reduceRight(func, initial)
reduce() is also an iterator! It calculates a single value from an array by calling a func for each element and passing an intermediate result between the calls. The intermediate result is the accumulator and this is the value that is carried over through each iteration.**

**Additionally:**

- Array.isArray(arr) checks arr for being an array.

-------------------------

## FETCHING DATA WITH SuperAgent

**What is SuperAgent?**

- Superagent is a library that helps programmers make asynchronous HTTP requests.

**How to install it:**

- `npm install SuperAgent`

**Once it's installed, load the module in your file:**

- `const superagent = require('superagent');`

**Now let's take a look at a code snippet from [npmjs.com](https://www.npmjs.com/package/superagent#node):**

```

/*
Promise with then/catch:
- .then is a method takes a callback function and returns another Promise or the final value
- If the promise is rejected, the return value passes through any .then(s) and is picked up by the .catch


superagent.get('http://swapi.dev/api/people/')
.then((result) => console.log(result)
.catch(err => console.error('Error getting people', err);


 /*
 -Above, superagent makes an HTTP request to the server
 - This example doesn't really let the USER know that something went wrong, and that is NOT What we want. Instead, the catch should do something that tells use that something went wrong.
 - Promises are useful because they can be returned and passed around.




/*
Promise with async/await:
- Since async functions are waiting for Promises, when a promise encounters an error it throws an exception that will be catched inside a catch method on the promise.
- In async/await functions it is common to use try/catch blocks to catch such errors.
- Inside the try, we place our code that we will 'try' to run
- Inside the catch we place code to run if there are any errors
*/


(async () => {
  try {
    const res = await superagent.get(''http://swapi.dev/api/people/');
    console.log(res);
  } catch (err) {
    console.error(err);
  }

})();



```

## So, what is a Promise exactly?

- Promises work like promises in real life. There is a promise to do something, a success or failure is not certain at the time, but there is a promise that something will happen in the future.
- Once a promise has been called, it will start in pending state.
- A pending promise can either be fulfilled with a value or rejected with a reason (error). When either of these options happens, the associated handlers queued up by a promise's then method are called.
- Promises do not always resolve to success, instead, they sometimes are REJECTED with an error
- New Promises take an arg that is a function with two params
- The two params are resolve and reject
- Promises do the same thing as callbacks but are more powerful and help us to mitigate the amount of callbacks in our code
- Let's look at this example:

```
const p = new Promise((resolve, reject) => {
    setTimeout(() => {
        //callback function will be called after 2 seconds and produce value of 1
        //resolve(1); //resolved is fulfilled

        //this returns error to consumer
        reject(new Error('message'));
    }, 2000);

});
p
//call then to get the result
.then(result => console.log('result', result))
//call catch to get error
.catch(err => console.log('Error', err.message));

```

----------------------------------

## Are all callback functions considered to be Asynchronous? The answer is NO.

- Simply taking a callback doesn't make a function asynchronous. There are many examples of functions that take a function argument but are not asynchronous.
- For a function to be asynchronous it needs to perform an asynchronous operation. (For ex: `setTimeout()`)
- Callbacks are a way to tell your code that when a certain thing is done, execute another peice of code
- A callback is a function passed into another function as an argument to be executed later
- Callbacks are great for simple cases but as you have code that requires more and more callbacks, things can get out of control really fast! Then we enter...CALLBACK HELL! Callback hell is really just many nested callbacks that make our code VERY hard to read.

**References used for this page include:**
- [npmjs.com](https://www.npmjs.com/package/superagent#node) for superagent install instructions and use
- [dev.to](https://dev.to/marek/are-callbacks-always-asynchronous-bah) and [stackoverflow.com](https://stackoverflow.com/questions/19083357/are-all-javascript-callbacks-asynchronous-if-not-how-do-i-know-which-are#:~:text=Callbacks%20that%20you%20call%20yourself,calls%2C%20which%20are%20always%20synchronous.&text=js%20disk%20or%20network%20APIs,end%20up%20being%20async%20too.) for understanding more on callbacks and whether they are really ALL asynchronous
- [lorenstewart.me](https://lorenstewart.me/2017/01/22/javascript-array-methods-mutating-vs-non-mutating/) for that nice cheatsheet on array methods. I edited lines for map() and reduce()