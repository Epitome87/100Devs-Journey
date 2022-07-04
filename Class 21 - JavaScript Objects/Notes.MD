# Class 21 - JavaScript Objects

## Objects

What are objects?

- Objects are a **collection of variables and functions**
- Objects **represent the attributes and behavior** of something used in a program
- Object variables are called **properties** and object functions are called **methods**
- Objects store **"keyed"** collections

```js
let stopwatch = {};

stopwatch.currentTime = 12;

stopwatch.tellTime = function (time) {
  console.log(`The current time is ${time}.`);
};

stopwatch.tellTime(stopwatch.currentTime);
```

```js
stopwatch = {};

stopwatch.seconds = 20;
stopwatch.hours = 4;
stopwatch.isWorking = true;
stopwatch.start = function () {};
stopwatch.stop = function () {};
```

## Potential Ankis

Q. What is an object? Can you show two ways to create and use one?

A. Objects are a collection of variables and functions.

```js
const person = {
  name: 'Matthew',
  age: 35,
  eat: function () {
    console.log('numnum');
  },
};

const anotherPerson = {};
anotherPerson.name = 'Caitlin';
```
