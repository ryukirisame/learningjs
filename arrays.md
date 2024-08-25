
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

**Primitive Values:**

If the array contains primitive values (e.g., numbers, strings, booleans), these values are copied directly. Since primitives are immutable and are not references, this copying is straightforward.

**Objects:**
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











