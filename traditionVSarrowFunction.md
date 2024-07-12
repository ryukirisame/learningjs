
# Difference between tradition function and arrow function in JS

## Syntax

**Traditional Function**:
```
function traditionalFunction(a, b) {
  return a + b;
}
```

**Arrow Function**:
```
const arrowFunction = (a, b) => a + b;
```

## 'this' Binding

**Traditional Function**:
Has its own 'this' context, which is determined by how the function is called (runtime binding).
Can use call, apply, or bind to explicitly set the this context.

```
const obj = {
  value: 42,
  traditionalFunction: function() {
    console.log(this.value);
  }
};

obj.traditionalFunction(); // 42

const detachedFunction = obj.traditionalFunction;
detachedFunction(); // undefined (or global object in non-strict mode)
```

**Arrow Function**:
Does not have its own this context; it inherits this from the enclosing lexical scope at the time it is defined (lexical binding).
Cannot use call, apply, or bind to change this.
```
const obj = {
  value: 42,
  arrowFunction: () => {
    console.log(this.value);
  }
};

obj.arrowFunction(); // undefined (or global object in non-strict mode)
```

## Arguments Object

**Traditional Function:**
Has access to the arguments object, which is an array-like object containing all arguments passed to the function.
```
function traditionalFunction() {
  console.log(arguments);
}

traditionalFunction(1, 2, 3); // [1, 2, 3]
```

**Arrow Function:**
Does not have its own arguments object. To access arguments, you need to use rest parameters.

```
const arrowFunction = (...args) => {
  console.log(args);
};

arrowFunction(1, 2, 3); // [1, 2, 3]
```


## Constructor
**Traditional Function:**
Can be used as a constructor function and can be invoked with the new keyword to create instances.
```
function TraditionalFunction(name) {
  this.name = name;
}

const instance = new TraditionalFunction('John');
console.log(instance.name); // John
```

**Arrow Function:**
Cannot be used as a constructor function and will throw an error if used with new.

```
const ArrowFunction = (name) => {
  this.name = name;
};

// const instance = new ArrowFunction('John'); // TypeError: ArrowFunction is not a constructor
```


## Implicit Return

**Traditional Function:**
Requires an explicit return statement to return a value.
```
function traditionalFunction(a, b) {
  return a + b;
}
```
**Arrow Function:**
Can have an implicit return for single-expression functions, where the expression's value is returned automatically.
```
const arrowFunction = (a, b) => a + b;
```

## 'prototype' Property

**Traditional Function**
Have a default 'prototype' property. This 'prototype' object will be set as [[Prototype]] of every instance created if the function is used as constructor.

**Arrow Function**
Doesn't have a default 'prototype' property.
