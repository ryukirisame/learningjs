
# 'new' Keyword

The new operator lets developers create an instance of a user-defined object type or of one of the built-in object types that has a constructor function.

When a function is called with the new keyword, the function will be used as a constructor. new will do the following things:

1. Creates a blank, plain JavaScript object. For convenience, let's call it newInstance.
2. Points newInstance's [[Prototype]] to the constructor function's prototype property, if the prototype is an Object. Otherwise, newInstance stays as a plain object with Object.prototype as its [[Prototype]].
3. Executes the constructor function with the given arguments, binding newInstance as the this context (i.e. all references to this in the constructor function now refer to newInstance).
4. If the constructor function returns a non-primitive, this return value becomes the result of the whole new expression (In this case, the new object is not an instance of Constructor). Otherwise, if the constructor function doesn't return anything or returns a primitive, newInstance is returned instead. (Normally constructors don't return a value, but they can choose to do so to override the normal object creation process.)

- A function can know whether it is invoked with new by checking ```new.target```
- When you call a function without the new keyword, JavaScript treats it as a normal function call.
- When you call a function with the new keyword, JavaScript treats it as a constructor function call. 

