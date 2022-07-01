# Class 14 - JavaScript Functions for Beginners

This class will mostly be the same as last class.

## Agenda

- Let's Talk: 2 Classes
- Learn: What is Programming?
- Learn: JavaScript Basics
- Review: Previous Class Work
- Learn: Pseudo Code
- Build: Temperature Converter
- Learn: Functions
- Build: Functions
- Homework: Read Please

## Functions

Functions are simple sets of _instructions_
They form the "building blocks" of a program.
They help us stay DRY! We can re-use functions to handle repeat code.
With it, we put a set of instructions in memory that we can use over and over.

```js
function name(parameters) {
  // Body
}

// Call
name(arguments);
```

Helpful way to remember parameters vs arguments: "Whenever I _call_ my mom, it's to _argue_.

Parameters are like variables that only exist inside our function.

## Potential Anki Questions

Q. Difference between count++ and ++count? What are these two operators called? What will the values be here:

```js
let count = 5;
alert(count++); // What is value here?

let otherCount = 5;
alert(++otherCount); // What is value here?
```

A. The first one increments the value _after_ that line executes. The second one increments the value _before_ the line is finished executing. The value of count in the alert will be 5. The value of otherCount in the alert will be 6. These are called the increment and pre-increment operators, respectively.

Q. Name the different vocabulary that makes up defining a function and running one.

A. Function declaration, function name, parameters, function call, function arguments

```js
// Declaration
function name(parameters) {
  // Body (logic)
}

// Call
name(arguments);
```
