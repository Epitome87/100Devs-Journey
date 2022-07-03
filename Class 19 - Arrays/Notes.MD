# Class 16 - JavaScript Loops

## Agenda

- Let's Talk: #100Devs
- Review - Functions && Loops
- Learn: Arrays
- Learn: Array Iteration
- Learn: Array Methods
- Homework: Objects

## Arrays

- A data structure to store **ordered collections**
- Array elements are numbered **starting with zero**
- Arrays have many **methods** to **manage the order** of elements
- Can be **created by a constructor** or **literal notation**

Arrays have an **element** and an **index** (ranging from 0 to 1 less than the array's length).

### Declaring Arrays

**Literal Notation**

```js
let newArr = [];
```

**Array Constructor**

```js
let newArr = new Array();
```

Arrays are populated with elements. Elements can be of any type

```js
newArr = ['Zebra', true, 21];
```

Be careful: An empty space counts as an element!

### Array Indexing

Elements can be accessed by their index numbers:

```js
newArr = ['Zebra', , true, 21];
newArr[0]; // Zebra
newArr[1]; // undefined
```

Elements can be updated by using the index at that position:

```js
newArr = ['Zebra', , true, 21];
newArr[1] = 'Bob';

newArr; // 'Zebra', 'Bob', true, 21
```

You can overwrite whole arrays by assigning an array to a different array:

```js
let cars = ['Honda', 'Toyota', 'Ford', 'Tesla'];
let nums = [1, 2, 3];

cars = nums; // cars: [1, 2, 3]
```

### Array Length

How do you determine how many elements are in your array? The **length property**. Note it is a property, not a method!

```js
newArray.length; // 4
```

### Array Iteration

Iterates through an array passing in the value and index of each element:

```js
let bestColors = ['red', 'green', 'blue'];

for (let i = 0; i < bestColors.length; i++) {
  console.log(bestColors[i]);
}
```

There is also the .forEach array method:

```js
bestColors.forEach((element, index, arr) => console.log(x, i, arr));
bestColors.forEach((element, index) => console.log(x, i));
bestColors.forEach((element) => console.log(x));
```

Note we don't have to grab the index or array parameter if we don't need it, so we can exclude it.
