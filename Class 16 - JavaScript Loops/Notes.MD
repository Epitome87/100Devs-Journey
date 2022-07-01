# Class 16 - JavaScript Loops

## Agenda

- Let's Talk: Next Week
- Review: Pseudo Code
- Review: Variables
- Review: Conditionals
- Review: FUnctions
- Learn: Loops
- Homework: Work During Break

## Functions

Remember:

- Functions are simple sets of _instructions_
- Functions are _reusable_
- Functions _perform one action_ as a best practice
- Functions form the basic _building blocks_ of a program

## Loops

- **Repeat an action** some number of times
- Three main types of loops in Javascript: `for`, `while`, and `do while`
- Each type offers a different way to **determine the start and end points** of a loop.

**Loops - For**

```js
for ([initialExpression]; [conditionExpression]; [incrementExpression]) {
  // Do stuff
}
```

For example:

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

Beware of **infinite loops** -- when the condition in the for-loop is never false.

**Loops - While**

```js
let count = 0;

while (count < 5) {
  console.log(count);
  count++;
}
```

## Potential Ankis

Q. What are the three main loop types in JavaScript?

`for` loops, `while` loops, and `do-while` loops.

Q. What is the vocabulary of all the parts in a for loop?

A. We have the _initial expression_, the _condition expression_ (or just _condition_), and the _increment expression_.
We set an initial value, run the loop's logic if the condition is true, and increment at the end.
