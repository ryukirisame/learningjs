
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

# Promises 

Callbacks come with their own set of challenges, such as Callback Hell and Inversion of Control. To address these issues, JavaScript introduced Promises—a more robust and manageable way to handle asynchronous code.

### Transitioning to Promises

```
const cart = ["jordan shoe", "titan watch", "van heusen shirt", "jeans"];

api.createOrder(cart)
    .then(() => api.proceedToPayment())
    .then(() => api.showOrderSummary())
    .then(() => api.updateWallet())
    .then(() => console.log("Order process completed successfully!"))
    .catch(error => console.error("An error occurred:", error));
```

#### Benefits of Using Promises:

- Flattened Structure: The code is no longer nested, making it easier to read and understand.
- Chained Operations: Promises allow you to chain operations, ensuring they execute in sequence without deep nesting.
- Centralized Error Handling: The .catch() block handles errors from any step in the chain, making error management simpler and more consistent.
- Control Over Execution: You maintain control over the flow of your code. You decide when and how the next step is executed, reducing the risk of unexpected behavior.
- Predictability: Promises provide a predictable and consistent way to handle asynchronous operations, reducing the chances of bugs and errors.
- Error Propagation: If an error occurs in createOrder, it will automatically propagate to the .catch() block, ensuring that issues are handled properly.


## A real world scenario

Imagine you walk into a restaurant and order a meal. The process of getting your meal can be thought of in terms of asynchronous operations. You don't just stand at the counter waiting for your food; instead, you place your order and then wait for it to be prepared and served. This is similar to how a Promise works in programming.

1. **Promise Creation**: When you place your order, the restaurant starts working on it. This is like creating a new Promise. The restaurant promises that your meal will be ready at some point in the future.
2. **Pending State**: While the restaurant is preparing your meal, you are in a "pending" state. You don't yet know whether the meal will be served perfectly (fulfilled) or if there will be a problem (rejected).
3. **Fulfilled State**: If everything goes well, the restaurant prepares your meal, and it's served to you. The Promise is fulfilled, and you can enjoy your food.
4. **Rejected State**: If something goes wrong (e.g., they run out of the ingredients needed for your meal), the restaurant might tell you that they can't fulfill your order. This is a rejection, and you need to decide what to do next (maybe order something else or leave the restaurant).

```
// A function that simulates ordering a meal at a restaurant
function orderMeal(meal) {
    return new Promise((resolve, reject) => {
        console.log(`Ordering ${meal}...`);

        // Simulate meal preparation time
        setTimeout(() => {
            const success = Math.random() > 0.2; // 80% chance of success

            if (success) {
                resolve(`Your ${meal} is ready! Enjoy your meal!`);
            } else {
                reject(`Sorry, we're out of ${meal} today.`);
            }
        }, 2000); // 2 seconds to prepare the meal
    });
}

// Placing an order and handling the result
orderMeal('pizza')
    .then(message => {
        console.log(message); // If the promise is fulfilled, this runs
    })
    .catch(error => {
        console.log(error); // If the promise is rejected, this runs
    });
```

- orderMeal Function: This function simulates the process of ordering a meal. It returns a Promise that either resolves with a success message or rejects with an error message after 2 seconds.
- resolve and reject: These are functions provided by the Promise. resolve is called when the meal is successfully prepared, while reject is called if something goes wrong (e.g., the restaurant is out of that meal).
- then: This method is used to specify what should happen if the Promise is fulfilled. In our example, it logs the success message to the console.
- catch: This method handles any errors that occur, such as the meal not being available.


## What is a Promise?

A Promise is an object representing the eventual completion or failure of an asynchronous operation.

**A Promise is in one of these states:**
- pending: initial state, neither fulfilled nor rejected.
- fulfilled: meaning that the operation was completed successfully.
- rejected: meaning that the operation failed.

![image](https://github.com/user-attachments/assets/06dcd653-2468-478b-a548-a8aa79814f6f)


### Creating a Promise
You create a Promise using the Promise constructor, which takes a function (called the executor) as an argument. This function is automatically executed when the Promise is created and receives two functions as arguments: resolve and reject.

- resolve: A function that, when called, changes the state of the Promise from pending to fulfilled and provides a value.
- reject: A function that, when called, changes the state of the Promise from pending to rejected and provides a reason (usually an error).


### Using Promises: .then(), .catch(), and .finally()
The promise methods then(), catch(), and finally() are used to associate further action with a promise that becomes settled.

NOTE: The catch() and finally() methods call then() internally and make error handling less verbose. For example, a catch() is really just a then() without passing the fulfillment handler.

### .then()
The .then() method is used to specify what should happen when the Promise is fulfilled. It takes two arguments:

- A function that handles the resolved value (fulfilled state).
- (Optional) A function that handles the rejection (rejected state).

#### Returning Values

1. If the callback function attached to .then() returns a non-Promise value, that value is automatically wrapped in a Promise. The new Promise will resolve with this value.
```
Promise.resolve(1)
  .then(value => {
    **return** value + 1;  // Returns a non-Promise value (2)
  })
  .then(result => console.log(result));  // Logs 2
```

2. If the callback function returns a Promise, .then() returns that Promise directly. The resulting Promise will adopt the state of the returned Promise (resolved or rejected).
```
Promise.resolve(1)
  .then(value => {
    **return** Promise.resolve(value + 1);  // Returns an existing Promise
  })
  .then(result => console.log(result));  // Logs 2
```

3. If the callback function throws an error, or returns a Promise that is rejected, the returned Promise will be rejected with that error.
```
Promise.resolve(1)
  .then(value => {
    throw new Error("Something went wrong!");  // Throws an error
  })
  .catch(error => console.log(error.message));  // Logs "Something went wrong!"
```

### .catch()
The .catch() method is a shorthand for handling errors (rejections) that occur in the Promise chain.

- In a Promise chain, if an error occurs in any .then() block, it will be passed down to the nearest .catch() block. This is because each .then() block returns a new Promise, and if this Promise is rejected, it will propagate down the chain until it finds a .catch() block that can handle the error.


### .finally()
The .finally() method is used to execute code after the Promise has been settled, regardless of whether it was fulfilled or rejected. This is useful for cleaning up resources or performing actions that should happen after the asynchronous operation is complete, no matter the outcome.


## Promise Chaining
One of the powerful features of Promises is chaining. Since .then() also returns a Promise, you can chain multiple asynchronous operations in sequence, ensuring that each operation completes before the next one starts.

```
fetchData()
  .then((response) => {
    return processResponse(response);
  })
  .then((processedData) => {
    return saveData(processedData);
  })
  .then(() => {
    console.log('Data saved successfully!');
  })
  .catch((error) => {
    console.error('An error occurred:', error);
  });
```

## Static Methods of Promises

- Promise.resolve(value): Returns a Promise that is resolved with the given value.
- Promise.reject(reason): Returns a Promise that is rejected with the given reason.
- Promise.all()
- Promise.allSettled()
- Promise.any()
- Promise.race()

# Advanced Promises Methods

## Promise.all()

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


## Promise.allSettled()

- ```Promise.allSettled(iterable)``` is a method in JavaScript that returns a promise that resolves after all of the given promises have either resolved or rejected. 
- Unlike Promise.all(), which short-circuits and rejects as soon as one promise rejects, Promise.allSettled() waits for all promises to settle (either resolve or reject) and then provides an array of objects describing the outcome of each promise.


### How It Works
Promise.allSettled() returns a promise that resolves with an array of results. Each result is an object with two properties:

- status: A string that is either "fulfilled" or "rejected".
- value (if status is "fulfilled"): The value with which the promise was fulfilled.
- reason (if status is "rejected"): The reason why the promise was rejected.

**Example**

```
const promise1 = Promise.resolve('Success');
const promise2 = Promise.reject('Error');
const promise3 = new Promise((resolve) => setTimeout(resolve, 100, 'Another success'));

Promise.allSettled([promise1, promise2, promise3])
  .then((results) => {
    results.forEach((result, index) => {
      console.log(`Promise ${index + 1}:`, result);
    });
  });

// Output
// Promise 1: { status: 'fulfilled', value: 'Success' }
// Promise 2: { status: 'rejected', reason: 'Error' }
// Promise 3: { status: 'fulfilled', value: 'Another success' }

```

- When handling the results of Promise.allSettled(), you typically check the status property of each result to determine whether the promise was fulfilled or rejected.
- Promise.allSettled() itself never rejects. It always resolves with an array of objects that describe the outcome of each promise, regardless of whether individual promises were fulfilled or rejected.


## Promise.race()

```Promise.race(iterable)``` is a JavaScript method that returns a promise that resolves or rejects as soon as one of the promises in the iterable resolves or rejects. It’s a way to get the result of the fastest promise, whether it’s fulfilled or rejected.

### Use Cases

**Timeout Handling**
Promise.race() is commonly used to implement timeout functionality for asynchronous operations. For example, you can race a fetch request against a timeout promise to ensure you don’t wait indefinitely:

Example:

```
const fetchPromise = fetch('https://jsonplaceholder.typicode.com/posts');
const timeoutPromise = new Promise((_, reject) =>
  setTimeout(() => reject(new Error('Request timed out')), 5000)
);

Promise.race([fetchPromise, timeoutPromise])
  .then((response) => {
    // Handle successful fetch
    return response.json();
  })
  .catch((error) => {
    // Handle timeout or fetch error
    console.error(error);
  });
```


## Promise.any()
```Promise.any(iterable)``` is a method in JavaScript that returns a promise that resolves as soon as any of the promises in the iterable resolves. If none of the promises resolve (i.e., all of them reject), it returns a promise that rejects with an AggregateError containing all the rejection reasons.


### How It Works
**Resolve**: Promise.any() returns a promise that resolves with the value of the first promise that resolves.

**Reject**: If all the promises in the iterable reject, Promise.any() returns a promise that rejects with an AggregateError, which is an object that aggregates individual errors together.


Example
```
const promise1 = new Promise((resolve, reject) => setTimeout(reject, 100, 'Error 1'));
const promise2 = new Promise((resolve, reject) => setTimeout(reject, 200, 'Error 2'));
const promise3 = new Promise((resolve, reject) => setTimeout(reject, 300, 'Error 3'));

Promise.any([promise1, promise2, promise3])
  .then((value) => {
    console.log(value);
  })
  .catch((error) => {
    console.error(error); // AggregateError: All promises were rejected
    console.error(error.errors); // ["Error 1", "Error 2", "Error 3"]
  });
```
