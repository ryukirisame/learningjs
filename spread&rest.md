# Spread & Rest Operator

The ... operator in JavaScript, known as the spread operator or rest parameter depending on the context, is a versatile tool that can be used for both expanding elements and collecting them into an array.

## Spread Operator
When used in an expansion context, the ... operator is called the spread operator. It is used to spread the elements of an array or object into individual elements.

```
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5, 6];
console.log(newArr); // [1, 2, 3, 4, 5, 6]
```

```
const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 };
console.log(newObj); // { a: 1, b: 2, c: 3 }

```

```
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];
console.log(sum(...numbers)); // 6
```

# Rest Parameter
When used in a function parameter context, the ... operator is called the rest parameter. It collects all remaining arguments into an array.

Here, ...numbers collects all arguments passed to the sum function into an array called numbers.
```
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

**Combining Destructuring and Rest Parameters**
```
const user = {
  id: 1,
  name: 'John',
  address: {
    street: '123 Main St',
    city: 'New York',
    country: 'USA'
  },
  hobbies: ['reading', 'traveling', 'sports']
};

const {
  name,
  address: { city, ...allOtherAddress },
  ...allOther
} = user;

console.log(name);       // 'John'
console.log(city);       // 'New York'
console.log(allOtherAddress); // { street: '123 Main St', country: 'USA' }
console.log(allOther);    // { id: 1, hobbies: ['reading', 'traveling', 'sports'] }
```



