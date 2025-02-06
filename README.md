# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Imagine you are teaching a friend about OOP. They mainly want to understand what is Encapsulation. Write a brief lesson on Encapsulation that includes the following:

- What is encapsulation?
- What major goal does this help to achieve in software engineering?
- Give an example (in code) of encapsulation.
- An explanation of how the code example demonstrates encapsulation

### Response 1

## Prompt 2

The following `friendsManager` object is an example of an interface that is **NOT** consistent and predictable:

```js
const friendsManager = {
  friends: [],
  addFriend(newFriend) {
    if (typeof newFriend !== "string") return;
    this.friends.push(newFriend);
  },
};

friendsManager.addFriend("daniel");
friendsManager.addFriend(true);
friendsManager.friends.push("emmanuel");
friendsManager.friends.push(42);
```

Explain how the code is not consistent or predictable, then provide an example in code that uses closure to make it more consistent and predictable.

### Response 2

>

## Prompt 3

With OOP in JavaScript, it's possible to use factory functions to achieve encapsulation and re-use them to make objects that look alike. However, factory functions have drawbacks and we often use classes instead.

How would you explain to a budding developer what the drawbacks of using factory functions are and why it is better to use classes instead?

### Response 3

## Prompt 4

Do some research on the history of when / how classes were introduced into JavaScript and share your findings. Your response should include:

- What version of JavaScript were classes introduced in and when did it come out?
- Why were classes introduced into JavaScript?

### Response 4

> In December 1999, ES3 introduced classes with classic functionality but also suffered from prototype pollution. For years, the community largely ignored prototypal inheritance, leading to the development of frameworks and libraries that provided classical inheritance abstractions. These abstractions allowed classes to be defined more conveniently through object literals.
>
> The main difference between ES5 and ES3 is that ES5 introduced property descriptors, enabling fine-grained control over property attributes. Additionally, ES5 introduced `Object.create()`, allowing the creation of objects with invisible prototype links instead of modifying existing ones.
>
> Over the years, ES6 improved the class system by:
>
> 1. Introducing shorthand syntax for object literal methods, eliminating the need to explicitly use the `function` keyword.
> 2. Providing the `super` reference, which is available in every method of a class that extends another class.
> 3. Allowing the creation of static methods and accessors.
>
> Beyond previous ECMAScript specifications, ES6 classes come with specific rules:
>
> 1. A subclass must always invoke `super()` inside its constructor.
> 2. The `this` reference cannot be accessed before calling `super()`.
> 3. Properties cannot be defined directly on the prototype, not even as public static constants.
>
> Classes were introduced in ECMAScript 2015 (ES6) to provide a more structured and readable way to implement object-oriented programming patterns in JavaScript. They simplify inheritance, improve code organization, and make JavaScript more accessible to developers familiar with classes.

## Prompt 5

OOP can still be achieved in JavaScript without using the `class` keyword and instead using the "Constructor Functions" and the "Prototype Chain" (look them up!)

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.greet = function () {
  return `Hi, I'm ${this.name}, and I'm ${this.age} years old.`;
};

const alice = new Person("Alice", 30);
console.log(alice.greet());
```

Provide one point that advocates for the use of this syntax and then provide a counter-argument for the use of classes instead.

### Response 5
