
# Destructuring
Destructuring in JavaScript is a syntax that allows you to unpack values from arrays or properties from objects into distinct variables.

# Array Destructuring

Array destructuring allows you to unpack elements from an array into individual variables.

**Basic Example**
```
const array = [1, 2, 3];

const [first, second, third] = array;

console.log(first);  // 1
console.log(second); // 2
console.log(third);  // 3
```

**Skipping Elements**
You can skip elements by leaving a blank space in the destructuring pattern.

```
const array = [1, 2, 3, 4];

const [first, , third] = array;

console.log(first);  // 1
console.log(third);  // 3
```

**Using Rest Parameter**
You can use the rest parameter to collect remaining elements into a new array.

```
const array = [1, 2, 3, 4, 5];

const [first, second, ...rest] = array;

console.log(first);  // 1
console.log(second); // 2
console.log(rest);   // [3, 4, 5]
```

# Object Destructuring

Object destructuring allows you to unpack properties from an object into distinct variables.

**Basic Example**

```
const obj = { a: 1, b: 2, c: 3 };

const { a, b, c } = obj;

console.log(a); // 1
console.log(b); // 2
console.log(c); // 3
```

**Renaming Variables**
You can rename the variables while destructuring.

```
const obj = { a: 1, b: 2 };

const { a: alpha, b: beta } = obj;

console.log(alpha); // 1
console.log(beta);  // 2
```

**Using Rest Parameter**
You can use the rest parameter to collect remaining properties into a new object.

```
const obj = { a: 1, b: 2, c: 3 };

const { a, ...rest } = obj;

console.log(a);    // 1
console.log(rest); // { b: 2, c: 3 }
```


# Nested Destructuring
You can destructure nested arrays or objects.





