
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
