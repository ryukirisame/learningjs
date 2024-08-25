
# 'new' Keyword

The new operator lets developers create an instance of a user-defined object type or of one of the built-in object types that has a constructor function.

- A function can know whether it is invoked with new by checking ```new.target```
- When you call a function without the new keyword, JavaScript treats it as a normal function call.
- When you call a function with the new keyword, JavaScript treats it as a constructor function call. 

When a function is called with the new keyword, the function will be used as a constructor. new will do the following things:

1. Creates a blank, plain JavaScript object. For convenience, let's call it newInstance.
2. Points newInstance's [[Prototype]] to the constructor function's prototype property, if the prototype is an Object. Otherwise, newInstance stays as a plain object with Object.prototype as its [[Prototype]].
3. Executes the constructor function with the given arguments, binding newInstance as the this context (i.e. all references to this in the constructor function now refer to newInstance).
4. If the constructor function returns a non-primitive, this return value becomes the result of the whole new expression (In this case, the new object is not an instance of Constructor). Otherwise, if the constructor function doesn't return anything or returns a primitive, newInstance is returned instead. (Normally constructors don't return a value, but they can choose to do so to override the normal object creation process.)

# Classes

Classes in JavaScript are a syntactic sugar over the existing prototype-based inheritance. They provide a clearer and more concise syntax to create objects and handle inheritance.

Within a class body, there are a range of features available:
1. Constructor
2. Instance Field
3. Instance Method
4. Static Field
5. Static Method
6. Static Block
7. Private Fields & Methods

   
```
class MyClass {
  // Constructor
  constructor() {
    // Constructor body
  }
  // Instance field
  myField = "foo";
  // Instance method
  myMethod() {
    // myMethod body
  }
  // Static field
  static myStaticField = "bar";
  // Static method
  static myStaticMethod() {
    // myStaticMethod body
  }
  // Static block
  static {
    // Static initialization code
  }
  // Fields, methods, static fields, and static methods all have
  // "private" forms
  #myPrivateField = "bar";
}
```
The pattern above would roughly translate to the following with function constructors:
```
function MyClass() {
  this.myField = "foo";
  // Constructor body
}
MyClass.myStaticField = "bar";
MyClass.myStaticMethod = function () {
  // myStaticMethod body
};
MyClass.prototype.myMethod = function () {
  // myMethod body
};

(function () {
  // Static initialization code
})();
```

**Note**: Private fields and methods are new features in classes with no trivial equivalent in function constructors.


- Typical function constructors can both be constructed with 'new' and called without 'new'. However, attempting to "call" a class without 'new' will result in an error.
- Unlike function declarations, class declarations are not hoisted (or, in some interpretations, hoisted but with the temporal dead zone restriction), which means you cannot use a class before it is declared. This behavior is similar to variables declared with let and const.

```
new MyClass(); // ReferenceError: Cannot access 'MyClass' before initialization

class MyClass {}
```

## Class Expressions

Similar to functions, class declarations also have their expression counterparts.

```
const MyClass = class {
  // Class body...
};
```

Class expressions can have names as well. The expression's name is only visible to the class's body.

```
const MyClass = class MyClassLongerName {
  // Class body. Here MyClass and MyClassLongerName point to the same class.
};
new MyClassLongerName(); // ReferenceError: MyClassLongerName is not defined
```

## constructor

- ```constructor```  method is a special method of a class for creating and initializing an object instance of that class.
- The constructor method is not explicitly called; it's automatically invoked when you use new to create an instance.
- Every class can have one constructor method, and if you don't define one, JavaScript provides a default one.

**There are some additional syntax restrictions:**

- A class method called constructor cannot be a getter, setter, async, or generator.
- A class cannot have more than one constructor method. (Because JS only supports run-time polymorphism, not compile-time polymorphism)
- Within a class constructor, the value of 'this' points to the newly created instance. You can assign properties to it, or read existing properties. The this value will be automatically returned as the result of new. You are advised to not return any value from the constructor — because if you return a non-primitive value, it will become the value of the new expression, and the value of this is dropped. 
```
class MyClass {
  constructor() {
    this.myField = "foo";
    return {};
  }
}

console.log(new MyClass().myField); // undefined

```




An example:
```
class Person {
  // Constructor method
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  // Method
  greet() {
    return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
  }
}

// Creating instances of the Person class
const person1 = new Person('Alice', 30);
const person2 = new Person('Bob', 25);

console.log(person1.greet()); // Outputs: Hello, my name is Alice and I am 30 years old.
console.log(person2.greet()); // Outputs: Hello, my name is Bob and I am 25 years old.
```


