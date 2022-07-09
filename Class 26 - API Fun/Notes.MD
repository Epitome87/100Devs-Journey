# Class 26 - API Fun

## Objects - Review

Nothing new, really.

```js
function Person(name, age, location, hobbies) {
  this.name = name;
  this.age = age;
  this.location = location;
  this.hobbies = hobbies;

  this.doStuff = function () {
    return this.name;
  };
}

// Class version
class Person {
  constructor(name, age, location, hobbies) {
    this.name = name;
    this.age = age;
    this.location = location;
    this.hobbies = hobbies;
  }

  doStuff() {
    return this.name;
  }
}
```

## API - Review

Nothing new!
