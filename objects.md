
# Arrays are objects

Arrays are a special kind of object where the keys are numeric indexes.

When you use Object.keys() on an array, it returns an array of the array’s indexes as strings. This is because arrays in JavaScript are objects, and Object.keys() returns the enumerable property names of the object. For arrays, these property names are the indexes (i.e., "0", "1", "2", etc.).

```
const arr = ['a', 'b', 'c'];

const keys = Object.keys(arr);
console.log(keys); // Output: ["0", "1", "2"]
```

- Arrays have additional properties and methods that are specific to arrays, such as length, push(), pop(), etc.  But, they are not enumerable.
- length is an own property, while push(), pop() etc are inherited from Array.prototype.


### Differences from Plain Objects
- Numeric Indexes: Arrays are optimized for numeric indexing,so, they use a numeric value as keys. While, plain objects use strings as keys.
- Arrays have an own length property that automatically updates as elements are added or removed. While, Objects do not have a built-in length property. The number of properties must be determined manually.
- Adding elements to an array automatically assigns them a numeric index. While, Keys must be explicitly defined when adding properties to an object.
- Ordering: Arrays maintain the order of elements based on their indexes, whereas the order of properties in plain objects is not guaranteed (though modern JavaScript engines maintain insertion order for string keys).


# in operator

The 'in' operator returns true if the specified property is in the specified object or its prototype chain.

The 'in' operator cannot be used to search for values in other collections. To test if a certain value exists in an array, use Array.prototype.includes(). For sets, use Set.prototype.has().

# Object.keys()
The Object.keys() static method returns an array of a given object's own enumerable string-keyed property names.

```
const object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};

console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```


# Object.values()

The Object.values() static method returns an array of a given object's own enumerable string-keyed property values.
```
const object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};

console.log(Object.values(object1));
// Expected output: Array ["somestring", 42, false]
```

# Object.entries()

The Object.entries() static method returns an array of a given object's own enumerable string-keyed property key-value pairs.

```
const object1 = {
  a: 'somestring',
  b: 42,
};

console.log(Object.entries(object1)) // [ [ 'a', 'somestring' ], [ 'b', 42 ] ]
```

# Object.prototype.hasOwnProperty()
The hasOwnProperty() method of Object instances returns a boolean indicating whether this object has the specified property as its own property (as opposed to inheriting it).

```
const object1 = {};
object1.property1 = 42;

console.log(object1.hasOwnProperty('property1'));
// Expected output: true

console.log(object1.hasOwnProperty('toString'));
// Expected output: false

console.log(object1.hasOwnProperty('hasOwnProperty'));
// Expected output: false
```

# Object.hasOwn()

- Object.hasOwn() is intended as a replacement for Object.prototype.hasOwnProperty().
- The Object.hasOwn() static method returns true if the specified object has the indicated property as its own property. If the property is inherited, or does not exist, the method returns false.

```
const object1 = {
  prop: 'exists',
};

console.log(Object.hasOwn(object1, 'prop'));
// Expected output: true

console.log(Object.hasOwn(object1, 'toString'));
// Expected output: false

console.log(Object.hasOwn(object1, 'undeclaredPropertyValue'));
// Expected output: false
```

# Object.create()

The Object.create() static method creates a new object, using an existing object as the prototype of the newly created object.

```
const person = {
  isHuman: false,
  printIntroduction: function () {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  },
};

const me = Object.create(person);

me.name = 'Matthew'; // "name" is a property set on "me", but not on "person"
me.isHuman = true; // Inherited properties can be overwritten

me.printIntroduction();
// Expected output: "My name is Matthew. Am I human? true"
```

# Object.getOwnPropertyNames()

Object.getOwnPropertyNames() is a method in JavaScript that returns an array of all properties (including non-enumerable properties) found directly on a given object. This includes both enumerable and non-enumerable properties but excludes properties inherited through the prototype chain.

```
const arr=[2,3,4,5];
console.log(Object.getOwnPropertyNames(arr));  // [ '0', '1', '2', '3', 'length' ]
```

# Object spread

When you use the spread operator (...) with an object in JavaScript, it expands the object's own enumerable properties into a new object.





