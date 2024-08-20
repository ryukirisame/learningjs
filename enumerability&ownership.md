
# Enumeration

- In JavaScript, enumeration refers to the process of listing all the properties of an object. When you enumerate the properties of an object, you go through each property and either perform an action on it (like logging it to the console) or gather those properties in some way (like creating an array of them). This is commonly done using loops or certain methods.
- When you enumerate the properties of an object, you’re essentially looping through all of its enumerable properties. Enumerable properties are those that are flagged to be listed in enumeration processes like for...in loops or Object.keys().

# Enumerability

Every property in JavaScript objects can be classified by three factors:
1. Enumerable or non-enumerable;
2. String or symbol;
3. Own property or inherited property from the prototype chain.

- Enumerability refers to whether a property of an object can be listed in a loop that iterates over the properties of that object, such as for...in, Object.keys(), or similar methods.

## What is an Enumerable Property?
- Enumerable properties are those properties whose internal enumerable flag is set to true. So, they are included in a loop or method that iterates over an object's properties. 
- By default, properties that you add to an object via direct assignment or object literals are enumerable.

### How to Check if a Property is Enumerable
You can check whether a property is enumerable using the ```propertyIsEnumerable()``` method.
```
const person = {
    name: "Alice",
    age: 30
};

console.log(person.propertyIsEnumerable('name')); // Output: true
console.log(person.propertyIsEnumerable('toString')); // Output: false (inherited from Object.prototype)
```

### Setting a Property's Enumerable Attribute
When you define a property using Object.defineProperty(), you can control whether the property is enumerable by setting the enumerable attribute.

```
const person = {};

// Define a property with enumerable set to true (default)
Object.defineProperty(person, 'name', {
    value: 'Alice',
    enumerable: true
});

// Define a non-enumerable property
Object.defineProperty(person, 'age', {
    value: 30,
    enumerable: false
});

console.log(Object.keys(person)); // Output: ["name"]
console.log(person.propertyIsEnumerable('age')); // Output: false
```
## Non-Enumerable Properties
- Non-enumerable properties in JavaScript are properties of an object that do not show up during property enumeration. 
- You can still access non-enumerable properties directly by their key, just like any other property.
- Many properties of JavaScript's built-in objects, like length on arrays or methods like toString() on objects, are non-enumerable.
- You can create a non-enumerable property using Object.defineProperty() by setting the enumerable attribute to false.

# Ownership of Properties

Ownership refers to whether a property belongs directly to the object itself or if it is inherited from the object's prototype chain.

## Own Properties

These are properties that are defined directly on the object, not inherited from its prototype.

```
const person = {
    name: "Alice"
};

console.log(person.hasOwnProperty('name')); // true
```

## Inherited Properties
These are properties that are inherited from an object's prototype chain. They are not directly on the object but can still be accessed as if they were.

```
const person = { name: "Alice" };

console.log(person.toString); // [Function: toString] (inherited from Object.prototype)
console.log(person.hasOwnProperty('toString')); // false
```

