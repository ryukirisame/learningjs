
# Inheritance

- In programming, inheritance refers to passing down characteristics from a parent to a child so that a new piece of code can reuse and build upon the features of an existing one.
- JavaScript implements inheritance by using objects. Each object has an internal link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype and acts as the final link in this prototype chain.
- It is possible to mutate any member of the prototype chain or even swap out the prototype at runtime, so concepts like static dispatching(compile time polymorphism) do not exist in JavaScript.

**NOTE**:  JavaScript is a dynamically typed language, meaning type information is not available at compile time but rather at runtime. This characteristic limits the ability to perform compile-time polymorphism as understood in statically typed languages.

## Objects
JavaScript objects are dynamic "bags" of properties (referred to as **_own properties_**).

Every object has an internal property [[Prototype]]. It is not directly accessible in JavaScript code. It refers to the prototype of the object, which is another object that the current object inherits properties and methods from. It's a hidden link that is used by the JavaScript engine to look up properties and methods on objects when they are not found directly on the object itself.

![image](https://github.com/user-attachments/assets/02d0f515-2a8b-49c0-b9ff-18b3032d7c6c)

\__proto__ is an accessor property that allows you to get or set the [[Prototype]] of an object. It is widely supported in all major browsers, although it is not recommended to use it in production code due to its legacy nature and potential performance issues. It allows you to interact with the [[Prototype]] internal property directly. In modern JavaScript, it's more common and recommended to use Object.create(), Object.getPrototypeOf(), and Object.setPrototypeOf() to interact with prototypes.

An example: 
```
const o = {
  a: 1,
  b: 2,
  // __proto__ sets the [[Prototype]]. It's specified here
  // as another object literal.
  __proto__: {
    b: 3,
    c: 4,
  },
};

// o.[[Prototype]] has properties b and c.
// o.[[Prototype]].[[Prototype]] is Object.prototype (we will explain
// what that means later).
// Finally, o.[[Prototype]].[[Prototype]].[[Prototype]] is null.
// This is the end of the prototype chain, as null,
// by definition, has no [[Prototype]].
// Thus, the full prototype chain looks like:
// { a: 1, b: 2 } ---> { b: 3, c: 4 } ---> Object.prototype ---> null

console.log(o.a); // 1
// Is there an 'a' own property on o? Yes, and its value is 1.

console.log(o.b); // 2
// Is there a 'b' own property on o? Yes, and its value is 2.
// The prototype also has a 'b' property, but it's not visited.
// This is called **Property Shadowing**

console.log(o.c); // 4
// Is there a 'c' own property on o? No, check its prototype.
// Is there a 'c' own property on o.[[Prototype]]? Yes, its value is 4.

console.log(o.d); // undefined
// Is there a 'd' own property on o? No, check its prototype.
// Is there a 'd' own property on o.[[Prototype]]? No, check its prototype.
// o.[[Prototype]].[[Prototype]] is Object.prototype and
// there is no 'd' property by default, check its prototype.
// o.[[Prototype]].[[Prototype]].[[Prototype]] is null, stop searching,
// no property found, return undefined.
```

Property Shadowing: Basically property overriding. If the child and parent both has a certain property, then the child version of the property is preferred. 


## Inheriting 'methods'

When an inherited function is executed, the value of 'this' points to the inheriting object, not to the prototype object where the function is an own property.

```
const parent = {
  value: 2,
  method() {
    return this.value + 1;
  },
};

console.log(parent.method()); // 3
// When calling parent.method in this case, 'this' refers to parent

// child is an object that inherits from parent
const child = {
  __proto__: parent,
};
console.log(child.method()); // 3
// When child.method is called, 'this' refers to child.
// So when child inherits the method of parent,
// The property 'value' is sought on child. However, since child
// doesn't have an own property called 'value', the property is
// found on the [[Prototype]], which is parent.value.

child.value = 4; // assign the value 4 to the property 'value' on child.
// This shadows the 'value' property on parent.
// The child object now looks like:
// { value: 4, __proto__: { value: 2, method: [Function] } }
console.log(child.method()); // 5
// Since child now has the 'value' property, 'this.value' means
// child.value instead
```

## Functions

Here are few things we should know about functions: 

1. Functions in JS are also objects. They are special objects that can be invoked, called callable objects. So, functions can have properties just like an object does.
2. Every constructor function (functions in general) has a prototype property:
    - This 'prototype' property is an object.
    - It contains properties and methods that should be shared by all instances of the constructor function.
3. When an object is created using the 'new' keyword, the new object’s internal [[Prototype]] (which can be accessed via \__proto__ in modern browsers) is set to the constructor function’s prototype property.
4. The 'prototype' property in constructor function has a property called 'constructor' which references the constructor function itself. so when objects are created using new keyword and the 'prototype' is inherited then we can simply do 'obj.constructor' to get the original constructor from which the object was created.

<img src="https://github.com/user-attachments/assets/49ded817-60f7-4e0d-a36b-5be20cf4ac31" width="600px"/>

## Constructor Functions

Suppose we are to create a series of boxes, where each box is an object that contains a value which can be accessed through a getValue function. A naive implementation would be:

```
const boxes = [
  { value: 1, getValue() { return this.value; } },
  { value: 2, getValue() { return this.value; } },
  { value: 3, getValue() { return this.value; } },
];
```

This is subpar (below standard) code, because each instance has its own function property that does the same thing, which is redundant and unnecessary. 
Instead, we can move getValue to the [[Prototype]] of all boxes:
```
const boxPrototype = {
  getValue() {
    return this.value;
  },
};

const boxes = [
  { value: 1, __proto__: boxPrototype },
  { value: 2, __proto__: boxPrototype },
  { value: 3, __proto__: boxPrototype },
];
```

This way, all boxes' getValue method will refer to the same function, lowering memory usage. 
However, manually binding the __proto__ for every object creation is still very inconvenient. This is when we would use a constructor function, which automatically sets the [[Prototype]] for every object manufactured. Constructors are functions called with 'new'.

```
// A constructor function
function Box(value) {
  this.value = value;
}

// Properties all boxes created from the Box() constructor
// will have
Box.prototype.getValue = function () {
  return this.value;
};

const boxes = [new Box(1), new Box(2), new Box(3)];
```

We say that new Box(1) is an instance created from the Box constructor function. Box.prototype is not much different from the boxPrototype object we created previously — it's just a plain object. Every instance created from a constructor function will automatically have the constructor's prototype property as its [[Prototype]] — that is, Object.getPrototypeOf(new Box()) === Box.prototype.


## A Catch

Re-assigning Constructor.prototype (Box.prototype = {...}) is a bad idea.

```
function Box(value) {
  this.value = value;
}

Box.prototype.getValue = function () {
  console.log(this.value);
};

const box = new Box(1);
box.getValue(); // 1

// Mutate Box.prototype after an instance has already been created.
// Here, we are re-assigning the prototype object itself.
Box.prototype={
    getValue(){
        console.log(this.value + 2);
    },
    constructor: Box
}

const box2=new Box(1);

box.getValue(); // 1. since its still referencing to old prototype object
box2.getValue(); // 3. since its referencing to new prototype object;
```
<img src="https://github.com/user-attachments/assets/ff9eae1c-cf8d-47c6-9d05-30fe250e6362" width="600px"/>


![image](https://github.com/user-attachments/assets/194d4888-199f-4101-bda7-e7945c9a430b)

We see that the [[Prototype]] of box and box2 are now pointing to two different objects.
Also, 'constructor' property in prototype of box2 is not available. 

Unless you manually re-set the constructor property, the constructor function can no longer be traced from instance.constructor, which may break user expectation. Some built-in operations will read the constructor property as well, and if it is not set, they may not work as expected


## Implicit constructors of literals

Some literal syntaxes in JavaScript create instances that implicitly set the [[Prototype]]. For example:

```
// Object literals (without the `__proto__` key) automatically
// have `Object.prototype` as their `[[Prototype]]`
const object = { a: 1 };
Object.getPrototypeOf(object) === Object.prototype; // true

// Array literals automatically have `Array.prototype` as their `[[Prototype]]`
const array = [1, 2, 3];
Object.getPrototypeOf(array) === Array.prototype; // true

// RegExp literals automatically have `RegExp.prototype` as their `[[Prototype]]`
const regexp = /abc/;
Object.getPrototypeOf(regexp) === RegExp.prototype; // true
```

## Building longer inheritance chains

To build longer prototype chains, we can set the [[Prototype]] of Constructor.prototype via the Object.setPrototypeOf() function.

```
function Base() {}
function Derived() {}
// Set the `[[Prototype]]` of `Derived.prototype`
// to `Base.prototype`
Object.setPrototypeOf(Derived.prototype, Base.prototype);

const obj = new Derived();
// obj ---> Derived.prototype ---> Base.prototype ---> Object.prototype ---> null
```

In class terms, this is equivalent to using the 'extends' syntax.

```
class Base {}
class Derived extends Base {}

const obj = new Derived();
// obj ---> Derived.prototype ---> Base.prototype ---> Object.prototype ---> null
```

### An Example

```
// Parent Constructor Function
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function () {
  console.log(`${this.name} makes a sound.`);
};

// Child Constructor Function
function Dog(name, breed) {
  // Inherit the name property from Animal
  Animal.call(this, name);  // note: we are not using new keyword here, so this call doesn't create a new animal object.
  this.breed = breed;
}

// Set up inheritance
Object.setPrototypeOf(Dog.prototype, Animal.prototype);

// Override speak method in Dog prototype
Dog.prototype.speak = function () {
  console.log(`${this.name} barks.`);
};

// Add additional method to Dog prototype
Dog.prototype.fetch = function () {
  console.log(`${this.name} is fetching a ball.`);
};

// Usage Examples
const animal = new Animal("Generic Animal");
animal.speak(); // Output: 'Generic Animal makes a sound.'

const dog = new Dog("Buddy", "Golden Retriever");
dog.speak(); // Output: 'Buddy barks.'
dog.fetch(); // Output: 'Buddy is fetching a ball.'

// Checking instanceof
console.log(dog instanceof Dog); // Output: true
console.log(dog instanceof Animal); // Output: true
console.log(animal instanceof Dog); // Output: false
console.log(animal instanceof Animal); // Output: true
```

**Explanation**

When we do new Dog("Buddy", "Golden Retriever"), the following happens:
1. A new plain object is created. 
2. The [[Prototype]] of the new plain object is set to Dog.prototype object.
3. Then, the Dog constructor function starts to execute, with "this" referencing to the newly created plain object. 
4. Now, the first line encountered in Dog() is Animal.call(this, name). So what happens is, the Animal function is invoked with "this" as the context, which means the newly created object as the context.
5. Notice, that we did not use new keyword infront of Animal.call(), because we are not trying to create a new Animal object here, we are simply trying to inherit the properties of Animal.
6. The Animal() executes, and the newly created object will have name property set to "Buddy". So now the updated newly created object will be : {name : "Buddy"}.
7. Then, we come back to Dog() constructor, and the next line adds the "breed" property to the new object. So, now the object becomes: {name: "buddy" , breed: "Golden Retriever"}
8. Then finally, the new object will be returned and its reference will be stored in the dog variable.
9. Notice, that we have set the prototype of Dog.prototype to Animal.prototype.
10. So, the prototype chain becomes: dog -> Dog.prototype -> Animal.prototype 
11. So, now we have a prototype chain setup. So basically, the dog inherits everything from the two prototypes.
12. Also, the dog object has all the properties of animal and dog both. which is: name and breed.
13. All this process becomes equivalent to extending Animal class by the Dog class, if we were to use Classes instead of this constructor function syntax, which looks complicated.
14. So, whenever we have to setup a multi-level inheritance, we should prefer classes, as it abstracts away the pain of calling the parent constructor function and setting up the prototype chain manually.

### Class Version of the Same Code

```
// Parent Class
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

// Child Class
class Dog extends Animal {
  constructor(name, breed) {
    // Call the parent constructor with `super`
    super(name);
    this.breed = breed;
  }

  // Override speak method in Dog class
  speak() {
    console.log(`${this.name} barks.`);
  }

  // Add additional method specific to Dog
  fetch() {
    console.log(`${this.name} is fetching a ball.`);
  }
}

// Usage Examples
const animal = new Animal("Generic Animal");
animal.speak(); // Output: 'Generic Animal makes a sound.'

const dog = new Dog("Buddy", "Golden Retriever");
dog.speak(); // Output: 'Buddy barks.'
dog.fetch(); // Output: 'Buddy is fetching a ball.'

// Checking instanceof
console.log(dog instanceof Dog);    // Output: true
console.log(dog instanceof Animal); // Output: true
console.log(animal instanceof Dog); // Output: false
console.log(animal instanceof Animal); // Output: true
```

# Checking if an object is an instance of a class (without using instanceof)
https://leetcode.com/problems/check-if-object-instance-of-class/


