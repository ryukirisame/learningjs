
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

# apply Method
The apply method is similar to 'call' method, but it takes an array of arguments instead of listing them individually.

### Syntax
```
function.apply(thisArg, [argsArray])
```

thisArg: The value to use as this when calling the function. <br>
argsArray: An array or array-like object containing arguments to pass to the function.







