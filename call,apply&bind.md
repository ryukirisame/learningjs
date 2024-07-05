
# call, apply & bind method in JS

In JavaScript, call, apply, and bind are methods available on functions that allow you to set the this context and optionally pass arguments to the function. These methods are particularly useful for controlling how a function is invoked and what its this value is.

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









