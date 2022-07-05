# Anki

Here I will write out questions after each lecture or study assignment, as a way to actively recall what I just learned. Some of these will also be added to my Anki collection!

## Week 01

### Class 01

**Assignment #01**: Watch video on Active Recall `https://www.youtube.com/watch?v=ukLnPbIffxE`

Q1. What are some common revision techniques student use and think are effective, but are actually not?

- Re-reading
- Highlighting
- Summarizing / Note-making

Q2. What are two names for the most effective revision technique?

- Active Recall
- Active Retrieval

Q3. What does Active Recall involve?

- As the name suggest, simply recalling the study material shortly after it was introduced. The more effort something requires to retrieve it, and the more often, the stronger the neural connections will be.

Q4. Research has shown which to be more effective -- active recalling once, or re-reading material four times?

- Active recalling just a single time was shown to be more effective than re-reading four times!

Q5. What are some things or tools you could use to promote active recall?

- Flash cards (with an app such as Anki)
- Writing down as much as you remember after a study session
- A practice test right after learning new material
- Writing notes in the form of questions

**Assignment #02**: Watch video on Active Recall `https://www.youtube.com/watch?v=Z-zNHHpXoMM`

Q1. After Active Recall, what is the second important technique proven to help with studying? (The opposite of cramming)

- Spaced repetition

Q2. In general, what does spaced repetition involve?

- Spacing when you _actively recalling_ information. Spacing actions such as re-reading does not count!

Q3. Is spaced repetition useful only after completing a study session for the day?

- No; spaced repetition also has tremendous value when used _within_ a single study session.

Q4. What is the name of the curve that determines how we retain information over time?

- Forgetful Curve

Q5. What is the growth of the Forgetful Curve?

- It is an exponential decline over time

Q6. How can we "flatten" the Forgetful Curve?

- By actively recalling information in spaced repetitions. Each time we actively recall information, we improve the amount of information we will remember and how long it will take to forget. Eventually the curve is flat; the information is part of our long-term memory.

Q7. What is "The Magical Spreadsheet"?

- It is Ali's personal technique for implementing spaced repetition. It involves using a spreadsheet and writing the name of broad subjects as different sheets, and in those sheets writing down a comprehensive list of topics (scoped appropriately). Every time you actively recall information from that topic, put the current date in a column beside it. Color code each cell to represent how well / easily you actively recalled. Focus on new information first, and information you perform poorly on. Take a quantity over quality approach -- attempting to visit many topics on a general level rather than the fine details of a single topic.

Q8. What is "Interleaving Practice"?

- It is the concept of working on something and _just_ before mastery, moving onto a new concept.

**Assignment #03**: Do full Coursera course of "Learning how to Learn".

### Class 02 - Become a Software Engineer

**Assignment - Read Shay Howe article**

Q. Can inline elements wrap block level elements? Can block level wrap inline level? What are the exceptions?

A. No, inline elements cannot wrap block-level elements, although HTML was updated to allow anchor tags to do so. Block-level elements can wrap inline elements, as well as other block-level.

Q. What are the two most common types of links? What types of paths do each have?

- Links to _other pages_ of the same website and links to _other websites_
- Links to other pages of the same websites use relative links (no need to include domain), while links to other websites use absolute paths (include the full domain).

Q. How do we link to a part of the same page?

```html
<body id="top">
  <a href="#elementID">Go to Top</a>
</body>
```

Q. What is the syntax to link to an email address, when using an anchor tag? What about when including a subject and body?

```html
<a href="mailto:matthew@gmail.com">Email Me</a>
```

With subject and body:

```html
<a href="mailto:matthew@gmail.com?subject=Hello&body=How%20are%20you">Email Me</a>
```

Q. What is the syntax for opening a link in a new window?

- `<a href="https://somesite.com" target="_blank">Go Here</a>`
- To trigger the action of opening a link in a new window, use the target attribute with a value of \_blank. The target attribute determines exactly where the link will be displayed, and the \_blank value specifies a new window.

Q: When selectors are combined, what direction should they be read in? And what is the farthest right selector called?

- They should be read from right-to-left. The farthest right selector is known as the _key selector_ -- it identifies exactly which element the styles will be applied to. Any selector to the left of this serves as a prequalifier.

Q. In CSS, what are the two forms length values can come in? Can you give examples of each?

- Relative lengths, and Absolute lengths.
- Some examples of absolute lengths include px, in (inch), mm (millimeters)
- Some examples of relative lengths include: % (percentage), em, rem, ch, vh, vw

Q. When specifying an absolute length of pixels in CSS, how many inches is a pixel equal to?

- A px is 1/96th of an inch. So 96 pixels can fit into an inch.
- The exact measurement of a pixel, however, may vary slightly between high-density and low-density devices.

Q. What will the width and height properties on an inline element do?

A. Nothing; inline elements do not accept width and height properties or any values tied to them. Block and inline-block elements will, however.

Q. Explain how margins and paddings work different on inline elements.

A. Inline-level elements are affected a bit differently than block and inline-block elements when it comes to margins and padding. Margins only work horizontally—left and right—on inline-level elements. Padding works on all four sides of inline-level elements; however, the vertical padding—the top and bottom—may bleed into the lines above and below an element.

Q. Before CSS Grid and Flexbox, what were two common ways to do side-by-side layouts?

A. Using floats or inline-block elements.

Q. What are two ways to handling the odd rendering behavior brought on by floats?

A. You could "clear" a float use a simple `clear: both` and hope it's enough for your situation. You could handle the odd behaviors a little more thoroughly by "containing" it using a **clearfix**. To contain floats, the floated elements must reside within a parent element. The parent element will act as a container, leaving the flow of the document completely normal outside of it:

```css
.group::before,
.group::after {
  content: '';
  display: table;
}
.group::after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
```

Q. Sometimes when working with inline-block elements, we may find ourselves running out of room to place them all side by side, yet we're setting their widths to an amount that equals 100%. What's the issue? What are two ways to fix it?

A. We aren't accounting for the single space character between them. To fix it, we can either make sure one inline-block element's opening tag is on the same line as the previous one's closing tag. We can also open an HTML comment directly after an inline-block element's closing tag, and close the HTML comment immediately before the next inline-block element's opening tag.

Q. What are the "box offset" properties? In conjunction with which property-value pairs would you typically need to use these?

A. The box offset properties are left, right, top, bottom. Typically used when working with a position: relative, position: absolute.

### Class 03 - Review / Hands on Keyboard

### Class 04 - Style With CSS

### Class 05 - CSS Layout

## Class 06 - Relationship, Specificity, Box Model, Responsiveness

## Class 07 - Responsive CSS

## Class 08 - Layouts & Unleash Your Inner Baddie

## Class 09 - Live Networking

## Class 10 - Trough of Sorrow

## Class 16

### Homework: The JS Way

Q. A \_\_ is a piece of information used in a computer program.

A. Value.

**Variables**

Q. \_\_ a variable means the computer reserves memory in which to store the variable.

A. Declaring.

Q. What is the value of a variable that has been declared but not assigned a value?

A. undefined.

Q. \_\_ a variable means giving it a value.

A. Assigning.

Q. Values exist in different forms, called **\_. What do ** determine?

A. Type. A value's type determines its role and actions available to the variable.

Q. Each instruction inside a program is called a **. They usually end in a **.

A. Statement, semi-colon.

Q. A ** is an information storage area. Every ** has a **, a **, and a \_\_.

A. Variable. Variable, name, type, value.

Q. In JavaScript, how is the type of a variable deduced? What is the term for this type of language?

A. The type of a variable is deduced from the value stored in it. This type of language is a **dynamically typed** language.

Q. The ** of a variable is the part of the program where the variable is visible and usable. What is the ** for let and cost?

A. Scope. The scope for let and const is **block-level**, or **block-scoped**.

Q. A(n) ** is a piece of code that produces a value. It combines variables, values, and operators. Evaluating a(n) ** produces a value, which has a type.

A. Expression.

Q. Calculating an expression's value is called \_\_. During this, variables are replaced by their values.

A. Evaluating.

Q. Expressions may be included in strings delimited by a pair of backticks. Such a string is called a \_\_.

A. Template literal.

Q. \_\_ may happen **implicitly** during the evaluation of an expression, or **explicitly** when using the Number() and String() commands, to obtain respectively a number or a string.

A. Type conversion (or type coercion).

Q. If a value fails to convert into a number, what will the result be?

A. NaN (not a number)

Q. Regardless of the data entered, what value type does the `prompt()` command always return?

A. String.

Q. How can you convert a string into a number? And a number into a string?

A. Convert a string into a number with Number(str). Convert a number into a string with String(num).

**Conditions**

Q. The _ keyword defines a _, also called a \_. The associated code block is only run if the \** is *satisfied\* (its value is true).

A. `if`, conditional statement, test. Condition.

Q. A \_\_ is an expression whose evaluation always produces a boolean result (true or false).

A. Condition.

Q. What are the comparison operators? What do they return?

A. They return a boolean result.

```js
Operator	Meaning
===	Equal
!==	Not equal to
<	Less than
<=	Less than or equal to
>	Greater than
>=	Greater than or equal to
```

Q. An ** statement can be associated to an `if` to express an **.

A. `else`, alternative.

Q. What are the logical operators? What are they called and what is their syntax?

A. `||`, `&&`, and `!`. They are called **logical or**, **logical and**, and **logical not**.

Q. The \_\_ statement is used to kick off the execution of one code block among many, depending on the value of an expression. What is its syntax?

A. Switch.

```js
switch (expression) {
  case value1:
    // Code to run when the expression matches value1
    break;
  case value2:
    // Code to run when the expression matches value2
    break;
  // ...
  default:
  // Code to run when neither case matches
}
```

Q. As logical expressions are evaluated from left to right, they are tested for possible \_\_ evaluation. What are the rules that determine this evaluation?

A. Short-circuit.

```js
false && expr returns false.
true || expr returns true.
```

Q. A Value or expression that can be converted to false is said to be _. A value that can be converted to true is said to be _.

A. Falsy. Truthy.

Q. All values are considered _truthy_ except for which _falsy_ ones?

A.

```js
String: "", '' (empty string)
Number: 0
Boolean: false
undefined
null
NaN
```

```js
console.log(true && 'Hello'); // "Hello"
console.log(false && 'Hello'); // false
console.log(undefined && 'Hello'); // undefined
console.log('' && 'Hello'); // ""
console.log('Hello' && 'Goodbye'); // "Goodbye"

console.log(true || 'Hello'); // true
console.log(false || 'Hello'); // "Hello"
console.log(undefined || 'Hello'); // "Hello"
console.log('' || 'Hello'); // "Hello"
console.log('Hello' || 'Goodbye'); // "Hello"
```

**Repeat Statements**

Q. What is the JavaScript construct that allows you to repeat a series of statements?

A. A loop.

Q. What is each pass through a loop called?

A. Iteration.

Q. What is the code block associated with a loop called?

A. The body of the loop.

Q. What are three common loop types in JavaScript?

A. for, while, do-while.

Q. In a for loop, what is the variable used during initialization, condition, and the final expression called? What is it often named?

A. The **counter** variable. It is often named **i**.

Q. When might a while loop be better than a for loop?

A. A **while** loop may be better than a **for** loop when we **don't know the number of iterations**.

Q. What is the term for when we are checking if a given number is even or odd?

A. **Parity**.

**Functions**

Q. What is a group of statements that performs a particular task called?

A. A **function**.

Q. What is the syntax used when writing a function? What are the different grammar associated with it?

A. Function declaration. Function name. Parameters. Function body. Return value.

```js
function doCoolStuff(param1, param2) {
  // Body
  return 'Cool!';
}
```

Q. What is the syntax used when calling a function? What are the different grammar associated with it?

A. Calling a function. Passing arguments.

```js
doCoolStuff(arg1, arg2);
```

Q. If you try to retrieve the return value of a function that does not actually have one, what value does JavaScript return to us?

A. **undefined**.

Q. What are variables declared in the body of a function called? Where can they be accessed?

A. **Local variables**. They are scoped to the function body.

Q. When calling a function, the values we pass to it are called what? And what are these values called when we we are declaring the function?

A. When calling a function, we call the values passed into it **arguments**. When declaring a function, we call them **parameters**.

Q. What is a **function expression**?

A. Defines a function as part of a larger expression, typically a variable assignment. They are often used to create anonymous functions.

Q. What is an anonymous function? What is the older way to create one, and what is the more modern way?

A. A function without a name. Typically created via a function expression or by creating a fat arrow function. Typically used in places where we won't need to call it again (as a callback) or when we are assigning a variable to store the function.

Q. When creating an arrow function, what is the commonly-adapted name given to the `=>` syntax?

A. **Fat arrow** syntax.

**Objects**

Q. What is an object in JavaScript?
