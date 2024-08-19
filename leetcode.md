
# [2724. Sort By](https://leetcode.com/problems/sort-by/description/?envType=study-plan-v2&envId=30-days-of-javascript)

## Array.prototype.sort()


The sort() method in JavaScript is used to sort the elements of an array _**in place**_ and returns the sorted array. By default, sort() converts the elements into strings and sorts them in ascending order (based on UTF-16 code unit values). This can lead to unexpected results when sorting numbers unless a custom compare function is provided.

```
array.sort([compareFunction])
```

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
- A negative value indicates that a should come before b.
- A positive value indicates that a should come after b.
- Zero or NaN indicates that a and b are considered equal.
  
To memorize this, remember that (a, b) => a - b sorts numbers in ascending order.


