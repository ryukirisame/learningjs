
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

# Constructors

Here are few things we should know about functions: 

1. Functions in JS are also objects. They are special objects that can be invoked, called callable objects. So, functions can have properties just like an object does.
2. Every constructor function (functions in general) has a prototype property:
    - This 'prototype' property is an object.
    - It contains properties and methods that should be shared by all instances of the constructor function.
3. When an object is created using the 'new' keyword, the new object’s internal [[Prototype]] (which can be accessed via \__proto__ in modern browsers) is set to the constructor function’s prototype property.
4. The 'prototype' property in constructor function has a property called 'constructor' which references the constructor function itself. so when objects are created using new keyword and the 'prototype' is inherited then we can simply do 'obj.constructor' to get the original constructor from which the object was created.

5. 

