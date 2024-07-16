
# call, apply & bind method in JS

Because functions are objects, they inherit from Function.prototype, which means they have access to methods like call, apply, and bind.

In JavaScript, call, apply, and bind are methods available on functions that allow you to set the 'this' context and optionally pass arguments to the function. These methods are particularly useful for controlling how a function is invoked and what its this value is.

# 'call' Method
The call method allows you to invoke a function with a specified this value and arguments provided individually.

### Syntax
```
function.call(thisArg, arg1, arg2, ...)
```
thisArg: The value to use as this when calling the function. <br>
arg1, arg2, ...: Arguments to pass to the function.


### Example

```
function greet(greeting, punctuation) {
  console.log(greeting + ', ' + this.name + punctuation);
}

const person = { name: 'Alice' };

greet.call(person, 'Hello', '!'); // Output: Hello, Alice!
```

In this example:

'this' inside greet refers to person. <br>
The arguments 'Hello' and '!' are passed individually.


**Using call for Method Borrowing**
```
const obj1 = {
  name: 'Alice',
  greet: function() {
    console.log('Hello, ' + this.name);
  }
};

const obj2 = { name: 'Bob' };

obj1.greet.call(obj2); // Output: Hello, Bob
```


# apply Method
The apply method is similar to 'call' method, but it takes an array of arguments instead of listing them individually.

### Syntax
```
function.apply(thisArg, [argsArray])
```

thisArg: The value to use as this when calling the function. <br>
argsArray: An array or array-like object containing arguments to pass to the function.


### Example
```
function greet(greeting, punctuation) {
  console.log(greeting + ', ' + this.name + punctuation);
}

const person = { name: 'Alice' };

greet.apply(person, ['Hello', '!']); // Output: Hello, Alice!
```

In this example:

'this' inside greet refers to person. <br>
The arguments 'Hello' and '!' are passed as an array.


Use apply() when the number of arguments is not known beforehand or when the arguments are already in an array-like structure (e.g., arguments object or an array).

# 'bind' Method
The bind method creates a new function with a fixed 'this' value and some arguments already set.

### Syntax
```
const boundFunction = function.bind(thisArg, arg1, arg2, ...)
```

thisArg: The value to use as this when calling the new function. <br>
arg1, arg2, ...: Arguments to pre-fill for the new function.

### Example
```
function greet(greeting, punctuation) {
  console.log(greeting + ', ' + this.name + punctuation);
}

const person = { name: 'Alice' };

const boundGreet = greet.bind(person, 'Hello');
boundGreet('!'); // Output: Hello, Alice!
```

In this example:

'this' inside greet refers to person. <br>
The greeting argument is pre-filled with 'Hello', and the remaining arguments can be provided when boundGreet is called.


**Using bind for Partial Application**
```
function multiply(a, b) {
  return a * b;
}

const double = multiply.bind(null, 2);
console.log(double(5)); // Output: 10
```

# Differences Between call, apply, and bind
### Invocation:
- 'call' and 'apply' invoke the function immediately.
- 'bind' returns a new function that can be called later.

### Arguments:
- 'call' takes arguments individually.
- 'apply' takes arguments as an array.
- 'bind' pre-fills arguments, allowing partial application.


# Partial Application and Pre-Fill in JavaScript
Partial application is a technique in functional programming where a function is applied to some of its arguments, producing a new function that expects the remaining arguments. This concept can be implemented in JavaScript using the bind method.

### Pre-Fill in Context of bind
When we talk about "pre-fill," we mean providing some of the arguments to a function in advance, so that when the resulting function is called later, it has some arguments already fixed (or pre-filled).

### Example of Partial Application

```
function multiply(a, b, c) {
  return a * b * c;
}

// Create a new function where `a` is pre-filled with 2 and `b` with 3
const multiplyBySix = multiply.bind(null, 2, 3);

console.log(multiplyBySix(4)); // Output: 24
```

## Creating a Generic Partial Application Function
You can create a generic function for partial application:

```
function partial(fn, ...preFilledArgs) {
  return function(...laterArgs) {
    return fn(...preFilledArgs, ...laterArgs);
  };
}

const add = (a, b, c) => a + b + c;
const addPartially = partial(add, 1, 2);

console.log(addPartially(3)); // Output: 6
```

# Currying

Currying is the process of breaking down a function that takes multiple arguments into a series of unary (single-argument) functions. Instead of taking all arguments at once, a curried function takes the first argument, and returns a new function that takes the second argument, and so on, until all arguments have been provided and the original function can be executed.

That is, when we turn a function call sum(1,2,3) into sum(1)(2)(3). 

NOTE: The number of arguments a function takes is also called arity.

### Why currying?
- Currying helps you avoid passing the same variable again and again.
- It helps to create a higher order function.

Example:

```
function sum(a, b, c) {
    return a + b + c;
}
sum(1,2,3); // 6
```

Let’s create a curried version of the function and see how we would call the same function (and get the same result) in a series of calls:
```
function sum(a) {
    return (b) => {
        return (c) => {
            return a + b + c
        }
    }
}
console.log(sum(1)(2)(3)) // 6
```

### Currying with Arrow Functions
Using arrow functions, currying can be more concise:
```
const curriedAdd = a => b => a + b;

console.log(curriedAdd(2)(3)); // Output: 5
```

### Currying Functions with More Arguments
For functions with more arguments, currying involves nesting more functions:

```
const curriedMultiply = a => b => c => a * b * c;

console.log(curriedMultiply(2)(3)(4)); // Output: 24

const multiplyByTwo = curriedMultiply(2);
const multiplyByTwoAndThree = multiplyByTwo(3);

console.log(multiplyByTwoAndThree(4)); // Output: 24
```

# Currying vs. Partial Application in JavaScript

Some might start to think that the number of nested functions a curried function has depends on the number of arguments it receives. Yes, that makes it a curry.

Let’s take same sum example:
```
function sum(a) {
    return (b, c) => {
        return a * b * c
    }
}
```
It can be called like this:

```
let x = sum(10);
x(3,12);
x(20,12);
x(20,13);
// OR
sum(10)(3,12);
sum(10)(20,12);
sum(10)(20,13);
```
The above function expects three arguments and has two nested functions. This version isn’t a curry. We just did a partial application of the sum function.

Currying and partial application are related because of closure, but they are different concepts.

Partial application transforms a function into another function with smaller arity.

```
function sum1(x, y, z) {
    return sum2(x,y,z)
}
// to
function sum1(x) {
    return (y,z) => {
        return sum2(x,y,z)
    }
}
```
For currying, it would look like this:

```
function sum1(x) {
    return (y) = > {
        return (z) = > {
            return sum2(x,y,z)
        }
    }
}
```
Currying creates nesting functions according to the number of the arguments of the function. Each function receives an argument. If there is no argument, there is no currying.


# sum(1)(2)(3)(4)..( n)() Problem

we can utilize the concept of closures and recursive function calls.

```
function sum(a) {
    function innerSum(b) {
        if (b === undefined) {
            return a;
        }
        return sum(a + b);
    }
}

console.log(sum(1)(2)(3)(4)()); // Output: 10
console.log(sum(5)(10)(15)());  // Output: 30
console.log(sum(1)(2)(3)());    // Output: 6
```

- Initial Call: When sum(a) is called, it initializes a with the first argument.
- Inner Function: The innerSum(b) function is defined inside sum. This function takes the next argument b and:
    - If b is undefined, it means the chain has ended, so it returns the accumulated sum a.
    - Otherwise, it recursively calls sum(a + b), which creates a new closure with the updated sum and continues the chain.

### Recursive Nature
The key aspect of this implementation is the recursive call return sum(a + b), which creates a new instance of the sum function with the updated accumulated sum. This recursive approach leverages the power of closures to maintain state across multiple invocations and allows the chaining to continue until the terminating condition (no argument) is met.
