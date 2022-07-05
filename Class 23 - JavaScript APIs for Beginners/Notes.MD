# Class 23 - JavaScript APIs for Beginners

## Agenda

- Review
- APIs

## Declaring Arrays

```js
let newArray = new Array();
```

Notice how this way to declare an array uses the `new` keyword and a capital letter: it must be a constructor function!
Therefore it's given properties like length, and methods like forEach.

The literal notation also provides this benefit, though!

```js
let newArray = [];
```

Because remember, under the hood it's an object!

**Let's Code: Space Review**

1. Create an array of numbers. Sum all the numbers. Alert the sum.

```js
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((acc, curr) => acc + curr, 0);
```

2. Create a function that takes in an array of numbers. Return a new array of numbers that is every original number squared.

```js
const squared = (numbers) => numbers.map((num) => Math.pow(num, 2));
```

3. Create a function that takes a string. Print the reverse of that string to the console.

```js
const reverseString = (string) => string.split('').reverse().join('');
```

4. Create a function that takes in a string. Alert if the string is a palindrome or not

```js
const isPalindrome = (string) => {
  string = string.toLowerCase().replaceAll(' ', '');
  for (let i = 0; i < string.length; i++) {
    if (string[i] != string[string.length - 1 - i]) return false;
  }

  return true;
};

// Another way
const isPalindrome = (string) =>
  string.toLowerCase().replaceAll(' ', '') == string.toLowerCase().replaceAll(' ', '').split('').reverse().join('');
```

## APIs

Application Programming Interface

- A **simple interface** for some complex action
- Think of a restaurant menu. We ask for an order and receive it back, without us having to know or care about how it was done.
- Lets one thing **communicate with another thing** without having to know how things are implemented

We will make a **request** to a server using a URL. That server will hear the request and send a **response** (typically **JSON**).

```js
fetch('https://dog.ceo/api/breeds/image/random")
.then(res => res.json())    // Parse response as JSON
.then(data => console.log(data))
.catch(err => console.log("Something went wrong"))
```