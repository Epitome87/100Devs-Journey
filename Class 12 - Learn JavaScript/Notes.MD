# Class 12 - Learn JavaScript

## Agenda

- Let's Talk: Baby Learns to Walk?
- Learn: What is Programming?
- Build: Youtube Background Picker
- Learn: JavaScript Variables && Types
- Build: Not-so-great Calculator
- Learn: JavaScript Arithmetic && Conditionals
- Build: Angry Parent Simulator
- Build: Temperature Converter
- Homework: Repetition, Repetition, Repetition!

## What is Programming?

A computer will do what you tell it to do.

A **program** is a set of instructions that you write to tell a computer what to do.
**Programming** is the task of writing those instructions in a language that the computer can understand.

**JavaScript** is the language we will be using to write these instructions.

**Syntax**: "Spelling and grammar" rules of a programming language.

JavaScript syntax includes:

- Semicolon: :
- Brackets: []
- Curly Brackets: {}
- Parentheses: ()
- Quotation Marks: " "
- Arithmetic: +, -, /, \*, %
- Other Unique Characters: []{}<>,./?:;;"`\||-()\*&&%$#!+=~

The core concepts in JavaScript that must be mastered are: Variables, Conditionals, Functions, Loops

## Variables

What are variables?

**Variables**

- We can use to tell our program to remember values for us to use later on
- The entity we use to store the value is called a **variable**.

**Declaration**: let age

- Creates a named space in memory for data

**Assignment**: age = 25

- Assigns that space in memory a value (25)

Both at the same time: let age = 25

We can also **re-assign** a variable to a new value at any time.

**Variable Conventions**

**camelCase**:

```js
let numberOfApples = 9;
```

**Variables & Data Types**

What can you store in variables?

- String
- Number
- Objects
- Functions

**Strings**

- Stores text
- String is surrounded by single or double quotes
  - Either is fine, but try to be consistent!

```js
let name = "Matthew';
let lastName = 'McGrath';
let quote = "They \"purchased\" it.";
let anotherQuote = "They 'purchased' it.";
let bestQuote = `They "purchased" it.`;
```

**Numbers**

Represent numeric data. Can be an int (whole numbers) or a float (decimals).
Can also have signed (positive, negative) and unsigned numbers

Arithmetic:
+: Addition
-: Subtraction
\*: Multiplication
/: Division
%: Modulus (gives remainder)

## Conditionals

To make decisions in programming, we use **conditionals**.

Conditionals are TRUE or FALSE.

```js
if (age > 18) {
  console.log('You are an adult');
}
```

To use conditionals to make decisions, we have to be able to make comparisons. So we have to know how to compare stuff in JavaScript.

**Comparisons:: Equality**

Are two things equal?

```js
9 === 9; // true
7 === 3; // false
'Hello' === 'Hello'; // true
```

**Logical Operators**

| Operator | Description                           | Comparing | Returns |
| -------- | ------------------------------------- | --------- | ------- |
| ==       | Equal to                              | x == 8    | FALSE   |
| ===      | Exactly equal to (value and type)     | x === "3" | FALSE   |
| !=       | Is not equal                          | X != 8    | TRUE    |
| !==      | Is not equal (neither value nor type) | x !== "3" | TRUE    |
| >        | Greater than                          | x > 8     | FALSE   |
| <        | Less than                             | x < 8     | TRUE    |
| >=       | Greater than or equal to              | x >= 8    | FALSE   |
| <=       | Less than or equal to                 | x <= 8    | TRUE    |

**Conditional Syntax**

```js
if (condition is true) {
    // Do cool stuff
}
```

```js
if (condition is true) {
    // Do this cool stuff
}
else if (condition is true) {
    // Do this other cool stuff
}
else {
    // Default cool stuff
}
```

**Multiple Conditions**

```js
// All conditions have to be true
if (name === 'Bruce' && parents === 'Dead') {
  // Turn off bat signal
}

// Either condition must be true
if (day === 'Saturday' || day === 'Sunday') {
  // It's the weekend
}
```

## Homework

Read: `https://javascript.info/variables` + Tasks
Read: `https://javascript.info/function-basics` + Tasks
