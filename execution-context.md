
## What happens when you redeclare var multiple times?
```js
function test() {
    var x = 10;
    var x = 20;
    var x;
    x = 30;
}

```

#### Result:

- All var x refer to one and the same memory cell
- Redeclarations are ignored, except assignments overwrite the value
- So the final value is 30

#### Why does var behave this way?
Because all var declarations in the entire function are:


1. Hoisted
2. Stored in the same Variable Environment record
3. Using function scope, not block scope**



## Nested functions and var
```js
function outer() {
    var x = 1;

    function inner() {
        var x = 2;
        console.log(x);
    }

    inner();
    console.log(x);
}
```
#### How it works:

- `outer()` has `x` (in its Variable Environment)
- `inner()` has its own `x` (in its Variable Environment)

They do not overwrite each other.

## Inside a function, there is only one Variable Environment — and it belongs to the entire function, not to any blocks.


## So where does each type of declaration go in global context?

### `var` declarations → Global Variable Environment

```js
var x = 10;
console.log(window.x); // 10  (in browsers)
```

global `var` becomes:

- A property of `window` (browser)
- A property of `global` (Node)
- A property of `globalThis` (both)

### let and const → Global Lexical Environment (Declarative Environment Record)
`let` and `const` do not become properties of the global object.


## When is lexical environment of blocks created? 
The inner lexical environment is created ONLY when execution actually enters the block, not during the creation phase of the function execution context.

```js
function test() {
  console.log("start");

  {
    let x = 10;
  }

  console.log("end");
}
```
- The lexical environment of the block containing variable `x` is created during the execution phase of the function and only when the execution reaches the block.

### So basically,
- Lexical Environments are created lazily.
- Only when execution reaches the block.
- This applies to:
    - if () { ... }
    - for (...) { ... }
    - while { ... }
    - try/catch
    - Standalone { } blocks
- Always at runtime, not at function creation time.
- Once the block lexical environment gets created then only the execution of the block continues.
- and destroyed when execution leaves the block.
- All var go to Variable Environment(which is function scoped), so even if the block ends, the var variable is accessible.

# Environment Record
## What is an Environment Record?
- An Environment Record is the actual storage mechanism inside a Lexical/Variable Environment. It's where JavaScript keeps track of all the identifiers (variable names, function names) and their values.
- Simple Analogy: If the Lexical Environment is a "room", then the Environment Record is the "filing cabinet" inside that room where all documents (variables) are stored.

## Types of environment record
1. Declarative Environment Record (DER)
2. Object Environment Record (OER)
3. Function Environment Record (FER)
4. Global Environment Record (GER)
5. Module Environment Record (MER)


# Declarative Environment Record (DER)
This is the most common, most fundamental ER.


Used for:

- `let` and `const`
- block scopes `{ }`
- function ke andar block scopes (for `let/const`)
- catch clauses (`catch(e)`)
- `class` declarations
- parameters (inside functions)
- `var` inside functions?
    - YES, because function Variable Environment uses DER too.

- DER is used whenever a variable/identifier does NOT map onto an object property.
- It holds bindings in an internal spec-defined structure — NOT on an object.

## Example of DER inside a block

```js
// Block scope creates Declarative Environment Record
{
    let blockVar = 'I am block scoped';
    const blockConst = 42;
    
    console.log('Inside block:');
    console.log('  blockVar:', blockVar);
    console.log('  blockConst:', blockConst);
}

console.log('Outside block:');
console.log('  blockVar exists?', typeof blockVar);
console.log('  blockConst exists?', typeof blockConst);
```
Output:
```js
Inside block:
  blockVar: I am block scoped
  blockConst: 42

Outside block:
  blockVar exists? undefined
  blockConst exists? undefined
```
```
Declarative Environment Record Structure

Block Scope's Lexical Environment:
├─ Environment Record: Declarative
│  ├─ blockVar: "I am block scoped"
│  └─ blockConst: 42
│
└─ Outer Reference: → Parent Scope

Key Point: These variables are NOT accessible outside the block
because the Declarative Record is destroyed when block exits.
```

## Example of DER inside a function
Let's suppose we have a function
```js
function test(a, b) {
    let c = 10;
    const d = 20;
}
```
This function's lexical environment would look like this:
```
Function Lexical Environment (Declarative ER):
    c: 10
    d: 20
    function declarations
    parameters -> handled by Function ER (we'll see later)

```
We will come back to this example when we reach Function Environment Record, which extends the DER.

## Environment Record of Variable Environment inside a function execution context 

```js
function x() {
    var p = 1;
}
```
The function execution context's variable environment is of type Declarative ER. 
```
Function Variable Environment (Declarative ER):
    p: 1
```

### NOTE: Declarative Environment Record doesn't support TDZ. 

# Function Environment Record (FER)

A Function Environment Record is an Environment Record specifically created for a function execution context (its lexical environment).

It contains:
1. Parameters
2. Function name binding (for named function expressions)
3. `arguments` object
4. Lexical scoping for closures
5. `this` binding resolution

### WHEN is a Function Environment Record created?

Whenever a function call begins, before running its body:
```js
let foo = function example(a, b) {
    let x = 10;
    var y = 20;
    console.log(foo.name); // example
}
foo(5, 6);
```
#### The engine:

1. Creates a new Function Execution Context (FEC)
2. Inside that, creates a Function Environment Record (FER)
3. Inside the FER, it allocates function specific bindings:
    - parameter bindings → `a = 5`, `b = 6`
    - function name → `example` (only in case of named function expression)
    - `arguments` object
    - `super` (if class/derived)
    - `this` binding

4. Then, the function’s LE and VE are created on top of that.

```
Function Environment Record (FER)
|
|-- Parameter Bindings
|       a: 5
|       b: 6
|
|-- Function name binding
|       example: <function>   (ONLY for named function expressions/declarations)
|
|-- arguments object
|       arguments: {0:5, 1:6, length:2}
|
|-- ThisBinding
|       this: <value>
|
|-- [[OuterEnv]]
|       → parent lexical environment

```

### Remember earlier we said:

- Function LE uses declarative ER
- Function VE uses declarative ER

That's still true — the Lexical Environment for the function uses a Function Environment Record, which extends Declarative ER with function-specific bindings.
So basically, `FER = DER + function specific bindings`

## Example - Parameters in FER 
```js
function foo(a, b) {
    console.log(a, b);
}
foo(10, 20);
```

```
FER:
   a: 10
   b: 20
   arguments: {0:10, 1:20, length:2}
   this: <value>
   outer → global LE
```

## EXAMPLE — Function name binding (named functions)
```js
let x = function bar() {
    console.log(bar); // bar exists here
};
console.log(bar); // ReferenceError
```
Inside the function body, FER contains:
```
FER:
   bar: <function>   // function name binding
```
But outside, `bar` does not exist.

## EXAMPLE — Closures (stores outer environment)

```js
function outer() {
    let x = 10;

    return function inner() {
        console.log(x); // closure
    };
}
const fn = outer();
fn();
```
FER for inner() contains:
```
[[OuterEnv]] → outer()'s Lexical Environment (DER)
```
This is how closures work.

## EXAMPLE — Arguments object differences

FER creates two types of arguments:

1. Mapped arguments object (non-strict mode)
    - `arguments[i]` mirrors parameter variables

2. Unmapped arguments object (strict mode)
    - No linkage between parameters and `arguments`

```js
function test(a) {
    a = 99;
    console.log(arguments[0]); // 99 (non-strict)
}
```
Strict Mode:
```js
"use strict";
function test(a) {
    a = 99;
    console.log(arguments[0]); // still original argument
}
```

## Summary
When we call a function, a Function Execution Context (FEC) is created. It contains:
1. Lexical Environment (LE)
2. Variable Environment (VE)
3. This Binding


Both LE and VE contain:
1. Environment Record
2. Outer (Reference to parent Lexical Environment)

### Function's LE
The function's Lexical Environment uses a Function Environment Record, which is basically an extension of DER. So basically,
```
FunctionEnvironmentRecord = DER + parameters + arguments + function name + super + this binding logic
```
The FER simply adds extra fields on top of DER.

### Function's VE
The function's variable environment uses the normal declarative environment record as its environment record.


### Final Model
```
FunctionExecutionContext:

   LexicalEnvironment:
        EnvironmentRecord → FunctionEnvironmentRecord (FER)
        Outer → parent LE

   VariableEnvironment:
        EnvironmentRecord → DeclarativeEnvironmentRecord (DER)
        Outer → parent LE

   ThisBinding:
        <value>
```

## Arrow Functions
Arrow functions are special because they break the usual rules of execution contexts and environment records. 
They use Declarative Environment Record for their lexical environment. It simply reuses the outer Lexical Environment’s bindings. So, eventually:
1. It does not have its own `this` binding.
2. It does not have its own `arguments` object.
3. It does not have its own `super`
4. The function name is inherited from outer scope.
5. As for function parameters, normally they go into FER, but in this case, they are put into DER (because obviously, arrow functions still need parameters, so they were put into DER of arrow function)
6. So basically, they have made the EV of arrow function "lighter" than normal function.


#### NOTE: The function name binding is resolved from the outer scope. 
```js
const f = () => console.log(f);
f();
```
Inside the arrow function, `f` works only because it resolves from the outer scope:
- It is not an internal function name binding
- It comes from the outer lexical environment (the let-bound variable)

```
ArrowFunctionExecutionContext
|
|-- LexicalEnvironment:
|       ER = DeclarativeEnvironmentRecord
|       Outer = parent's LE
|
|-- VariableEnvironment:
|       ER = DeclarativeEnvironmentRecord (var inside arrow)
|
|-- ThisBinding = taken from OUTER EC (not created here)
|
|-- No arguments object created
```


### Comparison
Normal Function
```
Function LE:
   EnvironmentRecord = FunctionEnvironmentRecord
       a: <value>
       b: <value>
       arguments: { ... }
       this: <new this>
```
Arrow Function
```
Arrow Function LE:
   EnvironmentRecord = DeclarativeEnvironmentRecord
       a: <value>
       b: <value>
   (NO arguments)
   (NO this)
```


# Object Environment Record (OER)

This is the environment record type that interacts with JavaScript objects, especially the global object. All bindings(entries) are stored directly as properties on an object.

## Where is the OER used?
1. Global scope (for var and global function declarations)
2. With statements (with(someObject) { ... })


## 1. Global OER
This is the most important usage.

When you write:
```js
var x = 10;
function foo() {}
```
At the global level only, var x and foo are stored in the Object Environment Record, backed by the global object (window, global, globalThis).

So the OER contains:
```js
Object ER:
   x: 10
   foo: function
(These are actual properties of the global object)
```

This is exactly why:
```js
console.log(window.x);  // 10
console.log(window.foo); // function foo() {}
```

#### Why does global var go here instead of DER?
- Because historically JavaScript's global variables were just properties on the global object.
- ECMAScript maintained this behavior for compatibility.

## Properties of the OER
| Feature                     | Value                                              |
| --------------------------- | -------------------------------------------------- |
| Backing store               | An actual JavaScript object                        |
| Default candidate           | The global object                                  |
| Used by                     | global var, global function declarations, `with`   |
| Allows property-like lookup | Yes                                                |
| Allows deletion             | global var cannot be deleted, but with objects yes |
| No TDZ                      | Correct — OER has **no TDZ**                       |

## OER in the Global Execution Context

```js
Global Lexical Environment (Global Env Record)
|
|-- Declarative ER (global let/const)
|
|-- Object ER (global var / function declarations)
       (Backed by global object)
```
```js
Global Variable Environment → References the same Object ER of Global Lexical Env.
```
Thus:
- Global `var` lives in OER
- OER is part of the Global Lexical Environment
- So variable lookup finds `var` via Lexical Environment chain






## IMPORTANT DIFFERENCES FROM DECLARATIVE ER

| Feature                           | Declarative ER            | Object ER                    |
| --------------------------------- | ------------------------- | ---------------------------- |
| Stores variables in               | internal record           | actual JavaScript object     |
| Has TDZ                           | YES                       | NO                           |
| Used for                          | let/const/var-in-function | global var, with-object      |
| Allows shadowing local variables? | Yes                       | Not in global OER            |
| Find operation                    | identifier → binding      | identifier → property lookup |

















