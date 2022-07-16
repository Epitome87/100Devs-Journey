# Class 35 - Introduction to Node

## Agenda

- Let's Talk: #100Devs
- Learn: Callbacks
- Learn: Promises
- Learn: Async
- Learn: Node
- Homework: Simple Coin Flip

JavaScript is single-threaded, blocking, and synchronous: it can only process one operation at a time.

But if JS is synchronous, how do we do stuff like make an API request and keep scrolling or clicking?

**The environment!** Where we run JS (browser or server via Node) allows us to do async processes.
Browsers have a bunch of APIs we can use that are async and enable us to keep navigating our webpages while other operations are being processed asynchronously.

JS can do a lot of the **blocking** stuff in the browser because it is handing that stuff off to async Web APIs.

But...we are going to need to know how to handle responses coming back from those Web APIs
JS does this with callbacks, promises, and eventually async/await.

**Common Browser APIs**

- DOM (Document Object Model) API
  - "Essentially the API one uses to manipulate an HTML (or XML) document -- usually using JavaScript"

`setTimeout` and `setInterval` are not part of the JS specification.

## Callbacks

A callback is the function that has been passed as an argument to another function.

Callbacks are not really "a thing" in JS, just a convention.

Callback fires when **async task** or another function is done.

Callbacks can lead to _callback hell_ -- ugly deeply-nested code. This eventually lead to a more readable way to handle async code...

## Promise

Pretty much everything Web APIs respond with now is a Promise!

A promise is an object that represents the eventual completion or failure of an async operation and its value.
An object that MAY have a value in the future.

A promise can have three possible states:

- pending: Initial state, neither fulfilled nor rejected.
- fulfilled: The operation was completed successfully
- rejected: The operation failed.

```js
const promise = new Promise((resolve, reject) => {
  const error = false;
  if (!error) {
    resolve('Promise has been fulfilled');
  } else {
    reject('Error: Operation has failed');
  }
});

console.log(promise);
promise.then((data) => console.log(data)).catch((err) => console.log(err));
```

When a promise _resolves_ and is _fulfilled_, the `then` method gets fired.
When a promise is _rejected_ with an error, the `catch` method gets fired.

`.then()`: A promise object method that runs after the promise _resolves_
`.then(value)`: Whatever value the promise object has gets passed as an argument
`.catch()`: A promise object method that runs after the promise is rejected

## Async / Await

A way to handle async responses.
Syntactical sugar for Promises, making async code easier to write and to read.
They're technically Promises under the hood.

Await _waits_ for for an async process to complete inside an async function.

```js
async function getPaid() {
  const houseOneWait = await houseOne();
  const houseTwoWait = await houseTwo();
  const houseThreeWait = await houseThree();
}
```

However, we need to use try-catch blocks to handle any errors, much like the catch method did with pure Promises.

## Backend

Does JS have access to the DOM natively built in? Nope!
JS needed Web APIs to handle async and a bunch of stuff in the browser.

What do servers need?

- Well, they _serve_ up files, so we have to be able to manipulate files, and hear / send requests via the internet.
- Disk Access (HDD/SDD) & Network Access (internet, request / responses)

What if there was a hosting environment that allowed JS to have disk and network access? That's where **Node.js** comes in!

Node.js is a JS runtime built on Chrome's V8 JavaScript engine.
The same stuff that lets you run JS in the browser can now be used to run JS on Servers, Desktops, and elsewhere.

**Built In Modules**

Node.js comes with many built-in modules.

**Modules** are libraries or collections of functions

HTTP (network access)
FS (file system access)

**Access to millions of packages via NPM**!

Node.js is written in C/C++, so it's super fast!

## Homework

Do: Start prepping the bank
Do: Complete your professional links
Do: Make node-backend-simple-json more readable
Do: Make a coin-flip game where the randomization happens server-side
