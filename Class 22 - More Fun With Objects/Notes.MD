# Class 22 - More Fun With Objects

## Agenda

- Let's Talk: #100Devs
- Review: Functions && Loops
- Review: Arrays
- Learn: Objects
- Learn: Basic APIs
- Homework: Object City Y'all

## Objects

What if we want to make **a lot** of objects? We'll, we'd need a sort of **factory**. We will learn how to create this concept, first with **constructors**, then with **Classes** (syntactical sugar).

```js
function MakeCar(carMake, carModel, carColor, numberOfDoors) {
  this.make = carMake;
  this.model = carModel;
  this.color = carColor;
  this.honk = function () {
    alert('BEEP BEEP');
  };
  this.lock = function () {
    alert(`Locked ${this.doors} doors!`);
  };
}

let hondaCivic = new MakeCar('Honda', 'Civic', 'Silver', 4);
let teslaRoadster = new MakeCar('Tesla', 'Roadster', 'Red', 2);
```

- Note the capital letter. This is common convention to let us know it is a constructor.
- Note we call the constructor function with the `new` keyword.

**Let's Code: Create a mouse Object that has four properties and three methods**

```js
// Using object literal
let mouse = {};
mouse.brand = 'Logitech';
mouse.color = 'white';
mouse.model = 'Xtreme Gaming';
mouse.isWireless = true;
mouse.leftClick = function () {
  console.log('Left Click');
};
mouse.rightClick = function () {
  console.log('Left Click');
};

// Oh no, we have a second mouse! I have to type all that again?? Not with constructors!
function Mouse(brand, color, model, isWireless) {
  this.brand = brand;
  this.color = color;
  this.model = model;
  this.isWireless = isWireless;
  this.leftClick = function () {
    console.log('Left Click');
  };
  this.rightClick = function () {
    console.log('Right Click');
  };
}

let mouse1 = new Mouse('Corsair', 'white', 'MMO', false);
let mouse2 = new Mouse('Logitech', 'black', 'Pro Wireless', true);
```

- Note when we console.log mouse1 or mouse2, we can see the factory the object came out of! Any object can look at itself and look at where it was made.
- So if we forget wher

Oops! We forgot to enable bluetooth in our Mouse factory! We can simply add it after the fact with:

```js
let teslaRoadster = new MakeCar('Tesla', 'Roadster', 'Red', 2);

MakeCar.prototype.bluetooth = true;

teslaRoadster.bluetooth; // true
```

A Prototype is another object that is used as a fallback source of properties.

Our Tesla Roadster looks at itself, sees it doesn't have bluetooth, and looks up to its prototype to see if it has bluetooth. If so, Tesla Roadster gets access to it!

This is called **prototypal inheritance**. An object will always check itself if it has a property or method. If not, it will then check its prototype up the inheritance chain.

The top-most object in the chain is `Object.prototype`. Every single thing in JS is an object, and they all inherit from this! Which is why a number has access to methods like `.toString()`.

If an `Array.prototype` doesn't have a method, it goes up to `Object.prototype` and asks. The same with `String.prototype`.

**Let's Code: Create a Street Fighter constructor that makes fighting game characters with 4 properties and 3 methods**

```js
function MakeFighter(name, kick, catchPhrase, specialMove) {
  this.name = name;
  this.kick = kick;
  this.taunt = taunt;
  this.special = special;

  this.taunt = function () {
    console.log(`You can't handle my ${this.specialMove}`);
  };

  this.winning = function () {
    console.log(`Haha! ${this.catchPhrase}`);
  };

  this.dash = function () {
    console.log('Whoopp, missed me!');
  };
}

const ryu = MakeFighter('Ryu', 'high', 'high', 'HADUUUUUUUKEN!', 'Haduken');
const ryu = MakeFighter();
```
