# Class 31 - Inheritance & Polymorphism

## Agenda

- Let's Talk: #100Devs
- Learn: Objects
- Learn: Basic OOP Principles
- Do: Work In Teams: The Four Pillars
- Do: Work In Teams: Tic-tac-toe
- Homework: Object City

## Inheritance

We can **extend** our classes:

```js
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }
}

let simba = new Dog('Simba', 'Shepherd');
```

Doing so allows us to make use of **Inheritance** -- making a class from another class for a hierarchy of classes that share a set of properties and methods.

We can use the concept of private properties as follows:

```js
class Animal {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name;
  }

  speak() {
    console.log(`${this._name} makes a sound`);
  }
}

let simba = new Animal('Simba');

simba.name = 'Bob'; // Won't allow us to change name -- perfect!
```

However, note that `_name` can still be accessed and changed. It is just _convention_ to use underscore and have everyone agree to not modify this property.

## Polymorphism

Code written to use an interface automatically knows how to work with any number of different objects that provide the interface.
Sibling descendants of a base class will all have the same interface but varying implementations.
When you are not sure of the objects type at runtime, the most specific method is called. Therefore the behavior of the method called may differ, depending on the objects type at runtime.
Provides a way to perform a single action in different forms.
Provides an ability to call the same method on different JavaScript objects.
Instead of conditionals and switch cases.

That's the power of Polymorphism!

## Four Pillars Review

**Encapsulation**

The process of storing functions (methods) with their associated data (properties) in one thing (object).

Why?

- Makes it easier to add new stuff
- Makes it easier to read through what was already coded
- Makes it so you are not afraid to make changes

**Abstraction**

Hide details and show essentials.

Why?

- Smaller, more manageable pieces of code
- Make code changes and still sleep at night!

**Inheritance**

Make a class from another class for a hierarchy of classes that share a set of properties and methods.

Why?

- Helps you eliminate redundant code

**Polymorphism**

Code written to use an interface automatically knows how to work with any number of different objects that provide the interface.

Why?

- Helps you avoid if/else and switch cases! Don't have to check something's _type_ before running logic on it
- Makes your code more reusable

## Homework

Do: Get a paid client, Volunteer, or contribute to free software
Do: FINISH _Professional Checklist_
Do: Codewars Array Ladder (search array problems) - 8kyu, 7kyu, 6kyu, 7kyu, 8kyu
