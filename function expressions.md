
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

### Named Function Expressions
Named function expressions can be useful for recursion or for better debugging.

