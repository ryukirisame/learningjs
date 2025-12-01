
### What happens when you redeclare var multiple times?
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
