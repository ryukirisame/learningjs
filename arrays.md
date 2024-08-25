
# [2724. Sort By](https://leetcode.com/problems/sort-by/description/?envType=study-plan-v2&envId=30-days-of-javascript)

## Array.prototype.sort()


The sort() method in JavaScript is used to sort the elements of an array _**in place**_ and returns the sorted array. By default, sort() converts the elements into strings and sorts them in ascending order (based on UTF-16 code unit values). This can lead to unexpected results when sorting numbers unless a custom compare function is provided.

```
array.sort(compareFunction)
```
- compareFunction is optional

### Without a compareFunction

- The elements are sorted as strings in ascending order.

```
const arr = [10, 5, 20, 1];
arr.sort();
console.log(arr); // Output: [1, 10, 20, 5]
```

Here, the numbers are converted to strings ("10", "5", "20", "1") and then sorted lexicographically. This might not be the intended behavior when sorting numbers.

### With a compareFunction

The function takes two arguments, 'a' and 'b', representing two elements being compared. 

It should return a number where:
- A negative value indicates that 'a' should come before 'b'.
- A positive value indicates that 'a' should come after 'b'.
- Zero or NaN indicates that 'a' and 'b' are considered equal.
  
To memorize this, remember that (a, b) => a - b sorts numbers in ascending order.

```
myArr.sort((a,b)=> {
        return fn(a) - fn(b);
    });
```

# Array.prototype.slice()

The slice() method of Array instances returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified.

**Parameters**
1. start index
2. end index (excluded)

**Return value**
A new array containing the extracted elements.

### ****Meaning of Shallow Copy****
When you create a shallow copy of an array, like with the slice() method, the following happens:

#### Primitive Values

If the array contains primitive values (e.g., numbers, strings, booleans), these values are copied directly. Since primitives are immutable and are not references, this copying is straightforward.

#### Objects
If the array contains objects (e.g., arrays, objects, functions), only the references to these objects are copied. The actual objects themselves are not duplicated.
This means that both the original and the copied array will refer to the same objects. If you modify an object in one array, the change will be reflected in the other.

```
// Original array with primitive values and an object
const originalArray = [1, 2, { a: 3, b: 4 }, 4];

// Create a shallow copy of a portion of the array
const shallowCopy = originalArray.slice(1, 3);

console.log(shallowCopy); // Output: [2, { a: 3, b: 4 }]

// Modify an object in the copied array
shallowCopy[1].a = 10;

console.log(originalArray); // Output: [1, 2, { a: 10, b: 4 }, 4]
console.log(shallowCopy);   // Output: [2, { a: 10, b: 4 }]
```

# Array.prototype.splice()

The splice() method in JavaScript is used to modify an array in place. It allows you to add, remove, or replace elements at a specified index. Unlike slice(), which returns a new array, splice() changes the original array and can affect its length.

```
array.splice(start, deleteCount, item1, item2, ...)
```

- start: The index at which to start modifying the array. If start is greater than the length of the array, it starts at the end.
- deleteCount: The number of elements to remove from the array, starting from the start index. If deleteCount is omitted or set to 0, no elements are removed.
- item1, item2, ...: Items to add to the array starting from the start index. If no items are specified, splice() only removes elements.


**Return Value**
An array containing the deleted elements.
If only one element is removed, an array of one element is returned.
If no elements are removed, an empty array is returned.

```
const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// Inserts at index 1
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "June"]

months.splice(4, 1, 'May');
// Replaces 1 element at index 4
console.log(months);
// Expected output: Array ["Jan", "Feb", "March", "April", "May"]
```

# Array.prototype.includes()

The includes() method of Array instances determines whether an array includes a certain value among its entries, returning true or false as appropriate.

```
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// Expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// Expected output: true

console.log(pets.includes('at'));
// Expected output: false
```

# Array.prototype.indexOf()
The indexOf() method of Array instances returns the first index at which a given element can be found in the array, or -1 if it is not present.

```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// Expected output: 1

// Start from index 2
console.log(beasts.indexOf('bison', 2));
// Expected output: 4

console.log(beasts.indexOf('giraffe'));
// Expected output: -1
```

# Array.prototype.findIndex()

The findIndex() method of Array instances returns the index of the first element in an array that satisfies the provided testing function. If no elements satisfy the testing function, -1 is returned.

```
const array1 = [5, 12, 8, 130, 44];

const isLargeNumber = (element) => element > 13;

console.log(array1.findIndex(isLargeNumber));
// Expected output: 3
```


# Object.prototype.valueOf()

The valueOf() method is used to return the primitive value of an object. It is a built-in method available on various data types and objects and can be used to convert an object to its primitive representation.





















