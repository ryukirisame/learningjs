
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




