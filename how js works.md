
## Global Object
In JavaScript, the global object is an object that is accessible from anywhere in your JavaScript code.

- In a web browser, the global object is the window object. This means that any global variables or functions you define are properties or methods of the window object.
- In Node.js, the global object is called global.

# Execution Context

The execution context represents the environment in which our code runs.

you can have 3 different types of execution contexts:
-	Global Execution Context – Every code that’s not within a function, is in the global environment. There can only be one global environment, and a global environment also contains a global object (window in the browser) and the value of this in non strict mode is equal to the global environment.
-	Function Execution Context – Every time a function is executed, a new execution context is created for that function. So every function has an execution context of its own which is created when the code is calling the function, and not before.
-	Eval Execution Context – This is created when an eval function is called.

# Execution Stack

The execution stack (also called calling stack in other languages) is a data structure of a Stack, which is used as a collection of all execution contexts which are active while the code runs.

# The Process of Creating an Execution Context

Every time an execution context is created, it happens in two phases:
1.	The Creation Phase (Memory Allocation Phase)
2.	The Execution Phase

During the creation phase the engine goes over the code, and every time it comes across a declaration of a variable or a function, it saves the variables(reserves memory)( without their actual value except function arguments, where the value is saved).

Then in the execution phase actually assigns the variables values and actually executes the code.

### Example Code
Let’s take a look at a quick example to see how this works.
```
function helloWorld (world) {  
  var foo = 'foo'  
  const bar = 'bar'  
  let fooBar = 'fooBar'  
  console.log('Hello, ' + world)  
}  
  
helloWorld('earth')  

```

1.	When this code will run, first of all a global execution context will be created and the engine will save the declaration of the helloWorld function with the argument that’s provided to the world parameter – ‘earth’.
2.	Then, in the execution phase, the engine will execute this function, and a new execution context will be created for that function.
3.	In the creation phase of the helloWorld execution context, the engine will save the variable name of type 'var' with an initial value of undefined (basically reserves memory for the variables).
4.	Let and const will be saved with an initial value of uninitialized.
5.	Once the creation phase has completed, the execution phase starts. This is where the assignment of the variables happen and the code gets executed.
6.	Foo will be assigned to ‘foo’ and executed.
7.	Bar will be assigned to ‘bar’ and executed.
8.	fooBar will be assigned to ‘fooBar’ and executed.
9.	Then the console.log function will be executed and ‘Hello, earth’ will be printed.

Here’s a visual representation that can help us understand how the function execution looks like in the creation phase, and in the execution phase.
First, in the creation phase:

```
FuntionExecutionContext = {  
  foo: undefined,bar: < uninitialized >,  
  fooBar: < uninitialized >,  
  Arguments: {0: 'world', length: 1},  
}  
```

Then, in the execution phase:

```
FuntionExecutionContext = {  
   foo: 'foo',bar: 'bar',  
   fooBar: 'fooBar',  Arguments: {0: 'world', length: 1}
}  
```

# Components of the Execution Context

Technically, an execution context contains the following things:


```
ExecutionContext = {  
  ThisBinding: <this value>,  
  VariableEnvironment: { ... },  
  LexicalEnvironment: { ... }
}

```
All of these things are created during the creation phase, and each serves a different role

# Lexical Environment

A lexical environment is essentially a structure that defines the association between identifiers, to specific variables and functions for a particular scope. a kind of map between variable and function names and their values.
The association between a name of a variable to its value is called binding.
``` let x = 10;  ```
The identifier is x, and it has binding to the value 10.

## Lexical Environment Structure
A lexical environment has 2 parts:
1.	Environment Record
2.	Reference to the our environment

### Environment Record
The precise definition is that an environment record holds the identifier bindings which were created in the scope of the lexical environment. So basically, it holds the function’s local variables, arguments, and inner function declarations.

There are 2 types of Environment Records:
1.	Declarative Environment Record - Its job is to host declarations of variables, functions and arguments that are inside the scope of functions. (before ES5, we had activation object, the declarative environment variable replaces the activation object. The primary motivation to do that was actually performance)
2.	Object Environment Record - Its job is to store declarations of variables and functions that are in the global scope.

Let’s take the following code example:
```
var x = 10;  
function foo(a) {  
var y = 20;  
}  
foo('hello');  
```

Here we have two environments, one is the global one and the other one is a function one (‘foo’). So how would that be represented theoretically behind the scenes?

```
// environment of the global context  
globalEnvironment = {  
environmentRecord: {  
// type  
type: "ObjectEnvironmentRecord",  
// built-ins:  
Object: function,  
Array: function,  
// etc ...  
  
// our bindings:  
x: 10  
foo: <function ref>  
},  
outer: null // no parent environment  
};  
  
// environment of the "foo" function  
fooEnvironment = {  
environmentRecord: {  
// type  
type: "DeclarativeEnvironmentRecord",  
// our bindings:  
y: 20,  
arguments: {0: 'hello', length: 1},  
},  
outer: globalEnvironment  
};  
```

Keep in mind that:
1.	Inside the environment record of the global environment we have all the prototype functions of Object, Array, and other built-in functions.
2.	The environment record of type declarative environment (which is created when calling a function) contains something called an arguments object. The arguments object is an object that contains the values that are passed into the function and their index. It also contains a property length which represents the number of arguments that were passed.

### Reference To Outer Environment

Each lexical environment holds a reference to its outer environment. In the example above we can see that the function foo has a ref to the global function.

The global environment itself has no ref as it has no environment as its parent, it’s the root environment.
When JS looks for a variable, if it’s not found in the current context it goes to the outer environment, and this process repeats itself till the value is found or till it gets to the global object which its reference to our environment equals to null since it has no environment above it.


## Block Lexical Environment
JavaScript ES6 introduced block-scoping, which means variables declared with let and const are block-scoped. A block lexical environment is created whenever you enter a block of code that uses these block-scoped variables. This includes blocks like those in loops, if statements, and so on.

### Execution Context and Call Stack
The execution context includes both the lexical environment and the this binding, and it is pushed to the call stack when a function is called. A new execution context is not pushed to the call stack for every block {} or control structure like if. Instead, a new lexical environment is created within the existing execution context for block-scoped variables.

### Where is the Block Lexical Environment Created?
When a block is encountered during code execution, and it contains let, const, or class declarations, a new block lexical environment is created. This environment exists within the current execution context and contains only the block-scoped variables.




# Closures
In JavaScript, a closure is a powerful feature that allows a function to access variables from an outer function's scope, even after the outer function has returned. Closures are created whenever a function is defined inside another function, giving the inner function access to the outer function's variables.

In JavaScript, the lexical environment of a function is generally destroyed once the function has finished executing, except when there are closures involved. When a function creates a closure, it means that some inner function retains a reference to variables defined in the outer function. This prevents the lexical environment from being garbage-collected, because it’s still in use.

```
function outerFunction() {
    var outerVar = 'I am outer';

    function innerFunction() {
        console.log(outerVar); // Accesses outerVar from outerFunction
    }

    return innerFunction;
}

const inner = outerFunction();
inner(); // Outputs: 'I am outer'
```
In this example:
1.	outerFunction creates a variable outerVar and defines innerFunction, which accesses outerVar.
2.	outerFunction returns innerFunction, creating a closure.
3.	When inner (the returned innerFunction) is called, it still has access to outerVar, even though outerFunction has completed execution.

The lexical environment of outerFunction is preserved because innerFunction maintains a reference to it. This behavior ensures that all variables defined in outerFunction remain accessible to innerFunction.


### Closures and Memory Management
When an inner function (closure) retains a reference to variables in its outer function, it effectively keeps the outer function's lexical environment in memory. This is because the closure forms a link to the lexical environment, ensuring that it is not garbage collected even after the outer function has completed execution. The captured lexical environment is preserved in the heap because the inner function maintains a reference to it.

**Q. Only the lexical environment part of the execution context of the outer function is preserved? or the entire execution context of the outer function is preserved?**
In JavaScript, when a closure is created, only the lexical environment (specifically, the variables and their bindings) of the outer function is preserved, not the entire execution context.

### Without Closures
When no closures are created, the lexical environment of a function is typically destroyed after the function execution is complete.

### Use Case of Closures
https://medium.com/deno-the-complete-reference/10-use-cases-of-closures-in-javascript-98fe0eab36db


<br>

### SetTimeout & Closures

**Problem Statement**: I want to write a code that prints 1,2,3,4,5 with 1 second interval. We are not supposed to use setInterval, but use setTimeout.

Let's try a solution:
```
(function x()
{
    for(var i=1;i<6;i++)
    {    
        setTimeout(()=> console.log(i), i*1000);
    }
})();
```

In this solution, we are setting up 5 setTimeout in a loop. 
However, the output will be:
```
6 
6 
6 
6 
6 
```

This solution didn't work. The issue with our code lies in the scoping of the variable i when using var. Since var is function-scoped, the same i variable is shared across all iterations of the loop. By the time the setTimeout callbacks are executed, the loop has already completed and i is equal to 6 for all the callbacks, resulting in the output 6 being printed five times.

To fix this, you can use let instead of var to take advantage of block scoping. This ensures that each iteration of the loop has its own i variable with the correct value. Here’s the corrected code:
```
function x() {
  for (let i = 1; i < 6; i++) {
    setTimeout(() => console.log(i), i * 1000);
  }
}
x();
```
**Explanation**:
When using let inside the for loop, a new binding of i is created for each iteration, so the setTimeout callbacks will correctly log 1, 2, 3, 4, and 5 at one-second intervals.

**NOTE**: When using let in a for loop, JavaScript creates a new binding for the loop variable i for each iteration of the loop. This is different from using var, which reuses the same variable for each iteration.

**Alternative Solution with Closures** 

Another way to solve this problem is by using closures to capture the value of i:

```
function x() {
  for (var i = 1; i < 6; i++) {
    (function(i) {
      setTimeout(() => console.log(i), i * 1000);
    })(i);
  }
}
x();
```
In this alternative solution:
- An immediately invoked function expression (IIFE) creates a new scope for each iteration.
- The current value of i is passed to the IIFE, which preserves the correct value of i for each setTimeout callback.

# 'this' Binding

- The value of this depends on how a function is called and not necessarily where it is defined.
- "this substitution" refers to the concept of how the 'this' keyword's value is determined or "substituted" in various contexts in JavaScript.
- The value of 'this' is determined by the execution context in which a function is called. Here are the primary rules for determining this binding:
1.	Global Context: When a function is called in the global context(outside any function), this refers to the global object (which is window in browsers and global in Node.js).
```
console.log(this); // In a browser, this logs the `window` object
```
2.	Function Context: When a regular function is called, this refers to the global object in non-strict mode and undefined in strict mode.
```
function myFunction() {
    console.log(this);
}
myFunction(); // In non-strict mode, logs `window`. In strict mode, logs `undefined`.
```
3.	Method Context: When a function is called as a method of an object, this refers to the object that the method is called on.
```
const obj = {
    value: 42,
    myMethod: function() {
        console.log(this.value);
    }
};
obj.myMethod(); // Logs 42
```
4.	Constructor Context: When a function is used as a constructor (with the new keyword), this refers to the newly created object.
```
function MyConstructor() {
    this.value = 42;
}
const instance = new MyConstructor();
console.log(instance.value); // Logs 42
```

5. Event Handlers
In DOM event handlers, this usually refers to the element that received the event.
```
document.querySelector('button').addEventListener('click', function() {
  console.log(this); // Logs the button element
});
```

6. Arrow Functions
Arrow functions do not have their own 'this' binding. Instead, they inherit 'this' from the surrounding lexical context (the scope in which they were defined).
```
const obj = {
    value: 42,
    myMethod: function() {
        const arrowFunction = () => {
            console.log(this); // Logs the `obj` object
        };
        arrowFunction();
    }
};
obj.myMethod();
```

<br>



# Hoisting

JavaScript Hoisting refers to the process whereby the interpreter “appears” to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.
This makes functions and variables accessible before their actual declarations in the code.
NOTE:  The code is not physically moved to the top of the scope.

## Function Declarations vs. Function Expressions
It's important to differentiate between function declarations and function expressions, as they behave differently in terms of hoisting.

### Function Declarations
A function declaration defines a named function and the entire definition is hoisted to the top of its scope.
```
console.log(myFunction()); // "Hello from myFunction!"

function myFunction() {
  return 'Hello from myFunction!';
}
```

### Function Expressions
Function expressions, including those defined using the function keyword and arrow functions, are not hoisted in the same way as function declarations. Only the variable declaration is hoisted, not the function definition.
Example with a function expression:
```
console.log(myFunction); // undefined
console.log(myFunction()); // TypeError: myFunction is not a function

var myFunction = function() {
  return 'Hello from myFunction!';
};
```

### Example with Arrow Functions
Arrow functions, which are also function expressions, behave the same way as regular function expressions in terms of hoisting.
Example with an arrow function:

```
console.log(myArrowFunction); // undefined
console.log(myArrowFunction()); // TypeError: myArrowFunction is not a function

var myArrowFunction = () => 'Hello from myArrowFunction!';
```

### Reason for Hoisting
During the Creation phase(Memory Allocation Phase) of execution context, we know that memory for variables and functions is reserved. And only in the execution phase, the actual code is executed. During the creation phase of the execution context, the memory for variables has been reserved and the identifier binding happens and the variable is initialized with the value undefined (for var) or uninitialized (for let and const). Now, in execution phase, when we try to access those variables even before the declaration then we can do so, as the variable exists in the memory, however, we get the value as undefined or uninitialized (for variables).

In the case of functions, the entire function code is stored for the function name during the creation phase, that’s why it works as intended. 

## var in Block Statements
When you declare a variable using var inside a block statement (like an if statement, loop, or any {} block), it is not confined to that block. Instead, it is hoisted to the top of the nearest function or global scope. This leads to the variable being accessible outside the block where it was defined.

```
if (true) {
  var x = 10;
}
console.log(x); // Outputs: 10
```

## Temporal Dead Zone

The Temporal Dead Zone (TDZ) is a behavior in JavaScript that affects variables declared with let and const. The TDZ refers to the period of time during which these variables exist in the scope but cannot be accessed before they are declared. This period starts from the beginning of the block in which the variable is defined and ends when the variable declaration is encountered and initialized.

### Understanding Temporal Dead Zone
**Declaration and Initialization**: When JavaScript code is parsed, variables declared with let and const are hoisted to the top of their block scope. However, unlike var, they are not initialized with undefined. Instead, they remain uninitialized until the actual declaration statement is executed.

**Accessing in TDZ**: Attempting to access a let or const variable before its declaration results in a ReferenceError. This is because the variable is in the TDZ and cannot be used.

**End of TDZ**: The TDZ ends when the variable is initialized, i.e., when the execution reaches the line where the variable is declared and assigned a value.

```
console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a = 3;
console.log(a); // 3
```
In the example above, the variable a is in the TDZ from the start of the block until the declaration let a = 3; is executed. Accessing a before its declaration results in a ReferenceError.

### Important Points

1. let and const are hoisted but its memory is allocated at other place than window which cannot be accessed before initialisation.
2. Temporal Dead Zone exists until variable is declared and assigned a value.
3. window.variable OR this.variable will not give value of variable defined using let or const.
4. We cannot redeclare the same variable with let/const(even with using var the second time). But in case of var, we can declare the same variable twice.
5. const variable declaration and initialisation must be done on the same line.
6. Use const wherever possible followed by let, Use var as little as possible(only if you have to). It helps avoid error.
7. Initialising variables at the top is good idea, helps shrinks TDZ to zero.
8. Syntax Error ... violation of JS syntax <br>
   Type Error ...  while trying to re-initialize const variable <br>
   Reference Error ... while trying to access variable which is not there in global memory.
9. Syntax error is similar to compile error, while TypeError and Reference Error falls under run time error.

# Implicit Global Variables
When you assign a value to an identifier that has not been declared using var, let, or const, JavaScript treats it as an implicit global variable. This means the variable is automatically added as a property of the global object (window in browsers and global in Node.js).

