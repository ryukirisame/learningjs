# async-await

```async``` and ```await``` are syntax features in JavaScript that make working with promises more intuitive and readable. They allow you to write asynchronous code that "**looks**" like synchronous code, but without blocking the execution thread.

# async Functions

- An async function is a function that returns a promise. The async keyword is used to define a function as asynchronous.
- When you call an async function, it always returns a promise, regardless of what you return inside the function. If the function returns a non-promise value, that value is automatically wrapped in a resolved promise using Promise.resolve(). If we don't return anything, then the function will implicitly return a promise that resolves to undefined.

**Example**
```
async function example() {
  return 'Hello, world!';
}

example().then(result => console.log(result)); // "Hello, world!"
```

- **Error Handling**: Inside an async function, if an exception is thrown, it results in the returned promise being rejected. This is equivalent to returning a rejected promise.
```
async function throwError() {
  throw new Error('Something went wrong');
}

throwError().catch(error => console.error(error)); // Error: Something went wrong
```

# await Keyword

- This keyword is used to pause the execution of an async function until the promise it is waiting for settles (either resolves or rejects).
- await can only be used inside async functions.
- Basically, the await checks the state of the Promise. If the Promise is pending, the function execution is suspended, and the function context is removed from the call stack.

**Syntax**
```const result = await expression;```

Here, expression is typically a Promise. The await keyword pauses the execution of the async function until the Promise resolves or rejects.

If you await a value that is not a Promise (like a number, string, or object), JavaScript automatically wraps that value in a resolved Promise. The await keyword will immediately return the value without any delay.
```
const value = await 42; // This is treated as Promise.resolve(42)
console.log(value); // 42
```

**Returning the Value:**
- If the Promise resolves, await returns the resolved value.
- If the Promise rejects, await throws the rejection as an exception (which can be caught using try...catch).

# How async and await combo works

Consider the following code
```
async function fetchData() {
  console.log('1: Start fetching data');
  
  let response = await fetch('https://jsonplaceholder.typicode.com/todos/1');
  console.log('2: Response received');
  
  let data = await response.json();
  console.log('3: Data processed');
  
  return data;
}

console.log('A: Before calling fetchData');
fetchData().then(result => {
  console.log('4: Final result', result);
});
console.log('B: After calling fetchData');
```

### Initial Code Execution
When JavaScript starts executing this code:

- Step 1: ```console.log('A: Before calling fetchData');``` is executed, and "A: Before calling fetchData" is logged to the console.
- Step 2: fetchData() is called, and the fetchData function begins executing.

### Entering the async Function
- Step 3: The fetchData function is now on the call stack. The code inside fetchData starts running.
- Step 4: ```console.log('1: Start fetching data');``` is executed, and "1: Start fetching data" is logged to the console.

### Encountering the First await
Step 5: The code reaches ```let response = await fetch('https://jsonplaceholder.typicode.com/todos/1');```.
- What Happens Here?
  - The fetch function is called, which initiates a network request and returns a promise.
  - Since await is used, the function pauses here and waits for the promise from fetch to resolve.

### Pausing the Function (Suspension)
Step 6: The fetchData function is suspended at the await line. It is removed from the call stack, and JavaScript continues executing the remaining code outside of fetchData.

### Continuing with the Synchronous Code
Step 7: console.log('B: After calling fetchData'); is executed, and "B: After calling fetchData" is logged to the console.

### Network Request Completes (Promise Resolution)
Step 8: Meanwhile, the fetch request completes, and the promise returned by fetch is resolved with the response object.
- Microtasks Queue: The resolved promise triggers a microtask. The event loop adds this microtask to the microtasks queue.
- So basically, when the promise gets resolved, a callback function called microtask is pushed to the microtask queue. This callback function contains the code to resume the execution of the fetchData() function from where it was paused.

### Resuming the async Function
Step 9: The event loop checks the call stack and finds it empty. It then processes the microtasks queue.
- Resuming fetchData: The fetchData function resumes from where it was paused. The response object is now available.
- Step 10: ```console.log('2: Response received');``` is executed, and "2: Response received" is logged to the console.

### Encountering the Second await
Step 11: The code now reaches ```let data = await response.json();```.
- What Happens Here?
  - response.json() is called, which returns a promise that resolves when the JSON data is fully parsed.
  - The function is paused again at this await, and fetchData is removed from the call stack.

### JSON Parsing Completes
Step 12: The JSON parsing completes, and the promise returned by response.json() resolves with the parsed data.
- Microtasks Queue: The resolution of this promise triggers another microtask. The event loop adds it to the microtasks queue.


### Final Resumption of the async Function
Step 13: The event loop processes the microtasks queue again.
- Resuming fetchData: The fetchData function resumes from where it was paused. The data object is now available.
- Step 14: console.log('3: Data processed'); is executed, and "3: Data processed" is logged to the console.

### Returning from the async Function
Step 15: The fetchData function reaches its end, and the return data; statement is executed.
- What Happens Here?
  - The data object is returned, but since fetchData is an async function, it is automatically wrapped in a resolved promise.

### Handling the Final Result
- Step 16: The promise returned by fetchData() is now resolved with the data.
  - The ```.then(result => { console.log('4: Final result', result); })``` attached to fetchData() is now triggered.
  - Step 17: The callback function inside .then() is pushed onto the call stack and executed.
  - Step 18: console.log('4: Final result', result); is executed, and "4: Final result [data]" is logged to the console.

### Final Output Order
```
A: Before calling fetchData
1: Start fetching data
B: After calling fetchData
2: Response received
3: Data processed
4: Final result { ...data... }
```

## Important Point
In our example, we had 2 await statements. Let's suppose the first one took 5 secs to complete, and the second one takes 3 secs to complete. So the total time will be 5 + 3 = 8 secs.

# Exception/Error Handling

```
async function fetchData() {
  try {
    let response = await fetch('https://jsonplaceholder.typicode.com/todos/1');
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    let data = await response.json();
    return data;
  } catch (error) {
    console.error('Error fetching data:', error);
    // Handle error (e.g., return a default value or rethrow the error)
    return null;
  }
}
```

- To handle errors in async functions, we use try...catch block.
- When using await, any error thrown by the promise will be propagated to the nearest catch block. This allows you to handle errors as they occur.
- If an error is not handled within the async function, it will propagate to the caller of the function. You can handle such errors using .catch() when calling the async function or by using try...catch in the calling context.

```
async function fetchData() {
  let response = await fetch('https://jsonplaceholder.typicode.com/invalid-endpoint');
  let data = await response.json();
  return data;
}

fetchData().then(data => {
  console.log('Data:', data);
}).catch(error => {
  console.error('Error in fetchData:', error);
});
```

## When does an error occur?

#### 1. Network or API failures
When making network requests (e.g., using fetch), errors can occur due to network issues, invalid URLs, or server-side problems.

#### 2. Promise Rejection
If the promise returned by an await expression is rejected, it will throw an error.

#### 3. Invalid Data Handling
Errors can also occur when processing or parsing data. For instance, if you attempt to parse a non-JSON response using response.json().

#### 4. Unhandled Promise Rejections
If an async function returns a promise that gets rejected and the rejection is not handled properly, it can lead to unhandled promise rejections.
```
async function fetchData() {
  let response = await fetch('https://jsonplaceholder.typicode.com/invalid-endpoint');
  let data = await response.json();
  return data;
}

fetchData(); // No error handling here
```
In this code:

1. Requesting Data: fetchData makes a request to an invalid endpoint.
2. Error Occurs: Since the endpoint is invalid, the fetch request will fail, and the promise returned by fetch will be rejected.
3. No Error Handling: The fetchData function does not have a .catch() method or a try...catch block to handle the rejection.


# Parallel execution using Promise.all()

```
async function fetchData() {
  try {
    // Perform multiple fetch requests in parallel
    let [response1, response2] = await Promise.all([
      fetch('https://jsonplaceholder.typicode.com/todos/1'),
      fetch('https://jsonplaceholder.typicode.com/todos/2')
    ]);

    // Wait for both responses to be converted to JSON
    let [data1, data2] = await Promise.all([
      response1.json(),
      response2.json()
    ]);

    // Return the combined results
    return [data1, data2];
  } catch (error) {
    console.error('Error fetching data:', error);
    // Handle the error (e.g., return a default value or rethrow the error)
    return [];
  }
}

fetchData().then(data => console.log(data));
```

In this case, all tasks run in parallel, and the total execution time will be determined by the longest task, not the sum of all tasks. 

