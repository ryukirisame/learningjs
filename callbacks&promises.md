
# Importance of Callback Functions
Callbacks enables asynchronous programming in JS.

# Issues with Callbacks

1. Callback Hell
2. Inversion of Control

## Callback Hell

Let's suppose we have an E-Commerce site. 
The flow is like this: Order is Created -> Payment -> Order Summary -> Update Wallet

Now, let's suppose we have different API's for each action. Now, the issue is, the API's must be called in a given sequence.
With our current knowledge of Callbacks, what we can do is like this:

```
const cart = ["jordan shoe", "titan watch", "van heusen shirt", "jeans"];

api.createOrder(cart, function () {
  api.proceedToPayment(function () {
    api.showOrderSummary(function () {
      api.updateWallet();
    });
  });
});
```

As we can see, we have multiple nested callbacks. This happened because the sequence of operations must be maintained.
This is making the code grow horizontally, rather than vertically. This kind of code will make it difficult for us to debug and is complex to read.

This multiple nesting of callbacks is called Callback Hell (Pyramid of Doom).

## Inversion of Control

Let's consider this code:
```
api.createOrder(cart, function () {
        api.proceedToPayment();
});
```
Here, we see that we are passing a callback function to createOrder API. Now, the control of calling the proceedToPayment API has been given to createOrder API, instead of us explicitly calling the payment API ourselves. This is called inversion of control, where we lose control over our code.

### Issues with Inversion of Control
- Unpredictability: We don't know how the code is written inside the createOrder API and how it will affect our proceedToPayment function.
- Execution Guarantee: Will our proceedToPayment function be called as expected? There is uncertainty about the callback's execution.
- Multiple Invocations: What if the proceedToPayment function is called multiple times due to a bug or logic error inside createOrder?
- Error Handling: We are reliant on the createOrder API to handle errors properly. If it has bugs, our callback may not execute correctly or at all.




# Advanced Promises Methods

## Promises.all()

```Promise.all(iterable)``` is a method in JavaScript that allows you to handle multiple promises concurrently. It takes an iterable (like an array) of promises and returns a single promise that resolves when all of the promises in the iterable have resolved, or rejects if any of the promises reject.

### How it works
**Resolve**: Promise.all() resolves when all promises in the iterable have resolved. It returns an array of the results, in the same order as the original promises.
**Reject**: Promise.all() rejects as soon as any promise in the iterable rejects. The returned promise rejects with the reason of the first promise that rejects.

**Example**
```
const promise1 = Promise.resolve(3);
const promise2 = 42;
const promise3 = new Promise((resolve, reject) => {
  setTimeout(resolve, 100, 'foo');
});

Promise.all([promise1, promise2, promise3]).then((values) => {
  console.log(values); // [3, 42, "foo"]
}).catch((error) => {
  console.error(error);
});
```

### Handling Errors
If any of the promises reject, Promise.all() will reject with the reason of the first promise that rejects.

```
const promise1 = Promise.resolve('success');
const promise2 = Promise.reject('error');
const promise3 = new Promise((resolve) => {
  setTimeout(resolve, 100, 'another success');
});

Promise.all([promise1, promise2, promise3]).then((values) => {
  console.log(values);
}).catch((error) => {
  console.error(error); // "error"
});
```

### Use Cases

**Fetching Multiple Resources**

You can use Promise.all() to fetch multiple resources concurrently and process the results once all fetches have completed.

```
const urls = [
  'https://jsonplaceholder.typicode.com/posts/1',
  'https://jsonplaceholder.typicode.com/posts/2',
  'https://jsonplaceholder.typicode.com/posts/3'
];

const fetchPromises = urls.map(url => fetch(url).then(response => response.json()));

Promise.all(fetchPromises).then((results) => {
  results.forEach(result => {
    console.log(result);
  });
}).catch((error) => {
  console.error('Error fetching data:', error);
});
```

**NOTE**
1. Non-Promise Values: If the iterable contains non-promise values, they are treated as if they were resolved promises with those values.
2. Performance: Using Promise.all() can be more efficient than awaiting each promise individually, especially when the promises are independent of each other and can run concurrently.
3. Error Handling: When using Promise.all(), it's important to handle errors appropriately, as a single rejected promise will cause the entire operation to fail.




