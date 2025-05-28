
# Debouncing

Debouncing is a technique where a function call is delayed until after a specified amount of time has elapsed since the last time the function was invoked. It's typically used to ensure that a function is not called too frequently, especially in situations like:

- Handling user input events (e.g., keypresses, mouse moves).
- Limiting the frequency of API calls based on user actions.
- Preventing performance issues due to excessive function calls.

## Implementation of Debouncing

Here's a basic implementation of a debouncing function in JavaScript:

```js
function debounce(func, delay) {
    let timerId;
    
    return function() {
        const context = this;
        const args = arguments;
        
        clearTimeout(timerId);
        timerId = setTimeout(() => {
            func.apply(context, args);
        }, delay);
    };
}
```

1. debounce Function: It takes two parameters:
  - func: The function to be debounced.
  - delay: The time interval in milliseconds to wait before invoking func.

2. Returned Function: This function is returned by debounce:
  - It clears any existing timeout (clearTimeout(timerId)).
  - Sets a new timeout (setTimeout) that will invoke func after delay milliseconds.
  - Uses apply to preserve the context (this) and pass any arguments (args) to func.

Let's say you have a function saveData that you want to debounce to improve performance:

```js
function saveData() {
    // Code to save data to the server
    console.log('Data saved');
}

const debouncedSave = debounce(saveData, 1000); // Debounce saveData function with a delay of 1000ms

// Example usage - simulate calling saveData multiple times
debouncedSave(); // This call will be delayed by 1000ms
debouncedSave(); // This call will reset the timer, delaying again
debouncedSave(); // This call will reset the timer again

// After 1000ms of no calls, saveData will finally be invoked
```

### Using Debouncing for Rate Limiting
When applied to rate limiting, debouncing helps in scenarios where you want to prevent a function from executing too frequently within a short time span. For example, consider a scenario where you have a search input field and you want to trigger an API call to fetch search results. If the user is typing rapidly, you might want to wait until they pause typing before making the API call to avoid overwhelming the server with requests.


### Use Case: Search Input Field
Consider a search input field that fetches suggestions from a server as the user types. Without debouncing, every keystroke would send a request, potentially leading to hundreds of requests per minute. Debouncing allows us to delay the function call until the user has stopped typing for a predefined time.

# Throttling

Throttling is a technique used to limit the rate at which a function is called. Throttling transforms a function such that it can only be called once in a specific interval of time.

Throttling limits the execution of a function to once per specified time interval. If the function is called multiple times within that interval, only the first call is executed immediately. Subsequent calls are ignored until the interval has elapsed, at which point the function can be called again. This ensures that the function is executed at a controlled rate, preventing it from being invoked more frequently than necessary.

One implementation of throttling can be:

```js
function throttle(fn, delay) {
  let lastExecutedTime = 0;

  return function () {
    const context = this;
    const args = arguments;
    const currentTime = Date.now();

    if (currentTime - lastExecutedTime >= delay) {
      // execute the function
      fn.apply(context, args);
      lastExecutedTime = currentTime;
    } 
    else {
      // block the execution of function or reschedule it for later
      console.log("blocked");
    }
  };
}
```

### Implementing throttling using setTimeout
```js
function callAPI(a, b) {
  console.log(a, b);

  console.log("Calling api...");
}

function throttle(fn, delay) {
  let flag = true;

  return function () {
    const context = this;
    const args = arguments;
    if (flag) {
      fn.apply(context, args);
      flag = false;
      setTimeout(() => {
        flag = true;
      }, delay);
    } else {
      console.log("blocked");
    }
  };
}

const throttledCallApi = throttle(callAPI, 1000);
```

- The implementation depends on the particular use case. This is a simple example where we are completely blocking the execution of function call within a specific time period.


### Use Case: Scroll Event Listener
An example use case is attaching a listener to the scroll event of a webpage. Since the scroll event can fire dozens of times per second, throttling can be used to limit the number of times your callback function executes, improving performance.

# Debouncing vs Throttling
Debouncing postpones/delays the execution until after a period of inactivity, while throttling limits the execution to a fixed number of times over an interval.









