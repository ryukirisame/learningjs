
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

### Own Properties

These are properties that are defined directly on the object, not inherited from its prototype.

```
const person = {
    name: "Alice"
};

console.log(person.hasOwnProperty('name')); // true
```

### Inherited Properties
These are properties that are inherited from an object's prototype chain. They are not directly on the object but can still be accessed as if they were.

```
const person = { name: "Alice" };

console.log(person.toString); // [Function: toString] (inherited from Object.prototype)
console.log(person.hasOwnProperty('toString')); // false
```

## Listing Own Properties Only
To list only the properties that belong directly to an object (ignoring inherited properties), you can use Object.keys() or Object.getOwnPropertyNames().

# Combining Enumerability and Ownership

## Enumerating own enumerables

### Using for...in Loop
The for...in loop iterates over all enumerable properties of an object, including those inherited from its prototype chain. However, you can filter out inherited properties using hasOwnProperty.
```
const obj = {
    name: 'Alice',
    age: 25,
    city: 'New York'
};

for (let key in obj) {
    if (obj.hasOwnProperty(key)) { // Filters out inherited properties
        console.log(key, obj[key]);
    }
}
```

### Using Object.keys()
Object.keys() returns an array of the object's own enumerable property names (keys).

```
const obj = {
    name: 'Alice',
    age: 25,
    city: 'New York'
};

const keys = Object.keys(obj);
keys.forEach(key => {
    console.log(key, obj[key]);
});
```

### Using Object.entries()
Object.entries() returns an array of the object's own enumerable property [key, value] pairs. You can then use forEach to iterate over them.

```
const obj = {
    name: 'Alice',
    age: 25,
    city: 'New York'
};

const entries = Object.entries(obj);
entries.forEach(([key, value]) => {
    console.log(key, value);
});
```

## Enumerating inherited enumerables

These are inherited properties that are enumerable. While Object.keys() does not list them, for...in will.

# Non-Enumerable Own Properties
Sometimes, you need properties to be non-enumerable but still owned by the object. This is often the case for internal properties or methods that should not be exposed during enumeration:
```
const person = {};
Object.defineProperty(person, 'secret', {
    value: 'hidden',
    enumerable: false
});

console.log(Object.keys(person)); // []
console.log(person.secret); // "hidden"
```

# Why all this?

- Hiding Internal Properties: Non-enumerable properties are often used to hide internal details of an object that should not be exposed in a loop or during property inspection.
- Inheritance Control: Understanding inherited properties helps in designing objects that extend functionality without polluting the object with unnecessary or irrelevant properties.
- Efficient Object Design: By managing enumerability and ownership, you can create objects that are efficient and predictable when iterating over properties.

# Why should we not use for...in loop to iterate over an array

Using for...in to iterate over the indices of an array in JavaScript is generally not safe because for...in does not just iterate over the array's indices (like 0, 1, 2, etc.). It also iterates over all enumerable properties, including inherited properties and any other enumerable properties that are not numeric indices.


```
// Example Array
const arr = [10, 20, 30];

// Adding a non-index property to the array
arr.customProperty = "I'm not an index";

// Adding a method to the array's prototype
Array.prototype.customMethod = function() {
    console.log("I'm a method on the prototype");
};

// Using for...in to iterate over the array
for (let key in arr) {
    console.log(key, arr[key]);
}
```
```
0 10
1 20
2 30
customProperty I'm not an index
customMethod function() { console.log("I'm a method on the prototype"); }
```

## Safe Alternatives

```
// Safe iteration using a for loop
for (let i = 0; i < arr.length; i++) {
    console.log(i, arr[i]);
}

// Safe iteration using forEach
arr.forEach((value, index) => {
    console.log(index, value);
});
```

Or, use a for-of loop, which has the added benefit of also working with other iterable data structures.









