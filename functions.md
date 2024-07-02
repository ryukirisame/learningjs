# Function Declaration/Statement

In JavaScript, a function statement (also known as a function declaration) defines a named function. The syntax for a function statement is as follows:
```
function functionName(parameters) {
  // function body
}
```

# Function Expressions

In JavaScript, a function expression is a way to define a function inside an expression rather than as a separate statement. Function expressions can be named or anonymous, and they are often used for more flexible and concise function definitions.

## Syntax of Function Expressions

**Anonymous Function Expression**:

```
const myFunction = function(a, b) {
  return a + b;
};
```

**Named Function Expression:**

```
const myFunction = function add(a, b) {
  return a + b;
};
```

- In this example, add is a named function expression. The function name add is only available within the scope of the function itself, not outside of it. Hence, add is not accessible in the surrounding scope, which is why calling add(2, 3) outside of the function expression throws a ReferenceError.

**Why Use Named Function Expressions?**

_Debugging_: When debugging, the function name add will appear in stack traces, making it easier to identify the function.

_Recursion_: The name add can be used for recursive calls within the function body.


## Differences Between Function Expressions and Function Declarations

**Hoisting:**

Function Declarations are hoisted, meaning the function can be called before its declaration in the code.
Function Expressions are not hoisted in the same way. The variable holding the function expression is hoisted but not initialized until the assignment is reached in the code.


```
// Function Declaration
console.log(declaredFunction()); // Works, because the function is hoisted

function declaredFunction() {
  return 'I am declared!';
}

// Function Expression
console.log(expressionFunction()); // Error: expressionFunction is not a function

var expressionFunction = function() {
  return 'I am expressed!';
};
```

**Naming:**

Function declarations have a name.
Function expressions can be anonymous or named.

**Usage Context:**

Function declarations are useful when you need to ensure the function is available throughout the scope.
Function expressions are useful for defining functions within other expressions, such as in callbacks or immediately invoked function expressions (IIFEs).


### Immediately Invoked Function Expressions (IIFE)

IIFEs are functions that are defined and immediately executed. They are useful for creating a new scope and avoiding polluting the global namespace.

```
(function() {
  console.log('This is an IIFE');
})();
```

# First Class Functions

In JavaScript, functions are considered first-class citizens, meaning they are treated like any other variable. This allows functions to be assigned to variables, passed as arguments to other functions, returned from functions, and stored in data structures.

## Higher Order Functions
In JavaScript, a higher-order function is a function that either takes one or more functions as arguments, returns a function, or both.

## Our own implementation of map function

```
function myMap(array, callback) {
  const resultArray = [];
  for (let i = 0; i < array.length; i++) {
    resultArray.push(callback(array[i], i, array));
  }
  return resultArray;
}

const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = myMap(numbers, function(num) {
  return num * 2;
});

console.log(doubledNumbers); // [2, 4, 6, 8, 10]
```


# Callback Functions

A callback function is simply a function that is passed to another function as a parameter and then invoked (called back) at a certain point within the receiving function.

- Callbacks are often used for handling asynchronous operations, such as reading files, making network requests, or setting timers.


**Simulating Asynchronous operation**

```
function fetchData(callback) {
  // Simulate an asynchronous operation using setTimeout
  setTimeout(() => {
    const data = { name: 'Alice', age: 25 };
    callback(null, data);
  }, 2000);
}

fetchData(function(error, data) {
  if (error) {
    console.error('Error:', error);
  } else {
    console.log('Data received:', data);
  }
});
```

## Write a js program that counts the number of times a button is clicked without using any global variable.

To count the number of times a button is clicked without using any global variables, you can use closures to encapsulate the click count.

```
<!DOCTYPE html>
<html>
<head>
    <title>Button Click Counter</title>
</head>
<body>
    <button id="clickMe">Click me</button>
    <p id="count">Count: 0</p>

    <script>
        // Immediately Invoked Function Expression (IIFE) to create a local scope
        (function() {
            // Get the button and count elements
            const button = document.getElementById('clickMe');
            const countDisplay = document.getElementById('count');

            // Initialize the count within the closure
            let count = 0;

            // Add an event listener to the button
            button.addEventListener('click', function() {
                // Increment the count
                count++;
                // Update the count display
                countDisplay.textContent = 'Count: ' + count;
            });
        })();
    </script>
</body>
</html>
```



