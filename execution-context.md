
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
- Lexical Environments are created lazily
- Only when execution reaches the block.
- This applies to:
    - if () { ... }
    - for (...) { ... }
    - while { ... }
    - try/catch
    - Standalone { } blocks
- Always at runtime, not at function creation time.



