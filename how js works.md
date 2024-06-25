
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











