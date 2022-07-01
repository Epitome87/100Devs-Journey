# Class 13 - Fun JavaScript Examples

## Agenda

- Let's Talk: Imposter Syndrome
- Learn: What is Programming?
- Learn: JavaScript Basics
- Review: Previous Class Work
- Learn: Pseudo Code
- Build: Temperature Converter
- Learn: Functions
- Build: Functions
- Homework: Read Please

## Imposter Syndrome

Feelings of doubt and inadequacy, fear of being "figured out." This is a common feeling in tech. Try to leave it at the door and approach each day with a positive outlook!

## Pseudo Code

Using plain English to write out what you hope to accomplish in code. Helpful for breaking down long, complex problems.

Pseudo code for converting Celsius to Fahrenheit:

```js
// Need the value that is in Celsius
// Convert that value from Celsius to Fahrenheit using: F = C * (9/5) + 32
// Show that converted value to the screen

const button = document.querySelector('#convertButton').addEventListener('click', convertToFahrenheit);

const convertToFahrenheit = function () {
  // Need the value that is in Celsius
  const celsius = document.querySelector('#celsiusInput').value;
  // Convert that value from Celsius to Fahrenheit using: F = C * (9/5) + 32
  const CELSIUS_TO_FAHRENHEIT = 9 / 5 + 32;
  const fahrenheit = celsius * CELSIUS_TO_FAHRENHEIT;

  // Show that converted value to the screen
  document.querySelector('#fahrenheitDisplay').innerText = fahrenheit;
};
```

## Potential Ankis

Q. Since document.querySelectorAll returns a NodeList, which is _like_ an Array but _not_ an Array, how can we iterate through it in a way that ensures maximum browser support?

A. One way is to convert it to an Array, using:

```js
Array.from(document.querySelectorAll('#targetID')).forEach((element) => element.addEventListener('click', func));
```

Another is to use a simple for-loop. We can also use the spread operator, although this may not be supported either:

```js
[...nodeList].forEach((item) => func());
```

## Homework

Last week:

Read: `https://javascript.info/variables` + Tasks
Read: `https://javascript.info/function-basics` + Tasks

New this week:

Read: `https://github.com/thejsway/thejsway/blob/master/manuscript/chapter04.md`
