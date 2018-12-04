# Class Extensions and Inheritance: `extends`

## Learning Goals

- Use the `extends` keyword

## Introduction

In JavaScript, as in other Object Oriented languages, we've learned
that you can create classes and build methods that can perform
actions on instance data, or specific to the class. What if you have
classes that exhibit many of the same behaviors, such as `Cat`, `Dog`,
and `Bird`, which all have a method for `speak`?

```js
class Dog {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} says woof!`
  }
}

class Cat {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} says meow!`
  }
}

class Bird {
  constructor(name) {
    this.name = name;
  }
  speak() {

      return `${this.name} says squawk!`
    }
  }
```

In JavaScript, you can create "child" object classes that inherit methods
from their "parent" classes. In this lesson, we'll discuss 1 way of
_extending_ functionality to other classes.

## Use the `extends` Keyword

To get started with inheriting class functionality, we utilize the `extends`
keyword. `extends` is used in class declarations to create a class which
is a _child_ of another class.

```js
class Pet {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} makes a loud sound!`
  }
}

// Inherits from Pet
class Dog extends Pet { ... }
class Cat extends Pet { ... }
class Bird extends Pet {
  constructor(name) {
    this.name = name;
  }

  fly() {
    return `${this.name} flies away!`
  }
}

let dog = new Dog("Shadow");
let cat = new Dog("Missy");
let bird = new Dog("Tiki");

dog.speak(); // Shadow makes a loud sound!
cat.speak(); // Missy makes a loud sound!
bird.speak(); // Tiki makes a loud sound!
bird.fly(); // Tiki flies away!
```

In addition to _inheriting_ the functionality of the `Pet` class, each "child"
class extending the functionality of the parent. For example, `Bird` has an
additional method called `fly` that is unique to it, and not present on `Pet`.
`Bird` can still call `speak()`.

## Conclusion

In this lesson, we learned about more functionality in JavaScript that allows us to leverage
Object Orientation concepts: class extensions and inheritance. With `extends` we can create 
new classes that are capable utilizing of all the same methods as its parent. Leveraging
inheritance and `extends` is vital in Object Oriented programming. It keep cade bases maintainable
by sharing and reusing code in a beneficial manner.

## Resources

* [Inheritance in JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Inheritance)
* [Extends](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/extends)
* [“Super” and “Extends” In JavaScript ES6 - Understanding The Tough Parts](https://medium.com/beginners-guide-to-mobile-web-development/super-and-extends-in-javascript-es6-understanding-the-tough-parts-6120372d3420)