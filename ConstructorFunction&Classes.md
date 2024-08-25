
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

## Instance Methods

If you define a function inside the constructor, like this:
```
class Color {
  constructor(r, g, b) {
    this.values = [r, g, b];
    this.getRed = function () {
      return this.values[0];
    };
  }
}

```
Here, every time you create a new Color instance, a new getRed function is created. This means that each Color object has its own copy of the getRed function, even though they all do the same thing.
```
console.log(new Color().getRed === new Color().getRed); // false
```

In contrast, if you use a method, it will be shared between all instances.
```
class Color {
  constructor(r, g, b) {
    this.values = [r, g, b];
  }

  getRed() {
    return this.values[0];
  }
}
```
The getRed function is only created once and is shared by all instances of Color. This is because methods are stored on the Color.prototype, not on each individual instance.

- A function can be shared between all instances, but still have its behavior differ when different instances call it, because the value of 'this' is different. 


## Private Fields

- There is a philosophy in object-oriented programming called "encapsulation". This means you should not access the underlying implementation of an object, but instead use well-abstracted methods to interact with it.
- Private properties are created by prefixing the property name with a ```#``` symbol.
- The # symbol is part of the private property's name, so it ensures that a private property will never conflict with a public property, even if they have similar names.
```
class Example {
  #name = 'Private Name';  // Private property
  name = 'Public Name';    // Public property

  getName() {
    return this.#name; // Accessing the private property
  }
}

const instance = new Example();

console.log(instance.name);       // Output: 'Public Name'
console.log(instance.getName());  // Output: 'Private Name'
```
- You need to declare a private field with # in the class body before you can use it in any methods within that class.
```
class Example {
  #privateField; // Declare the private field in the class body

  constructor(value) {
    this.#privateField = value; // Now you can use it in the class
  }

  getPrivateField() {
    return this.#privateField; // Accessing the private field
  }
}

```

- Accessing private fields outside the class is an early syntax error. The language can guard against this because #privateField is a special syntax, so it can do some static analysis and find all usage of private fields before even evaluating the code.
```
console.log(red.#values); // SyntaxError: Private field '#values' must be declared in an enclosing class
```

**Note:** Code run in the Chrome console can access private properties outside the class. This is a DevTools-only relaxation of the JavaScript syntax restriction.

- A class method can read the private fields of other instances, as long as they belong to the same class.
```
class Color {
  #values;
  constructor(r, g, b) {
    this.#values = [r, g, b];
  }
  redDifference(anotherColor) {
    // #values doesn't necessarily need to be accessed from this:
    // you can access private fields of other instances belonging
    // to the same class.
    return this.#values[0] - anotherColor.#values[0];
  }
}

const red = new Color(255, 0, 0);
const crimson = new Color(220, 20, 60);
red.redDifference(crimson); // 35

```

- Accessing a nonexistent private property throws an error instead of returning undefined like normal properties do. If you don't know if a private field exists on an object and you wish to access it without using try/catch to handle the error, you can use the in operator.

```
class Color {
  #values;
  constructor(r, g, b) {
    this.#values = [r, g, b];
  }
  redDifference(anotherColor) {
    if (!(#values in anotherColor)) {
      throw new TypeError("Color instance expected");
    }
    return this.#values[0] - anotherColor.#values[0];
  }
}
```
**Note**: Keep in mind that the # is a special identifier syntax, and you can't use the field name as if it's a string. "#values" in anotherColor would look for a property name literally called "#values", instead of a private field.


## Accessor Fields (Getters & Setters)

- Accessor fields allow us to manipulate something as if it is an "actual property".
```
class Color {
  constructor(r, g, b) {
    this.values = [r, g, b];
  }
  get red() {
    return this.values[0];
  }
  set red(value) {
    this.values[0] = value;
  }
}

const red = new Color(255, 0, 0);
red.red = 0;
console.log(red.red); // 0
```
It looks as if the object has a property called red — but actually, no such property exists on the instance! There are only two methods, but they are prefixed with get and set, which allows them to be manipulated as if they were properties.

- If a field only has a getter but no setter, it will be effectively read-only.

```
class Color {
  constructor(r, g, b) {
    this.values = [r, g, b];
  }
  get red() {
    return this.values[0];
  }
}

const red = new Color(255, 0, 0);
red.red = 0;
console.log(red.red); // 255
```

In strict mode, the red.red = 0 line will throw a type error: "Cannot set property red of #<Color> which has only a getter". In non-strict mode, the assignment is silently ignored.












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


