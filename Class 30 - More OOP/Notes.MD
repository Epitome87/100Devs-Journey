# Class 30 - OOP But it Actually Makes Sense!

## Agenda

- Let's Talk: #100 Devs
- Learn: Objects
- Learn: Basic OOP Principles
- Do: Work in Teams: Tic-tac-toe
- Homework: Object City

```js
// Create expresso machine class
class EspressoMachine {
    constructor(color, make, model, price) {
        this.color color;
        this.make = make;
        this.model = model;
        this.price = price;
    }
    turnOn() {
        console.log("Good day, I am on now!");
    }
    steam() {
        console.log("Hsssss");
    }
    brew() {
        console.log("Good stuff coming your way!");
    }
}

let gaggia = new EspressoMachine("red", "Gaggia", "Classic Pro", 400);
gaggia.turnOn();
gaggia.steam();
gaggia.brew();
```

## Encapsulation

The process of storing functions (methods) with their associated data (properties) -- in one thing (object).

Why? It makes it easier to add new functionality and data. Keeps code more readable.

- Makes it easier to add new stuff
- Makes it easier to read through what was already coded
- Makes it so you're not afraid to make changes.

## Abstraction

Complex or unnecessary details are hidden.
This enables you to implement things without understanding or even thinking about all the hidden complexity.
Smaller more manageable pieces of code.
Do stuff only once!

The process of achieving all the above is **Abstraction** -- hide details and show essentials. Simple, predictable, manageable.

Why?

- Smaller more manageable pieces of code. Helps you split the complexity of your software project into manageable parts.

## Homework

- Watch / Do: https://youtu.be/PFmuCDHHpwk
- Read / Do: JS Way Chapter 09
- Push? Read / Do: Eloquent JavaSCript Chapter 06
- Do: 7 Codewars
