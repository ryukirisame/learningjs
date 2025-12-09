I'll create extremely detailed notes on JavaScript Execution Context. However, I cannot directly create or download PDF files, but I'll provide you with the complete detailed notes in a format that you can easily convert to PDF using various methods I'll explain at the end.

Let me create the most comprehensive guide possible:

---

# **JAVASCRIPT EXECUTION CONTEXT: THE ULTIMATE COMPREHENSIVE GUIDE**

## **TABLE OF CONTENTS**

### **PART 1: FOUNDATIONAL CONCEPTS**
1. Introduction to Execution Context
   - 1.1 What is Execution Context?
   - 1.2 Why Does Execution Context Matter?
   - 1.3 The JavaScript Engine Architecture
   - 1.4 Execution Context vs Scope vs Context
   - 1.5 Historical Evolution of Execution Context

2. Types of Execution Contexts
   - 2.1 Global Execution Context (GEC)
   - 2.2 Function Execution Context (FEC)
   - 2.3 Eval Execution Context
   - 2.4 Module Execution Context (ES6+)
   - 2.5 Comparing Different Execution Contexts

3. The Execution Context Stack (Call Stack)
   - 3.1 Understanding the Stack Data Structure
   - 3.2 How Call Stack Works
   - 3.3 Stack Frames
   - 3.4 Stack Overflow Scenarios
   - 3.5 Visualizing the Call Stack
   - 3.6 Call Stack in Different Scenarios

### **PART 2: DEEP DIVE INTO COMPONENTS**

4. Anatomy of Execution Context
   - 4.1 The Three Pillars
   - 4.2 Variable Environment in Detail
   - 4.3 Lexical Environment in Detail
   - 4.4 This Binding Mechanism
   - 4.5 Environment Records
   - 4.6 Outer Environment References

5. Creation Phase (Memory Creation Phase)
   - 5.1 Step-by-Step Process
   - 5.2 Variable Object Creation
   - 5.3 Scope Chain Formation
   - 5.4 This Determination
   - 5.5 Memory Allocation Patterns
   - 5.6 Differences Between var, let, and const

6. Execution Phase (Code Execution Phase)
   - 6.1 Line-by-Line Execution
   - 6.2 Variable Assignment
   - 6.3 Function Invocation
   - 6.4 Expression Evaluation
   - 6.5 Statement Execution Order

### **PART 3: HOISTING MECHANISMS**

7. Complete Guide to Hoisting
   - 7.1 What is Hoisting?
   - 7.2 Variable Hoisting (var)
   - 7.3 Variable Hoisting (let and const)
   - 7.4 Function Declaration Hoisting
   - 7.5 Function Expression Hoisting
   - 7.6 Arrow Function Hoisting
   - 7.7 Class Hoisting
   - 7.8 Import/Export Hoisting
   - 7.9 Hoisting Priority and Precedence
   - 7.10 Common Hoisting Pitfalls

8. Temporal Dead Zone (TDZ)
   - 8.1 Understanding TDZ
   - 8.2 TDZ in Different Scenarios
   - 8.3 Why TDZ Exists
   - 8.4 TDZ with Function Parameters
   - 8.5 TDZ in Loops
   - 8.6 TDZ Best Practices

### **PART 4: SCOPE AND SCOPE CHAIN**

9. Scope in JavaScript
   - 9.1 What is Scope?
   - 9.2 Global Scope
   - 9.3 Function Scope
   - 9.4 Block Scope
   - 9.5 Lexical Scope
   - 9.6 Dynamic Scope (and why JS doesn't have it)
   - 9.7 Module Scope

10. The Scope Chain
    - 10.1 How Scope Chain Works
    - 10.2 Scope Chain Resolution
    - 10.3 Identifier Resolution Process
    - 10.4 Scope Chain with Nested Functions
    - 10.5 Scope Chain and Performance
    - 10.6 Common Scope Chain Mistakes

### **PART 5: THE 'THIS' KEYWORD**

11. Understanding 'this'
    - 11.1 What is 'this'?
    - 11.2 This in Global Context
    - 11.3 This in Function Context
    - 11.4 This in Method Context
    - 11.5 This in Constructor Functions
    - 11.6 This in Arrow Functions
    - 11.7 This in Event Handlers
    - 11.8 This in Strict Mode vs Non-Strict Mode

12. Controlling 'this'
    - 12.1 call() Method
    - 12.2 apply() Method
    - 12.3 bind() Method
    - 12.4 Comparing call, apply, and bind
    - 12.5 When to Use Each Method
    - 12.6 Creating Bound Functions
    - 12.7 Partial Application with bind

### **PART 6: CLOSURES AND EXECUTION CONTEXT**

13. Closures Deep Dive
    - 13.1 What are Closures?
    - 13.2 How Closures are Created
    - 13.3 Closures and Lexical Environment
    - 13.4 Closures and Memory
    - 13.5 Practical Closure Examples
    - 13.6 Closure Scope Chain
    - 13.7 Closures in Loops
    - 13.8 IIFE and Closures

14. Advanced Closure Patterns
    - 14.1 Module Pattern
    - 14.2 Factory Functions
    - 14.3 Private Variables
    - 14.4 Currying
    - 14.5 Function Composition
    - 14.6 Memoization
    - 14.7 Closure Performance Considerations

### **PART 7: ADVANCED TOPICS**

15. Execution Context in ES6+
    - 15.1 Block Scoping with let and const
    - 15.2 Arrow Functions and Lexical This
    - 15.3 Classes and Execution Context
    - 15.4 Modules and Module Scope
    - 15.5 Async/Await and Execution Context
    - 15.6 Generators and Execution Context

16. Asynchronous JavaScript and Execution Context
    - 16.1 Event Loop Explained
    - 16.2 Call Stack vs Callback Queue
    - 16.3 Microtasks vs Macrotasks
    - 16.4 Promise Execution Context
    - 16.5 Async Function Execution
    - 16.6 SetTimeout and SetInterval
    - 16.7 RequestAnimationFrame

17. Memory Management
    - 17.1 Garbage Collection Basics
    - 17.2 Memory Leaks in Closures
    - 17.3 WeakMap and WeakSet
    - 17.4 Memory Profiling
    - 17.5 Optimization Techniques

18. Debugging Execution Context
    - 18.1 Chrome DevTools
    - 18.2 Breakpoints and Call Stack
    - 18.3 Scope Inspector
    - 18.4 Watch Expressions
    - 18.5 Console Methods
    - 18.6 Performance Profiling

### **PART 8: PRACTICAL APPLICATIONS**

19. Real-World Scenarios
    - 19.1 Event Handlers and Context
    - 19.2 AJAX Callbacks
    - 19.3 React Component Methods
    - 19.4 Node.js and Global Context
    - 19.5 Web Workers
    - 19.6 Service Workers

20. Common Patterns and Anti-Patterns
    - 20.1 Best Practices
    - 20.2 Code Smells
    - 20.3 Refactoring Examples
    - 20.4 Performance Patterns

21. Interview Questions and Answers
    - 21.1 Beginner Level
    - 21.2 Intermediate Level
    - 21.3 Advanced Level
    - 21.4 Tricky Questions

---

# **PART 1: FOUNDATIONAL CONCEPTS**

---

## **1. INTRODUCTION TO EXECUTION CONTEXT**

### **1.1 What is Execution Context?**

**Execution Context** is a fundamental concept in JavaScript that defines the environment in which JavaScript code is evaluated and executed. It's an abstract concept (meaning you can't directly see or touch it) that the JavaScript engine uses internally to keep track of the code that is running.

Think of execution context as a "container" or "wrapper" that holds:
- **Variables** (identifiers and their values)
- **Functions** (function declarations and expressions)
- **Objects** (including the global object)
- **The scope chain** (for variable resolution)
- **The value of 'this'** (context object)

#### **Analogy: Execution Context as a Room**

Imagine you're in a room (execution context). This room has:
- **Furniture and objects** (variables and functions)
- **Doors to other rooms** (scope chain/outer references)
- **A note saying "You are here"** (this keyword)
- **A set of rules** (strict mode or not)

When you enter a function, you enter a new room. You can still access things from previous rooms if the doors are open (scope chain), but each room has its own local furniture.

#### **Technical Definition (ECMAScript Specification)**

According to the ECMAScript specification, an execution context is a specification device used to track the runtime evaluation of code. It contains:
- **Code Evaluation State**: Components needed to track execution
- **Function**: The function object being executed (null for global/eval)
- **Realm**: The set of intrinsic objects and environment
- **ScriptOrModule**: Script or module record
- **LexicalEnvironment**: Resolves identifier references
- **VariableEnvironment**: Holds bindings created by variable statements

### **1.2 Why Does Execution Context Matter?**

Understanding execution context is crucial because it explains:

#### **1. How JavaScript Executes Code**

JavaScript doesn't just run code from top to bottom blindly. It creates execution contexts, manages them in a stack, and follows specific rules.

```javascript
console.log("Start");  // What happens here?

function greet() {
    console.log("Hello");  // And here?
}

greet();  // Why does this work?

console.log("End");  // What's the order?

/*
Output:
Start
Hello
End

Why this order? Because of how execution contexts are created and managed!
*/
```

#### **2. Variable and Function Hoisting**

```javascript
// Why doesn't this throw an error?
console.log(myVar);  // undefined (not ReferenceError!)
var myVar = 5;

// Why can we call this before declaration?
sayHello();  // "Hello!"
function sayHello() {
    console.log("Hello!");
}

// But this throws an error?
sayHi();  // TypeError: sayHi is not a function
var sayHi = function() {
    console.log("Hi!");
};
```

**Answer**: During the creation phase of the execution context, declarations are hoisted (moved to the top), but initializations remain in place.

#### **3. Scope and Variable Access**

```javascript
var globalVar = "I'm global";

function outerFunction() {
    var outerVar = "I'm outer";
    
    function innerFunction() {
        var innerVar = "I'm inner";
        
        console.log(innerVar);   // ✓ Can access
        console.log(outerVar);   // ✓ Can access (how?)
        console.log(globalVar);  // ✓ Can access (how?)
    }
    
    innerFunction();
    console.log(innerVar);  // ✗ Cannot access (why?)
}

outerFunction();
console.log(outerVar);  // ✗ Cannot access (why?)
```

**Answer**: The scope chain in execution contexts determines what variables are accessible.

#### **4. The Value of 'this'**

```javascript
const obj = {
    name: "Object",
    regularFunc: function() {
        console.log(this.name);  // "Object"
    },
    arrowFunc: () => {
        console.log(this.name);  // undefined (why different?)
    }
};

obj.regularFunc();
obj.arrowFunc();

const detached = obj.regularFunc;
detached();  // undefined (what happened to 'this'?)
```

**Answer**: 'this' is determined by how the function is called, and this is set in the execution context.

#### **5. Closures**

```javascript
function createCounter() {
    let count = 0;
    
    return function() {
        count++;
        console.log(count);
    };
}

const counter = createCounter();
counter();  // 1
counter();  // 2
counter();  // 3

// How does the inner function still access 'count' 
// even after createCounter() has finished?
```

**Answer**: The inner function's execution context maintains a reference to its outer lexical environment (closure).

#### **6. Asynchronous Behavior**

```javascript
console.log("1");

setTimeout(function() {
    console.log("2");
}, 0);

Promise.resolve().then(function() {
    console.log("3");
});

console.log("4");

// Output: 1, 4, 3, 2 (Why this order?)
```

**Answer**: Understanding the call stack, event loop, and task queues (which manage execution contexts) explains this behavior.

#### **7. Memory Management**

```javascript
function createMemoryLeak() {
    const bigArray = new Array(1000000).fill("data");
    
    return function() {
        console.log(bigArray.length);
    };
}

const leak = createMemoryLeak();
// bigArray remains in memory due to closure
// Understanding execution context helps prevent such leaks
```

### **1.3 The JavaScript Engine Architecture**

To fully understand execution context, we need to understand how JavaScript engines work.

#### **JavaScript Engine Components:**

```
┌─────────────────────────────────────────┐
│         JAVASCRIPT ENGINE               │
├─────────────────────────────────────────┤
│                                         │
│  ┌─────────────────────────────────┐   │
│  │         PARSER                  │   │
│  │  (Converts code to AST)         │   │
│  └─────────────────────────────────┘   │
│                 ↓                       │
│  ┌─────────────────────────────────┐   │
│  │    INTERPRETER (Ignition)       │   │
│  │  (Generates bytecode)           │   │
│  └─────────────────────────────────┘   │
│                 ↓                       │
│  ┌─────────────────────────────────┐   │
│  │   COMPILER (TurboFan)           │   │
│  │  (Optimizes hot code)           │   │
│  └─────────────────────────────────┘   │
│                 ↓                       │
│  ┌─────────────────────────────────┐   │
│  │    EXECUTION CONTEXT            │   │
│  │  (Where code runs)              │   │
│  └─────────────────────────────────┘   │
│                                         │
└─────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│         RUNTIME ENVIRONMENT             │
├─────────────────────────────────────────┤
│  ┌─────────────────────────────────┐   │
│  │      CALL STACK                 │   │
│  │  (Manages execution contexts)   │   │
│  └─────────────────────────────────┘   │
│  ┌─────────────────────────────────┐   │
│  │      HEAP MEMORY                │   │
│  │  (Stores objects & data)        │   │
│  └─────────────────────────────────┘   │
│  ┌─────────────────────────────────┐   │
│  │      WEB APIs                   │   │
│  │  (Browser features)             │   │
│  └─────────────────────────────────┘   │
│  ┌─────────────────────────────────┐   │
│  │      CALLBACK QUEUE             │   │
│  │  (Async callbacks)              │   │
│  └─────────────────────────────────┘   │
│  ┌─────────────────────────────────┐   │
│  │      EVENT LOOP                 │   │
│  │  (Coordinates execution)        │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

#### **Detailed Process:**

**Step 1: Parsing**
```javascript
// Source Code
function add(a, b) {
    return a + b;
}

// Parser creates Abstract Syntax Tree (AST)
/*
FunctionDeclaration
├── Identifier: "add"
├── Parameters
│   ├── Identifier: "a"
│   └── Identifier: "b"
└── BlockStatement
    └── ReturnStatement
        └── BinaryExpression ("+")
            ├── Identifier: "a"
            └── Identifier: "b"
*/
```

**Step 2: Compilation/Interpretation**
- Modern engines use JIT (Just-In-Time) compilation
- Initially interpreted (fast startup)
- Hot code paths are compiled (fast execution)

**Step 3: Execution Context Creation**
- Global Execution Context is created
- Function Execution Contexts created on call
- Managed via Call Stack

### **1.4 Execution Context vs Scope vs Context**

These three terms are often confused. Let's clarify:

#### **Execution Context**
- **What**: Environment where code executes
- **Contains**: Variables, functions, scope chain, 'this'
- **Created**: When script loads (global) or function is called
- **Managed**: Via call stack

```javascript
// Creates Global Execution Context
var global = "global";

function outer() {
    // Creates Function Execution Context for outer()
    var outerVar = "outer";
    
    function inner() {
        // Creates Function Execution Context for inner()
        var innerVar = "inner";
    }
}
```

#### **Scope**
- **What**: Accessibility of variables
- **Types**: Global, Function, Block
- **Determined**: At write-time (lexically)
- **Purpose**: Controls variable visibility

```javascript
var globalScope = "accessible everywhere";

function functionScope() {
    var funcScope = "accessible in function";
    
    if (true) {
        let blockScope = "accessible in block only";
        var notBlockScoped = "actually function scoped";
    }
    
    console.log(funcScope);        // ✓ Works
    console.log(notBlockScoped);   // ✓ Works
    console.log(blockScope);       // ✗ ReferenceError
}
```

#### **Context (The 'this' value)**
- **What**: The object that a function belongs to
- **Determined**: At run-time (how function is called)
- **Can be**: Global object, object, new instance, explicit binding

```javascript
const obj = {
    name: "Object",
    method: function() {
        console.log(this.name);  // 'this' refers to obj
    }
};

obj.method();  // "Object"

const detached = obj.method;
detached();    // undefined - 'this' is now global/undefined
```

#### **Comparison Table:**

| Aspect | Execution Context | Scope | Context ('this') |
|--------|------------------|-------|------------------|
| **Definition** | Environment for code execution | Variable accessibility | Object function belongs to |
| **When Determined** | Runtime (when called) | Write-time (lexical) | Runtime (how called) |
| **Contains** | Variables, functions, scope, 'this' | Variable names | Object reference |
| **Types** | Global, Function, Eval | Global, Function, Block | Global, Object, Instance |
| **Changed By** | Function calls | Code structure | Call method, binding |

#### **Example Showing All Three:**

```javascript
var globalVar = "global";  // Global Scope

const obj = {
    name: "MyObject",
    
    method: function() {
        // Execution Context: created for this function call
        // Scope: can access 'name' and 'globalVar'
        // Context: 'this' refers to obj
        
        var localVar = "local";  // Function Scope
        
        console.log(this.name);      // Context
        console.log(localVar);       // Scope
        console.log(globalVar);      // Scope (outer)
        
        function inner() {
            // New Execution Context created
            // New Scope chain (can access outer scopes)
            // Different Context ('this' is different)
            
            console.log(localVar);     // Accessible via scope chain
            console.log(this.name);    // 'this' is NOT obj here
        }
        
        inner();
    }
};

obj.method();

/*
Execution Context: obj.method() creates execution context
Scope: method() can access obj properties, globalVar, localVar
Context: 'this' in method() is obj, but 'this' in inner() is global/undefined
*/
```

### **1.5 Historical Evolution of Execution Context**

Understanding how execution context has evolved helps appreciate why JavaScript works the way it does.

#### **Early JavaScript (1995-1999) - ES1/ES2/ES3**

```javascript
// No block scope - only function scope
if (true) {
    var x = 10;
}
console.log(x);  // 10 (var leaks out of blocks)

// Only var for variables
var name = "John";

// Only function declarations and expressions
function greet() {
    console.log("Hello");
}

// No arrow functions
var add = function(a, b) {
    return a + b;
};

// 'this' was confusing and unpredictable
var obj = {
    method: function() {
        setTimeout(function() {
            console.log(this);  // Global object, not obj!
        }, 100);
    }
};
```

#### **ES5 (2009) - Improvements**

```javascript
// Strict mode introduced
'use strict';

// Better 'this' control
function Person(name) {
    'use strict';
    // this is undefined if called without 'new'
    this.name = name;
}

// bind, call, apply became standardized
var obj = { name: "Object" };
function greet() {
    console.log(this.name);
}
var bound = greet.bind(obj);
bound();  // "Object"

// Object methods improved
Object.keys()
Object.create()
```

#### **ES6/ES2015 - Major Revolution**

```javascript
// Block scoping with let and const
if (true) {
    let x = 10;
    const y = 20;
}
// console.log(x);  // ReferenceError

// Arrow functions with lexical 'this'
const obj = {
    name: "Object",
    method: function() {
        setTimeout(() => {
            console.log(this.name);  // Works! 'this' is obj
        }, 100);
    }
};

// Classes
class Person {
    constructor(name) {
        this.name = name;
    }
    
    greet() {
        console.log(`Hello, ${this.name}`);
    }
}

// Modules with their own scope
// module.js
export const myVar = 10;

// Template literals
const name = "John";
console.log(`Hello, ${name}`);

// Destructuring
const { x, y } = { x: 10, y: 20 };

// Default parameters
function greet(name = "Guest") {
    console.log(`Hello, ${name}`);
}
```

#### **ES2016+ - Continued Evolution**

```javascript
// Async/Await (ES2017)
async function fetchData() {
    const response = await fetch('/api/data');
    const data = await response.json();
    return data;
}

// Optional Chaining (ES2020)
const user = { profile: { name: "John" } };
console.log(user?.profile?.name);  // "John"
console.log(user?.address?.street);  // undefined (no error)

// Nullish Coalescing (ES2020)
const value = null ?? "default";  // "default"
const value2 = 0 ?? "default";    // 0

// Private Fields (ES2022)
class Counter {
    #count = 0;  // Private field
    
    increment() {
        this.#count++;
    }
    
    getCount() {
        return this.#count;
    }
}

// Top-level await (ES2022)
// In modules:
const data = await fetchData();
```

#### **Impact on Execution Context:**

| Era | Key Changes | Impact on Execution Context |
|-----|-------------|---------------------------|
| **ES3** | Basic function scope | Simple execution contexts |
| **ES5** | Strict mode, better object methods | More predictable 'this', better debugging |
| **ES6** | let/const, arrow functions, classes | Block scope, lexical 'this', simplified context management |
| **ES2017+** | Async/await, optional chaining | Better async context handling, safer property access |

---

## **2. TYPES OF EXECUTION CONTEXTS**

### **2.1 Global Execution Context (GEC)**

The Global Execution Context is the default, outermost execution context. It's created when a JavaScript file first loads.

#### **Characteristics:**

1. **Only ONE per program**
2. **Created automatically** when script loads
3. **Never destroyed** until program terminates
4. **Creates global object** (window in browsers, global in Node.js)
5. **Sets 'this'** to global object
6. **All global code** runs in this context

#### **Detailed Example:**

```javascript
// Everything here is in Global Execution Context

console.log("This runs in GEC");

var globalVar = "I'm global with var";
let globalLet = "I'm global with let";
const globalConst = "I'm global with const";

// Function declaration in GEC
function globalFunction() {
    console.log("Global function");
}

// Object in GEC
const globalObject = {
    name: "Global Object"
};

// This in GEC
console.log(this);  // Window (browser) or Global (Node.js)

/*
Global Execution Context Structure:

GlobalExecutionContext = {
    LexicalEnvironment: {
        EnvironmentRecord: {
            Type: "Object",
            globalLet: "I'm global with let",
            globalConst: "I'm global with const",
            globalFunction: <function object>,
            globalObject: <object reference>
        },
        outer: null,  // No outer environment for global
        ThisBinding: <global object>
    },
    
    VariableEnvironment: {
        EnvironmentRecord: {
            Type: "Object",
            globalVar: "I'm global with var"
        },
        outer: null,
        ThisBinding: <global object>
    }
}
*/
```

#### **Global Object Properties:**

```javascript
// In Browser (Window object):
console.log(window);
console.log(window.document);
console.log(window.alert);
console.log(window.setTimeout);
console.log(window.fetch);

// var creates properties on global object
var myVar = 10;
console.log(window.myVar);  // 10

// let and const do NOT create properties on global object
let myLet = 20;
const myConst = 30;
console.log(window.myLet);    // undefined
console.log(window.myConst);  // undefined

/*
Why? 
- var declarations go to VariableEnvironment (attached to global object)
- let/const declarations go to LexicalEnvironment (separate)
*/
```

#### **Global Context in Different Environments:**

**Browser:**
```javascript
console.log(this);                    // Window
console.log(this === window);         // true
console.log(globalThis === window);   // true (ES2020)

// Access to DOM
console.log(window.document);
console.log(window.navigator);
console.log(window.location);
```

**Node.js:**
```javascript
console.log(this);                    // {} (empty object in modules)
console.log(global);                  // Global object
console.log(globalThis === global);   // true

// Different from browser
console.log(global.process);
console.log(global.require);
console.log(global.Buffer);
```

**Web Worker:**
```javascript
// self refers to worker global scope
console.log(self);
console.log(this === self);  // true

// No access to DOM
console.log(typeof document);  // undefined
console.log(typeof window);    // undefined
```

#### **Global Execution Context Creation Process:**

**Step 1: Creation Phase**
```javascript
// Before any code executes:

/*
1. Global object created (window/global)
2. 'this' set to global object
3. Variables declared with var initialized to undefined
4. Function declarations stored completely
5. let/const declared but uninitialized (TDZ)
*/

// Memory state after creation phase:
/*
globalVar: undefined
globalFunction: <function object in memory>
globalLet: <uninitialized>
globalConst: <uninitialized>
*/
```

**Step 2: Execution Phase**
```javascript
// Code executes line by line:

console.log(globalVar);  // undefined (from creation phase)
var globalVar = "assigned";
console.log(globalVar);  // "assigned"

console.log(globalLet);  // ReferenceError (TDZ)
let globalLet = "value";

globalFunction();  // Works (function already in memory)
```

#### **Multiple Scripts and Global Context:**

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
    <script src="script1.js"></script>
    <script src="script2.js"></script>
</head>
<body>
    <script>
        // inline script
    </script>
</body>
</html>
```

```javascript
// script1.js
var sharedVar = "from script1";
console.log("Script 1 executed");

// script2.js
console.log(sharedVar);  // "from script1"
// Both scripts share the SAME Global Execution Context!

// Potential issues:
var name = "John";  // script1.js
var name = "Jane";  // script2.js - overwrites!
```

#### **Global Context Memory Leaks:**

```javascript
// Anti-pattern 1: Accidental globals
function leaky() {
    // Forgot 'var', 'let', or 'const'
    accidentalGlobal = "I'm global now!";
}
leaky();
console.log(window.accidentalGlobal);  // "I'm global now!"

// Anti-pattern 2: Forgotten timers
setInterval(function() {
    // This runs forever!
    console.log("Still running...");
}, 1000);

// Anti-pattern 3: Detached DOM references
var element = document.getElementById('myDiv');
document.body.removeChild(element);
// 'element' still references the removed DOM node!

// Better:
element = null;  // Allow garbage collection
```

### **2.2 Function Execution Context (FEC)**

A Function Execution Context is created every time a function is invoked.

#### **Characteristics:**

1. **Created on function call**
2. **Destroyed when function returns**
3. **Can have multiple** (one per active function call)
4. **Has access to arguments**
5. **Creates local scope**
6. **'this' value depends on how called**

#### **Detailed Example:**

```javascript
function outerFunction(x) {
    var outerVar = "outer";
    
    function innerFunction(y) {
        var innerVar = "inner";
        console.log(x + y);  // Can access parameters from both
        console.log(outerVar);
        console.log(innerVar);
    }
    
    return innerFunction;
}

const inner = outerFunction(10);
inner(5);

/*
Execution Flow:

1. Global Execution Context created
   - outerFunction stored in memory

2. outerFunction(10) called
   - New Function Execution Context created
   - Parameters: x = 10
   - Variables: outerVar = "outer"
   - innerFunction defined
   - Returns innerFunction

3. inner(5) called (which is innerFunction)
   - New Function Execution Context created
   - Parameters: y = 5
   - Variables: innerVar = "inner"
   - Executes, then destroyed

4. outerFunction's context remains accessible due to closure
*/
```

#### **Function Execution Context Structure:**

```javascript
function exampleFunction(param1, param2) {
    var localVar = "local";
    let blockVar = "block";
    
    function innerFunc() {
        console.log("inner");
    }
    
    console.log(arguments);
}

exampleFunction("arg1", "arg2");

/*
FunctionExecutionContext = {
    LexicalEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative",
            blockVar: "block",
            innerFunc: <function reference>
        },
        outer: <reference to global lexical environment>,
        ThisBinding: <depends on how function was called>
    },
    
    VariableEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative",
            localVar: "local",
            param1: "arg1",
            param2: "arg2",
            arguments: { 0: "arg1", 1: "arg2", length: 2 }
        },
        outer: <reference to global lexical environment>,
        ThisBinding: <depends on how function was called>
    }
}
*/
```

#### **Creation and Execution Phases in FEC:**

```javascript
function demonstratePhases() {
    // Creation Phase happens before this line!
    
    console.log(hoistedVar);  // undefined
    console.log(hoistedFunc); // [Function]
    // console.log(notHoisted); // ReferenceError
    
    var hoistedVar = "I'm hoisted";
    let notHoisted = "I'm in TDZ";
    
    function hoistedFunc() {
        return "I'm hoisted completely";
    }
    
    const notHoistedFunc = function() {
        return "I'm not hoisted";
    };
}

demonstratePhases();

/*
CREATION PHASE:
1. Function Execution Context created
2. 'arguments' object created
3. 'this' determined
4. Variables with 'var' initialized to undefined
5. Function declarations stored completely
6. 'let'/'const' declared but uninitialized

Memory State After Creation Phase:
hoistedVar: undefined
hoistedFunc: <function object>
notHoisted: <uninitialized>
notHoistedFunc: <uninitialized>

EXECUTION PHASE:
Code runs line by line, assigning values
*/
```

#### **Arguments Object:**

```javascript
function showArguments(a, b, c) {
    console.log(arguments);
    console.log(arguments.length);
    console.log(arguments[0]);
    console.log(arguments[1]);
    console.log(arguments[2]);
    
    // arguments is array-like but not an array
    console.log(Array.isArray(arguments));  // false
    
    // Convert to real array
    const argsArray = Array.from(arguments);
    console.log(Array.isArray(argsArray));  // true
    
    // Rest parameters (ES6) - better alternative
    function betterWay(...args) {
        console.log(Array.isArray(args));  // true
    }
}

showArguments(1, 2, 3, 4, 5);

/*
Output:
[Arguments] { '0': 1, '1': 2, '2': 3, '3': 4, '4': 5 }
5
1
2
3
false
true
*/
```

#### **Arrow Functions and Execution Context:**

```javascript
// Arrow functions DON'T create their own execution context
// (in terms of 'this' and 'arguments')

const obj = {
    name: "MyObject",
    
    regularFunc: function() {
        console.log(this.name);      // "MyObject"
        console.log(arguments);      // Arguments object exists
        
        const arrowFunc = () => {
            console.log(this.name);  // "MyObject" (inherited)
            // console.log(arguments); // Would reference outer arguments
        };
        
        arrowFunc();
    },
    
    arrowMethod: () => {
        console.log(this.name);      // undefined
        // 'this' is lexically scoped to global
    }
};

obj.regularFunc("arg1", "arg2");
obj.arrowMethod();

/*
Key Differences:
1. Regular functions: Create their own execution context with 'this' and 'arguments'
2. Arrow functions: Inherit 'this' and don't have 'arguments'
*/
```

#### **Nested Function Execution Contexts:**

```javascript
function level1() {
    console.log("Level 1");
    
    function level2() {
        console.log("Level 2");
        
        function level3() {
            console.log("Level 3");
        }
        
        level3();
    }
    
    level2();
}

level1();

/*
Call Stack Visualization:

Initial:
[Global EC]

After level1() called:
[level1 EC]
[Global EC]

After level2() called:
[level2 EC]
[level1 EC]
[Global EC]

After level3() called:
[level3 EC]
[level2 EC]
[level1 EC]
[Global EC]

After level3() returns:
[level2 EC]
[level1 EC]
[Global EC]

After level2() returns:
[level1 EC]
[Global EC]

After level1() returns:
[Global EC]

Output:
Level 1
Level 2
Level 3
*/
```

#### **Function Context and 'this':**

```javascript
// Regular function call
function regularCall() {
    console.log(this);  // global object (non-strict) or undefined (strict)
}
regularCall();

// Method call
const obj = {
    method: function() {
        console.log(this);  // obj
    }
};
obj.method();

// Constructor call
function Constructor() {
    console.log(this);  // new object
    this.property = "value";
}
new Constructor();

// Explicit binding
function explicit() {
    console.log(this.name);
}
const context = { name: "Context Object" };
explicit.call(context);   // "Context Object"
explicit.apply(context);  // "Context Object"
const bound = explicit.bind(context);
bound();                  // "Context Object"

// Event handler
document.getElementById('btn').addEventListener('click', function() {
    console.log(this);  // the button element
});

// Arrow function (lexical this)
const objWithArrow = {
    name: "Object",
    method: function() {
        const arrow = () => {
            console.log(this.name);  // "Object" (inherited from method)
        };
        arrow();
    }
};
objWithArrow.method();
```

### **2.3 Eval Execution Context**

The `eval()` function creates its own execution context. **Note: eval() is generally considered dangerous and should be avoided.**

#### **How Eval Works:**

```javascript
function testEval() {
    var x = 10;
    
    eval('var y = 20; console.log(x + y);');
    
    console.log(y);  // 20 - eval can modify local scope!
}

testEval();

/*
Eval Execution Context:
1. Created when eval() is executed
2. Has access to calling scope
3. Can create/modify variables in calling scope
4. Extremely dangerous from security perspective
*/
```

#### **Why Eval is Dangerous:**

```javascript
// Security Risk
const userInput = "'; maliciousCode(); '";
eval(userInput);  // Can execute arbitrary code!

// Performance Issues
eval("var x = 10");  // Prevents optimizations

// Debugging Nightmare
function complex() {
    var result;
    eval("result = someComplicatedExpression()");
    // Where did the error occur? Hard to debug!
}

// Scope Pollution
function polluted() {
    var clean = "clean";
    eval("var polluted = 'dirty';");
    console.log(polluted);  // "dirty" - scope corrupted!
}
```

#### **Alternatives to Eval:**

```javascript
// Instead of eval for JSON
// DON'T:
const data = eval('(' + jsonString + ')');

// DO:
const data = JSON.parse(jsonString);

// Instead of eval for property access
// DON'T:
eval('obj.' + propertyName);

// DO:
obj[propertyName];

// Instead of eval for function creation
// DON'T:
eval('function ' + funcName + '() { /* code */ }');

// DO:
const functions = {
    [funcName]: function() { /* code */ }
};

// Instead of eval for expressions
// DON'T:
const result = eval(expression);

// DO:
const Function = new Function('return ' + expression);
const result = Function();
// Still not great, but safer than eval
```

### **2.4 Module Execution Context (ES6+)**

ES6 modules have their own execution context, separate from the global context.

#### **Module Characteristics:**

```javascript
// module.js
console.log(this);  // undefined (in modules, not global object!)

// Strict mode is automatic in modules
// No need for 'use strict';

// Variables are module-scoped, not global
var moduleVar = "I'm not global";
let moduleLet = "Also not global";

export const exportedValue = "I'm exported";

/*
Module Execution Context:
1. Separate from global context
2. Strict mode by default
3. 'this' is undefined at top level
4. Variables don't leak to global scope
5. Imported bindings are read-only
*/
```

#### **Module vs Script Context:**

```javascript
// script.js (traditional script)
console.log(this);  // Window object
var x = 10;
console.log(window.x);  // 10

// module.js (ES6 module)
console.log(this);  // undefined
var x = 10;
console.log(window.x);  // undefined
```

#### **Import/Export and Execution Context:**

```javascript
// math.js
export const PI = 3.14159;

export function add(a, b) {
    return a + b;
}

export default function multiply(a, b) {
    return a * b;
}

// app.js
import multiply, { PI, add } from './math.js';

console.log(PI);           // 3.14159
console.log(add(2, 3));    // 5
console.log(multiply(2, 3)); // 6

/*
Execution Flow:
1. math.js module context created and executed
2. Exports are bound
3. app.js module context created
4. Imports are resolved (live bindings)
5. app.js code executes
*/
```

#### **Module Hoisting:**

```javascript
// Imports are hoisted
console.log(PI);  // 3.14159 (works!)

import { PI } from './math.js';

// But this applies to the import statement, not the module code
// The module itself is only evaluated once, on first import
```

#### **Circular Dependencies:**

```javascript
// a.js
import { b } from './b.js';
export const a = 'a';
console.log('a.js:', b);

// b.js
import { a } from './a.js';
export const b = 'b';
console.log('b.js:', a);

// main.js
import './a.js';

/*
Execution:
1. main.js starts loading a.js
2. a.js starts loading b.js
3. b.js tries to import from a.js
4. a is undefined (not yet initialized)
5. b.js finishes
6. a.js finishes
7. Final values are correct

Output:
b.js: undefined
a.js: b
*/
```

### **2.5 Comparing Different Execution Contexts**

#### **Comprehensive Comparison Table:**

| Feature | Global EC | Function EC | Eval EC | Module EC |
|---------|-----------|-------------|---------|-----------|
| **When Created** | Script load | Function call | eval() call | Module load |
| **Count** | One per program | One per call | One per eval | One per module |
| **'this' Value** | Global object | Depends on call | Caller's this | undefined |
| **Strict Mode** | Optional | Optional | Optional | Always |
| **Variables Scope** | Global | Function | Can modify caller | Module |
| **Hoisting** | Yes | Yes | Yes | Import hoisting |
| **Access to outer** | No | Yes | Yes | Via imports |
| **arguments** | No | Yes | Caller's | No |
| **Destroyed** | Never | After return | After execution | Never |
| **Security** | Safe | Safe | Dangerous | Safe |

#### **Visual Comparison:**

```javascript
// GLOBAL EXECUTION CONTEXT
var globalVar = "global";
console.log(this);  // Window/Global object

function demonstrateAll() {
    // FUNCTION EXECUTION CONTEXT
    var funcVar = "function";
    console.log(this);  // Depends on how called
    console.log(arguments);  // Available
    
    // EVAL EXECUTION CONTEXT (don't use!)
    eval('var evalVar = "eval"; console.log(this);');
    console.log(evalVar);  // "eval" - leaked into function scope!
}

// MODULE EXECUTION CONTEXT
// module.js
export var moduleVar = "module";
console.log(this);  // undefined
// No access to Window directly
// Variables don't become global

demonstrateAll();
```

#### **Nested Contexts Example:**

```javascript
// Global EC
var global = "Global Context";

function outer() {
    // Function EC (outer)
    var outerVar = "Outer Context";
    
    function inner() {
        // Function EC (inner)
        var innerVar = "Inner Context";
        
        console.log(innerVar);   // Own context
        console.log(outerVar);   // Parent context
        console.log(global);     // Global context
        
        // Each has its own execution context
        // But they're linked via scope chain
    }
    
    inner();
}

outer();

/*
Context Hierarchy:

[Global EC]
    ├── global: "Global Context"
    └── outer: <function>
        
        [Outer Function EC]
            ├── outerVar: "Outer Context"
            ├── inner: <function>
            └── Scope Chain → [Global EC]
            
            [Inner Function EC]
                ├── innerVar: "Inner Context"
                └── Scope Chain → [Outer Function EC] → [Global EC]
*/
```

---


## **3. THE EXECUTION CONTEXT STACK (CALL STACK)**

### **3.1 Understanding the Stack Data Structure**

Before diving into the Call Stack, let's understand what a stack is.

#### **Stack Data Structure Basics:**

A stack is a **LIFO (Last In, First Out)** data structure. Think of it like a stack of plates:
- You can only add plates on top (push)
- You can only remove plates from the top (pop)
- You can't access plates in the middle directly

```javascript
// Simple stack implementation
class Stack {
    constructor() {
        this.items = [];
    }
    
    push(element) {
        this.items.push(element);
        console.log(`Pushed: ${element}`);
    }
    
    pop() {
        if (this.items.length === 0) {
            return "Stack is empty";
        }
        const removed = this.items.pop();
        console.log(`Popped: ${removed}`);
        return removed;
    }
    
    peek() {
        return this.items[this.items.length - 1];
    }
    
    isEmpty() {
        return this.items.length === 0;
    }
    
    size() {
        return this.items.length;
    }
    
    print() {
        console.log("Stack:", this.items.join(' -> '));
    }
}

// Example usage
const stack = new Stack();
stack.push('First');   // Bottom
stack.push('Second');
stack.push('Third');   // Top
stack.print();         // Stack: First -> Second -> Third

stack.pop();           // Removes 'Third'
stack.pop();           // Removes 'Second'
stack.print();         // Stack: First

/*
Visual:
        TOP
        ↓
    [Third]  ← Last In, First Out
    [Second]
    [First]
        ↑
      BOTTOM
*/
```

### **3.2 How Call Stack Works**

The JavaScript Call Stack (also called Execution Stack) manages execution contexts using the stack data structure.

#### **Call Stack Rules:**

1. **Global Execution Context** is pushed first
2. When a **function is called**, its execution context is pushed
3. When a **function returns**, its execution context is popped
4. Code in the **top context** is currently executing
5. Stack operates **synchronously**

#### **Basic Call Stack Example:**

```javascript
function first() {
    console.log("Inside first");
    second();
    console.log("Back in first");
}

function second() {
    console.log("Inside second");
    third();
    console.log("Back in second");
}

function third() {
    console.log("Inside third");
}

console.log("Global start");
first();
console.log("Global end");

/*
CALL STACK PROGRESSION:

Step 1: Initial state
┌─────────────┐
│  Global EC  │
└─────────────┘
Output: "Global start"

Step 2: first() called
┌─────────────┐
│   first()   │ ← Currently executing
├─────────────┤
│  Global EC  │
└─────────────┘
Output: "Inside first"

Step 3: second() called inside first()
┌─────────────┐
│  second()   │ ← Currently executing
├─────────────┤
│   first()   │
├─────────────┤
│  Global EC  │
└─────────────┘
Output: "Inside second"

Step 4: third() called inside second()
┌─────────────┐
│   third()   │ ← Currently executing
├─────────────┤
│  second()   │
├─────────────┤
│   first()   │
├─────────────┤
│  Global EC  │
└─────────────┘
Output: "Inside third"

Step 5: third() returns
┌─────────────┐
│  second()   │ ← Currently executing
├─────────────┤
│   first()   │
├─────────────┤
│  Global EC  │
└─────────────┘
Output: "Back in second"

Step 6: second() returns
┌─────────────┐
│   first()   │ ← Currently executing
├─────────────┤
│  Global EC  │
└─────────────┘
Output: "Back in first"

Step 7: first() returns
┌─────────────┐
│  Global EC  │ ← Currently executing
└─────────────┘
Output: "Global end"

FINAL OUTPUT:
Global start
Inside first
Inside second
Inside third
Back in second
Back in first
Global end
*/
```

#### **Detailed Step-by-Step Execution:**

```javascript
let result = 0;

function multiply(a, b) {
    return a * b;
}

function square(n) {
    return multiply(n, n);
}

function printSquare(n) {
    const squared = square(n);
    console.log(squared);
}

printSquare(4);

/*
DETAILED EXECUTION TRACE:

1. Global Execution Context Created
   Stack: [Global EC]
   Variables: result = 0
   Functions: multiply, square, printSquare defined

2. printSquare(4) called
   Stack: [printSquare(4) EC, Global EC]
   - New execution context created
   - Parameter n = 4
   - Waiting for square(n) result

3. square(4) called inside printSquare
   Stack: [square(4) EC, printSquare(4) EC, Global EC]
   - New execution context created
   - Parameter n = 4
   - Waiting for multiply(n, n) result

4. multiply(4, 4) called inside square
   Stack: [multiply(4,4) EC, square(4) EC, printSquare(4) EC, Global EC]
   - New execution context created
   - Parameters a = 4, b = 4
   - Executes: return 4 * 4
   - Returns 16

5. multiply(4, 4) returns 16
   Stack: [square(4) EC, printSquare(4) EC, Global EC]
   - multiply EC destroyed
   - square receives 16
   - Returns 16

6. square(4) returns 16
   Stack: [printSquare(4) EC, Global EC]
   - square EC destroyed
   - printSquare receives 16
   - Stores in 'squared' variable
   - Executes: console.log(16)

7. printSquare(4) completes
   Stack: [Global EC]
   - printSquare EC destroyed
   - Control returns to global context

Output: 16
*/
```

### **3.3 Stack Frames**

Each entry in the call stack is called a **stack frame**. A stack frame contains:

1. **Function being executed**
2. **Function parameters**
3. **Local variables**
4. **Return address** (where to continue after function returns)

#### **Visualizing Stack Frames:**

```javascript
function calculateTotal(price, quantity) {
    const subtotal = price * quantity;
    const tax = subtotal * 0.1;
    const total = subtotal + tax;
    return total;
}

function processOrder(item) {
    const price = item.price;
    const quantity = item.quantity;
    const total = calculateTotal(price, quantity);
    return total;
}

const item = { price: 100, quantity: 2 };
const orderTotal = processOrder(item);
console.log(orderTotal);

/*
STACK FRAME DETAILS:

When calculateTotal(100, 2) is executing:

┌─────────────────────────────────────────┐
│  calculateTotal Stack Frame             │
│  ─────────────────────────────────────  │
│  Parameters:                            │
│    price: 100                           │
│    quantity: 2                          │
│  Local Variables:                       │
│    subtotal: 200                        │
│    tax: 20                              │
│    total: 220                           │
│  Return Address: → processOrder line 4  │
└─────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  processOrder Stack Frame               │
│  ─────────────────────────────────────  │
│  Parameters:                            │
│    item: {price: 100, quantity: 2}      │
│  Local Variables:                       │
│    price: 100                           │
│    quantity: 2                          │
│    total: <waiting for return>          │
│  Return Address: → Global line 14       │
└─────────────────────────────────────────┘

┌─────────────────────────────────────────┐
│  Global Stack Frame                     │
│  ─────────────────────────────────────  │
│  Variables:                             │
│    item: {price: 100, quantity: 2}      │
│    orderTotal: <waiting for return>     │
│  Functions:                             │
│    calculateTotal: <function>           │
│    processOrder: <function>             │
└─────────────────────────────────────────┘
*/
```

### **3.4 Stack Overflow Scenarios**

A **stack overflow** occurs when the call stack exceeds its maximum size.

#### **Example 1: Infinite Recursion**

```javascript
function recursiveFunction() {
    recursiveFunction();  // Calls itself forever!
}

recursiveFunction();
// RangeError: Maximum call stack size exceeded

/*
Call Stack Growth:
┌────────────────────┐
│ recursiveFunction()│ ← 10000th call
├────────────────────┤
│ recursiveFunction()│ ← 9999th call
├────────────────────┤
│ recursiveFunction()│ ← 9998th call
├────────────────────┤
│       ...          │
├────────────────────┤
│ recursiveFunction()│ ← 2nd call
├────────────────────┤
│ recursiveFunction()│ ← 1st call
├────────────────────┤
│    Global EC       │
└────────────────────┘
        ↓
   STACK OVERFLOW!
*/
```

#### **Example 2: Deeply Nested Calls**

```javascript
function level1() {
    level2();
}

function level2() {
    level3();
}

function level3() {
    level4();
}

// ... imagine 10,000 levels

function level10000() {
    console.log("Too deep!");
}

level1();
// Eventually: RangeError: Maximum call stack size exceeded
```

#### **Example 3: Missing Base Case in Recursion**

```javascript
// Incorrect factorial (missing base case)
function factorial(n) {
    return n * factorial(n - 1);  // Never stops!
}

factorial(5);
// Stack overflow!

// Correct factorial
function factorialCorrect(n) {
    if (n === 0 || n === 1) {  // Base case
        return 1;
    }
    return n * factorialCorrect(n - 1);
}

factorialCorrect(5);  // 120
```

#### **Stack Size Limits:**

Different JavaScript environments have different stack size limits:

```javascript
// Measure stack depth
let stackDepth = 0;

function measureStack() {
    stackDepth++;
    try {
        measureStack();
    } catch (e) {
        console.log(`Maximum stack depth: ${stackDepth}`);
        console.log(e.message);
    }
}

measureStack();

/*
Typical limits:
- Chrome: ~10,000 - 15,000 frames
- Firefox: ~50,000 - 100,000 frames
- Node.js: ~10,000 - 15,000 frames
- Safari: ~50,000 frames

(Varies by device, memory, and configuration)
*/
```

#### **Preventing Stack Overflow:**

**Solution 1: Tail Call Optimization (TCO) - Theoretical**

```javascript
// Tail-recursive factorial (should be optimized in ES6 strict mode)
function factorial(n, accumulator = 1) {
    'use strict';
    if (n === 0) {
        return accumulator;
    }
    return factorial(n - 1, n * accumulator);  // Tail call
}

// Note: Most engines don't implement TCO yet!
```

**Solution 2: Iterative Approach**

```javascript
// Convert recursion to iteration
function factorialIterative(n) {
    let result = 1;
    for (let i = 2; i <= n; i++) {
        result *= i;
    }
    return result;
}

factorialIterative(10000);  // No stack overflow!
```

**Solution 3: Trampolining**

```javascript
// Trampoline function to avoid stack overflow
function trampoline(fn) {
    while (typeof fn === 'function') {
        fn = fn();
    }
    return fn;
}

function factorial(n, accumulator = 1) {
    if (n === 0) {
        return accumulator;
    }
    return () => factorial(n - 1, n * accumulator);
}

const result = trampoline(() => factorial(10000));
console.log(result);  // Works!
```

### **3.5 Visualizing the Call Stack**

#### **Using Chrome DevTools:**

```javascript
function first() {
    debugger;  // Execution will pause here
    second();
}

function second() {
    debugger;  // And here
    third();
}

function third() {
    debugger;  // And here
    console.log("Third");
}

first();

/*
In Chrome DevTools:
1. Open Developer Tools (F12)
2. Go to Sources tab
3. Refresh page
4. Execution pauses at first debugger
5. Look at Call Stack panel:

Call Stack:
└─ third       (current)
   └─ second
      └─ first
         └─ (anonymous) [Global]

You can click each frame to inspect variables!
*/
```

#### **Manual Call Stack Tracking:**

```javascript
class CallStackTracker {
    constructor() {
        this.stack = [];
    }
    
    push(functionName) {
        this.stack.push(functionName);
        this.display();
    }
    
    pop() {
        const removed = this.stack.pop();
        this.display();
        return removed;
    }
    
    display() {
        console.log('\nCall Stack:');
        console.log('┌' + '─'.repeat(30) + '┐');
        
        if (this.stack.length === 0) {
            console.log('│ (empty)' + ' '.repeat(22) + '│');
        } else {
            for (let i = this.stack.length - 1; i >= 0; i--) {
                const marker = i === this.stack.length - 1 ? ' ← TOP' : '';
                const padding = ' '.repeat(30 - this.stack[i].length - marker.length);
                console.log(`│ ${this.stack[i]}${padding}${marker}│`);
            }
        }
        
        console.log('└' + '─'.repeat(30) + '┘');
    }
}

const tracker = new CallStackTracker();

function first() {
    tracker.push('first()');
    console.log("Executing first");
    second();
    tracker.pop();
}

function second() {
    tracker.push('second()');
    console.log("Executing second");
    third();
    tracker.pop();
}

function third() {
    tracker.push('third()');
    console.log("Executing third");
    tracker.pop();
}

tracker.push('Global');
first();
tracker.pop();

/*
Output:

Call Stack:
┌──────────────────────────────┐
│ Global                  ← TOP│
└──────────────────────────────┘

Call Stack:
┌──────────────────────────────┐
│ first()                 ← TOP│
│ Global                       │
└──────────────────────────────┘
Executing first

Call Stack:
┌──────────────────────────────┐
│ second()                ← TOP│
│ first()                      │
│ Global                       │
└──────────────────────────────┘
Executing second

Call Stack:
┌──────────────────────────────┐
│ third()                 ← TOP│
│ second()                     │
│ first()                      │
│ Global                       │
└──────────────────────────────┘
Executing third

[Stack unwinds back to Global]
*/
```

### **3.6 Call Stack in Different Scenarios**

#### **Scenario 1: Synchronous Code**

```javascript
function syncExample() {
    console.log('1');
    
    function inner() {
        console.log('2');
    }
    
    inner();
    console.log('3');
}

syncExample();
console.log('4');

/*
Call Stack Timeline:

Time 0: [Global EC]
Output: (none yet)

Time 1: [syncExample EC, Global EC]
Output: "1"

Time 2: [inner EC, syncExample EC, Global EC]
Output: "2"

Time 3: [syncExample EC, Global EC]
Output: "3"

Time 4: [Global EC]
Output: "4"

Final Output: 1, 2, 3, 4
*/
```

#### **Scenario 2: Asynchronous Code**

```javascript
function asyncExample() {
    console.log('1');
    
    setTimeout(function timeout() {
        console.log('2');
    }, 0);
    
    Promise.resolve().then(function promise() {
        console.log('3');
    });
    
    console.log('4');
}

asyncExample();
console.log('5');

/*
Call Stack + Event Loop:

CALL STACK          CALLBACK QUEUE       MICROTASK QUEUE
═══════════         ══════════════       ═══════════════

[asyncExample]
[Global]
→ console.log('1')
Output: "1"

→ setTimeout registered         [timeout]
  (goes to Web API, then Callback Queue)

→ Promise registered                          [promise]
  (goes directly to Microtask Queue)

→ console.log('4')
Output: "4"

[Global]
→ console.log('5')
Output: "5"

[Empty]
→ Check Microtask Queue first!   [timeout]     [promise] ← Execute this first

[promise]
→ console.log('3')
Output: "3"

[Empty]
→ Now check Callback Queue        [timeout]
  
[timeout]
→ console.log('2')
Output: "2"

Final Output: 1, 4, 5, 3, 2
*/
```

#### **Scenario 3: Recursive Functions**

```javascript
function factorial(n) {
    console.log(`Computing factorial(${n})`);
    
    if (n === 0 || n === 1) {
        console.log(`Base case reached: returning 1`);
        return 1;
    }
    
    const result = n * factorial(n - 1);
    console.log(`factorial(${n}) = ${result}`);
    return result;
}

factorial(4);

/*
Call Stack Progression:

Step 1:
┌────────────────┐
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: Computing factorial(4)

Step 2:
┌────────────────┐
│ factorial(3)   │
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: Computing factorial(3)

Step 3:
┌────────────────┐
│ factorial(2)   │
│ factorial(3)   │
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: Computing factorial(2)

Step 4:
┌────────────────┐
│ factorial(1)   │
│ factorial(2)   │
│ factorial(3)   │
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: Computing factorial(1)
Output: Base case reached: returning 1

Step 5 (unwinding):
┌────────────────┐
│ factorial(2)   │
│ factorial(3)   │
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: factorial(2) = 2

Step 6:
┌────────────────┐
│ factorial(3)   │
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: factorial(3) = 6

Step 7:
┌────────────────┐
│ factorial(4)   │
│ Global         │
└────────────────┘
Output: factorial(4) = 24

Final Output:
Computing factorial(4)
Computing factorial(3)
Computing factorial(2)
Computing factorial(1)
Base case reached: returning 1
factorial(2) = 2
factorial(3) = 6
factorial(4) = 24
*/
```

---

# **PART 2: DEEP DIVE INTO COMPONENTS**

## **4. ANATOMY OF EXECUTION CONTEXT**

### **4.1 The Three Pillars**

Every execution context is built on three main components:

1. **Variable Environment**
2. **Lexical Environment**
3. **This Binding**

#### **Complete Structure Diagram:**

```javascript
ExecutionContext = {
    // Component 1: Variable Environment
    VariableEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative" | "Object",
            // Storage for var declarations and function declarations
            // Initialized during creation phase
        },
        outer: <reference to outer lexical environment>,
        ThisBinding: <value of this>
    },
    
    // Component 2: Lexical Environment
    LexicalEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative" | "Object" | "Global",
            // Storage for let and const declarations
            // Initially uninitialized (TDZ)
        },
        outer: <reference to outer lexical environment>,
        ThisBinding: <value of this>
    },
    
    // Component 3: This Binding
    ThisBinding: <determined by how function is called>
}
```

#### **Real Example with All Components:**

```javascript
const globalConst = "Global Constant";

function demonstrateComponents(param) {
    var varVariable = "Var Variable";
    let letVariable = "Let Variable";
    const constVariable = "Const Variable";
    
    function innerFunction() {
        console.log("Inner");
    }
    
    console.log(this);
    console.log(arguments);
}

const obj = { name: "Object" };
demonstrateComponents.call(obj, "argument1", "argument2");

/*
EXECUTION CONTEXT FOR demonstrateComponents:

{
    VariableEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative",
            varVariable: "Var Variable",
            innerFunction: <function object>,
            param: "argument1",
            arguments: {
                0: "argument1",
                1: "argument2",
                length: 2
            }
        },
        outer: <Global Lexical Environment>,
        ThisBinding: obj
    },
    
    LexicalEnvironment: {
        EnvironmentRecord: {
            Type: "Declarative",
            letVariable: "Let Variable",
            constVariable: "Const Variable"
        },
        outer: <Global Lexical Environment>,
        ThisBinding: obj
    },
    
    ThisBinding: obj  // Set by .call()
}
*/
```

### **4.2 Variable Environment in Detail**

The **Variable Environment** is a component that stores variable and function declarations made with `var` and function declarations.

#### **What Goes in Variable Environment:**

```javascript
function variableEnvironmentDemo() {
    // These go in Variable Environment:
    var x = 10;
    var y = 20;
    
    function declaredFunction() {
        return "I'm in Variable Environment";
    }
    
    // These do NOT go in Variable Environment:
    let a = 30;        // Goes to Lexical Environment
    const b = 40;      // Goes to Lexical Environment
    
    const expr = function() {  // The variable 'expr' goes to Lexical Environment
        return "Expression";
    };
}

/*
Variable Environment Record:
{
    x: 10,
    y: 20,
    declaredFunction: <function object>,
    arguments: {...}
}
*/
```

#### **Variable Environment and Hoisting:**

```javascript
function hoistingExample() {
    console.log(hoistedVar);      // undefined
    console.log(hoistedFunction); // [Function]
    // console.log(notHoisted);   // ReferenceError
    
    var hoistedVar = "I'm hoisted";
    
    function hoistedFunction() {
        return "I'm fully hoisted";
    }
    
    let notHoisted = "I'm in TDZ";
}

hoistingExample();

/*
Variable Environment during CREATION PHASE:
{
    hoistedVar: undefined,           // Initialized to undefined
    hoistedFunction: <function obj>, // Fully stored
    arguments: {...}
}

Lexical Environment during CREATION PHASE:
{
    notHoisted: <uninitialized>      // TDZ
}
*/
```

#### **Variable Environment with Nested Functions:**

```javascript
function outer() {
    var outerVar = "Outer";
    
    function inner() {
        var innerVar = "Inner";
        console.log(outerVar);  // Access through outer reference
    }
    
    inner();
}

outer();

/*
OUTER's Variable Environment:
{
    EnvironmentRecord: {
        outerVar: "Outer",
        inner: <function>
    },
    outer: <Global Environment>,
    ThisBinding: <global>
}

INNER's Variable Environment (when inner() executes):
{
    EnvironmentRecord: {
        innerVar: "Inner"
    },
    outer: <Outer's Environment>,  // Chain link!
    ThisBinding: <global>
}

This chain allows inner() to access outerVar!
*/
```

### **4.3 Lexical Environment in Detail**

The **Lexical Environment** is similar to Variable Environment but is specifically for `let`, `const`, and function parameters in ES6+.

#### **What Goes in Lexical Environment:**

```javascript
function lexicalEnvironmentDemo() {
    // These go in Lexical Environment:
    let x = 10;
    const y = 20;
    
    // Block scope also creates new Lexical Environment
    if (true) {
        let blockScoped = "Block";
        const alsoBlock = "Also Block";
        var notBlock = "Function Scoped"; // Goes to Variable Environment
    }
    
    // console.log(blockScoped);  // ReferenceError
    console.log(notBlock);        // "Function Scoped"
}

/*
Function's Lexical Environment:
{
    x: 10,
    y: 20
}

Block's Lexical Environment (inside if):
{
    blockScoped: "Block",
    alsoBlock: "Also Block"
}

Variable Environment:
{
    notBlock: "Function Scoped"
}
*/
```

#### **Lexical Environment and Block Scope:**

```javascript
function blockScopeExample() {
    let outerLet = "Outer";
    
    if (true) {
        // New Lexical Environment created for this block
        let blockLet = "Block";
        console.log(outerLet);  // Accessible via outer reference
        console.log(blockLet);  // In current environment
    }
    
    // console.log(blockLet);  // ReferenceError
    console.log(outerLet);     // Accessible
    
    for (let i = 0; i < 3; i++) {
        // New Lexical Environment for each iteration!
        setTimeout(() => console.log(i), 100);
    }
    // Outputs: 0, 1, 2 (each iteration has its own 'i')
}

blockScopeExample();

/*
Lexical Environment Structure:

Function Level:
{
    EnvironmentRecord: { outerLet: "Outer" },
    outer: <Global>,
    ThisBinding: <global>
}
    ↓
Block Level (if):
{
    EnvironmentRecord: { blockLet: "Block" },
    outer: <Function Level>,
    ThisBinding: <inherited>
}
    ↓
Block Level (for - iteration 0):
{
    EnvironmentRecord: { i: 0 },
    outer: <Function Level>,
    ThisBinding: <inherited>
}
    ↓
Block Level (for - iteration 1):
{
    EnvironmentRecord: { i: 1 },
    outer: <Function Level>,
    ThisBinding: <inherited>
}
*/
```

#### **Temporal Dead Zone (TDZ) in Lexical Environment:**

```javascript
function tdzExample() {
    // TDZ starts here for 'x' and 'y'
    
    console.log(varVariable);  // undefined (in Variable Environment)
    // console.log(x);         // ReferenceError (in TDZ)
    // console.log(y);         // ReferenceError (in TDZ)
    
    var varVariable = "Var";
    let x = "Let";    // TDZ ends for x
    const y = "Const"; // TDZ ends for y
}

/*
Lexical Environment during Creation Phase:
{
    x: <uninitialized>,  // TDZ
    y: <uninitialized>   // TDZ
}

Lexical Environment after declarations:
{
    x: "Let",
    y: "Const"
}
*/
```

### **4.4 This Binding Mechanism**

The **This Binding** determines the value of the `this` keyword in the execution context.

#### **This Binding Rules:**

```javascript
// Rule 1: Default Binding (Global Context)
function defaultBinding() {
    console.log(this);  // Global object (non-strict) or undefined (strict)
}
defaultBinding();

// Rule 2: Implicit Binding (Method Call)
const obj = {
    name: "Object",
    method: function() {
        console.log(this.name);  // "Object" - this is obj
    }
};
obj.method();

// Rule 3: Explicit Binding (call, apply, bind)
function explicitBinding() {
    console.log(this.name);
}
const context = { name: "Context" };
explicitBinding.call(context);   // "Context"
explicitBinding.apply(context);  // "Context"
const bound = explicitBinding.bind(context);
bound();                          // "Context"

// Rule 4: New Binding (Constructor)
function Constructor(name) {
    this.name = name;
    console.log(this);  // New object
}
new Constructor("Instance");

// Rule 5: Arrow Function (Lexical This)
const objWithArrow = {
    name: "Object",
    method: function() {
        const arrow = () => {
            console.log(this.name);  // "Object" - inherited from method
        };
        arrow();
    }
};
objWithArrow.method();

/*
This Binding Priority (highest to lowest):
1. new binding
2. Explicit binding (call, apply, bind)
3. Implicit binding (method call)
4. Default binding (global or undefined)
5. Arrow functions (lexical, not bound)
*/
```

#### **Detailed This Binding Examples:**

```javascript
// Example 1: Context Loss
const person = {
    name: "John",
    greet: function() {
        console.log(`Hello, ${this.name}`);
    }
};

person.greet();              // "Hello, John" - implicit binding
const greetFunc = person.greet;
greetFunc();                 // "Hello, undefined" - default binding

/*
Execution Context for person.greet():
{
    ThisBinding: person  // Implicit binding
}

Execution Context for greetFunc():
{
    ThisBinding: global  // Default binding (context lost!)
}
*/

// Example 2: Callbacks and This
const obj = {
    name: "Object",
    delayedGreet: function() {
        setTimeout(function() {
            console.log(this.name);  // undefined - 'this' is global
        }, 100);
        
        setTimeout(() => {
            console.log(this.name);  // "Object" - arrow function preserves 'this'
        }, 200);
    }
};

obj.delayedGreet();

// Example 3: Event Handlers
document.getElementById('btn').addEventListener('click', function() {
    console.log(this);  // The button element
});

document.getElementById('btn').addEventListener('click', () => {
    console.log(this);  // Window object (lexical)
});

// Example 4: Nested Functions
const nested = {
    name: "Nested",
    outer: function() {
        console.log(this.name);  // "Nested"
        
        function inner() {
            console.log(this.name);  // undefined - new context
        }
        inner();
        
        const innerArrow = () => {
            console.log(this.name);  // "Nested" - lexical
        };
        innerArrow();
    }
};

nested.outer();
```

### **4.5 Environment Records**

**Environment Records** are the actual storage mechanism within environments.

#### **Types of Environment Records:**

```javascript
/*
1. Declarative Environment Record
   - Used for: function scopes, block scopes
   - Stores: variables, functions, parameters

2. Object Environment Record
   - Used for: global scope, with statements
   - Stores: properties on an object (window/global)

3. Global Environment Record
   - Combination of both
   - Stores: global variables and built-ins
*/

// Example 1: Declarative Environment Record
function declarativeExample() {
    let x = 10;
    const y = 20;
    var z = 30;
    
    /*
    Declarative Environment Record:
    {
        x: 10,
        y: 20,
        z: 30
    }
    */
}

// Example 2: Object Environment Record (Global)
var globalVar = "Global";
let globalLet = "Also Global";

/*
Global Environment Record has TWO components:

Object Environment Record (bound to window):
{
    globalVar: "Global",
    // Also includes: document, console, alert, etc.
}

Declarative Environment Record:
{
    globalLet: "Also Global"
}
*/

console.log(window.globalVar);  // "Global"
console.log(window.globalLet);  // undefined

// Example 3: With Statement (creates Object Environment Record)
const obj = { x: 10, y: 20 };

with (obj) {
    console.log(x);  // 10
    console.log(y);  // 20
    
    /*
    New Object Environment Record created:
    - Bound to obj
    - All property lookups go through obj
    */
}

// Note: 'with' is deprecated and not allowed in strict mode!
```

#### **Environment Record Operations:**

```javascript
/*
Environment Records support these operations:

1. HasBinding(N) - Check if binding exists
2. CreateMutableBinding(N, D) - Create new binding
3. SetMutableBinding(N, V, S) - Set binding value
4. GetBindingValue(N, S) - Get binding value
5. DeleteBinding(N) - Delete binding
6. HasThisBinding() - Check if 'this' exists
7. GetThisBinding() - Get 'this' value
*/

// These happen internally during execution:

function internalOperations() {
    // 1. CreateMutableBinding("x", false)
    let x;
    
    // 2. SetMutableBinding("x", 10, false)
    x = 10;
    
    // 3. GetBindingValue("x", false)
    console.log(x);  // 10
    
    // 4. HasBinding("x") - returns true
    // 5. HasBinding("y") - returns false
}
```

### **4.6 Outer Environment References**

The **outer** reference links environments together, forming the scope chain.

#### **Detailed Scope Chain Example:**

```javascript
const global = "Global Variable";

function level1() {
    const level1Var = "Level 1";
    
    function level2() {
        const level2Var = "Level 2";
        
        function level3() {
            const level3Var = "Level 3";
            
            // Can access all outer scopes!
            console.log(level3Var);  // Own environment
            console.log(level2Var);  // Parent environment
            console.log(level1Var);  // Grandparent environment
            console.log(global);     // Global environment
        }
        
        level3();
    }
    
    level2();
}

level1();

/*
ENVIRONMENT CHAIN:

level3's Environment:
{
    EnvironmentRecord: { level3Var: "Level 3" },
    outer: ───────────────────────────────────┐
}                                             │
                                              ↓
level2's Environment:                         
{
    EnvironmentRecord: { level2Var: "Level 2" },
    outer: ───────────────────────────────────┐
}                                             │
                                              ↓
level1's Environment:
{
    EnvironmentRecord: { level1Var: "Level 1" },
    outer: ───────────────────────────────────┐
}                                             │
                                              ↓
Global Environment:
{
    EnvironmentRecord: { global: "Global Variable" },
    outer: null  // End of chain
}

Variable Resolution:
1. Look in level3's environment → Found level3Var
2. Look in level2's environment → Found level2Var
3. Look in level1's environment → Found level1Var
4. Look in Global environment → Found global
*/
```

#### **Lexical vs Dynamic Scoping:**

```javascript
// JavaScript uses LEXICAL (static) scoping

var x = "Global X";

function outer() {
    var x = "Outer X";
    
    function inner() {
        console.log(x);  // "Outer X" - determined by where defined
    }
    
    return inner;
}

function caller() {
    var x = "Caller X";
    const fn = outer();
    fn();  // Still "Outer X" - NOT "Caller X"!
}

caller();

/*
With LEXICAL scoping:
- Scope is determined at WRITE time (where function is defined)
- inner() is defined inside outer(), so it references outer's x

With DYNAMIC scoping (not JavaScript):
- Scope would be determined at RUN time (where function is called)
- inner() called from caller(), would reference caller's x

JavaScript's Outer Reference Chain:
inner() → outer() → Global

NOT:
inner() → caller() → Global
*/
```

#### **Closures and Outer References:**

```javascript
function createCounter() {
    let count = 0;
    
    return {
        increment: function() {
            count++;
            console.log(count);
        },
        decrement: function() {
            count--;
            console.log(count);
        },
        getCount: function() {
            return count;
        }
    };
}

const counter = createCounter();
counter.increment();  // 1
counter.increment();  // 2
counter.decrement();  // 1
console.log(counter.getCount());  // 1

/*
CLOSURE ENVIRONMENT STRUCTURE:

increment's Environment:
{
    EnvironmentRecord: {},
    outer: ──────────────────────┐
}                                │
                                 ↓
decrement's Environment:         │
{                                │
    EnvironmentRecord: {},       │
    outer: ──────────────────────┤
}                                │
                                 │
getCount's Environment:          │
{                                │
    EnvironmentRecord: {},       │
    outer: ──────────────────────┤
}                                │
                                 ↓
createCounter's Environment (preserved!):
{
    EnvironmentRecord: { count: 1 },
    outer: <Global>
}

All three functions share the SAME outer environment!
This is how they access and modify the same 'count'.
*/
```

---

## **5. CREATION PHASE (MEMORY CREATION PHASE)**

### **5.1 Step-by-Step Process**

The Creation Phase happens BEFORE any code executes. It sets up the execution context.

#### **Creation Phase Steps:**

```javascript
function creationPhaseExample(param1, param2) {
    console.log(a);  // What will this log?
    console.log(b);  // What will this log?
    console.log(c);  // What will this log?
    
    var a = 10;
    let b = 20;
    const c = 30;
    
    function declaredFunc() {
        return "Declared";
    }
    
    const expressionFunc = function() {
        return "Expression";
    };
}

creationPhaseExample("arg1", "arg2");

/*
CREATION PHASE STEPS:

Step 1: Create Execution Context
────────────────────────────────
Empty context object created

Step 2: Create Arguments Object
────────────────────────────────
arguments = {
    0: "arg1",
    1: "arg2",
    length: 2
}

Step 3: Scan for Function Declarations
───────────────────────────────────────
declaredFunc: <function object stored in memory>

Step 4: Scan for Variable Declarations (var)
─────────────────────────────────────────────
a: undefined (initialized)
expressionFunc: undefined (variable part only)

Step 5: Scan for let/const Declarations
────────────────────────────────────────
b: <uninitialized> (TDZ)
c: <uninitialized> (TDZ)

Step 6: Set Up This Binding
────────────────────────────
this: <determined by call type>

Step 7: Set Up Outer Reference
───────────────────────────────
outer: <reference to parent lexical environment>

MEMORY STATE AFTER CREATION PHASE:

Variable Environment:
{
    a: undefined,
    declaredFunc: <function object>,
    expressionFunc: undefined,
    param1: "arg1",
    param2: "arg2",
    arguments: {...}
}

Lexical Environment:
{
    b: <uninitialized>,
    c: <uninitialized>
}

NOW EXECUTION PHASE BEGINS:

console.log(a);  // undefined (from step 4)
console.log(b);  // ReferenceError (TDZ from step 5)
console.log(c);  // ReferenceError (TDZ from step 5)
*/
```

#### **Detailed Creation Phase Visualization:**

```javascript
var globalVar = "global";

function outer(x) {
    var outerVar = "outer";
    let outerLet = "outer let";
    
    function inner(y) {
        var innerVar = "inner";
        const innerConst = "inner const";
        
        console.log(x, y);
        console.log(outerVar, outerLet);
        console.log(innerVar, innerConst);
    }
    
    inner(20);
}

outer(10);

/*
═══════════════════════════════════════════════════════════
CREATION PHASE TIMELINE
═══════════════════════════════════════════════════════════

TIME 0: Script Loads
───────────────────────────────────────────────────────────
GLOBAL EXECUTION CONTEXT CREATION PHASE:

1. Global object created (window/global)
2. this = global object
3. Scan declarations:
   - globalVar: undefined
   - outer: <function object>

Memory State:
{
    VariableEnvironment: {
        globalVar: undefined,
        outer: <function object>
    }
}

TIME 1: outer(10) Called
───────────────────────────────────────────────────────────
OUTER EXECUTION CONTEXT CREATION PHASE:

1. New execution context created
2. arguments object created: { 0: 10, length: 1 }
3. Scan parameters: x = 10
4. Scan function declarations: inner = <function object>
5. Scan var declarations: outerVar = undefined
6. Scan let declarations: outerLet = <uninitialized>
7. Set outer reference: → Global Environment
8. Set this: global object (or undefined in strict)

Memory State:
{
    VariableEnvironment: {
        x: 10,
        outerVar: undefined,
        inner: <function object>,
        arguments: { 0: 10, length: 1 }
    },
    LexicalEnvironment: {
        outerLet: <uninitialized>
    },
    outer: <Global Environment>
}

TIME 2: inner(20) Called
───────────────────────────────────────────────────────────
INNER EXECUTION CONTEXT CREATION PHASE:

1. New execution context created
2. arguments object created: { 0: 20, length: 1 }
3. Scan parameters: y = 20
4. Scan var declarations: innerVar = undefined
5. Scan const declarations: innerConst = <uninitialized>
6. Set outer reference: → Outer Environment
7. Set this: global object (or undefined in strict)

Memory State:
{
    VariableEnvironment: {
        y: 20,
        innerVar: undefined,
        arguments: { 0: 20, length: 1 }
    },
    LexicalEnvironment: {
        innerConst: <uninitialized>
    },
    outer: <Outer Environment>
}

═══════════════════════════════════════════════════════════
CALL STACK AFTER ALL CREATION PHASES:
═══════════════════════════════════════════════════════════

┌─────────────────────────────────────────┐
│  inner() Execution Context              │
│  ─────────────────────────────────────  │
│  VarEnv: { y: 20, innerVar: undefined } │
│  LexEnv: { innerConst: <uninit> }       │
│  outer: → Outer Environment             │
├─────────────────────────────────────────┤
│  outer() Execution Context              │
│  ─────────────────────────────────────  │
│  VarEnv: { x: 10, outerVar: undefined } │
│  LexEnv: { outerLet: <uninit> }         │
│  outer: → Global Environment            │
├─────────────────────────────────────────┤
│  Global Execution Context               │
│  ─────────────────────────────────────  │
│  VarEnv: { globalVar: undefined }       │
│  outer: null                            │
└─────────────────────────────────────────┘

NOW EXECUTION PHASES BEGIN (bottom to top)
*/
```

### **5.2 Variable Object Creation**

During the creation phase, a **Variable Object** (or Environment Record) is created.

#### **Variable Object Contents:**

```javascript
function variableObjectDemo(a, b) {
    var x = 10;
    var y = 20;
    
    function foo() {
        return "foo";
    }
    
    var bar = function() {
        return "bar";
    };
    
    let letVar = 30;
    const constVar = 40;
}

variableObjectDemo(1, 2);

/*
VARIABLE OBJECT AFTER CREATION PHASE:

VariableEnvironment (Variable Object):
{
    // 1. Function parameters
    a: 1,
    b: 2,
    
    // 2. Function declarations (complete)
    foo: <function object>,
    
    // 3. Variable declarations (var - initialized to undefined)
    x: undefined,
    y: undefined,
    bar: undefined,  // Only the variable, not the function!
    
    // 4. Arguments object
    arguments: {
        0: 1,
        1: 2,
        length: 2,
        callee: <function reference>
    }
}

LexicalEnvironment:
{
    // let and const (uninitialized - TDZ)
    letVar: <uninitialized>,
    constVar: <uninitialized>
}

AFTER EXECUTION PHASE:

VariableEnvironment:
{
    a: 1,
    b: 2,
    foo: <function object>,
    x: 10,          // Assigned
    y: 20,          // Assigned
    bar: <function object>,  // Assigned
    arguments: {...}
}

LexicalEnvironment:
{
    letVar: 30,     // Initialized
    constVar: 40    // Initialized
}
*/
```

#### **Variable Object with Complex Scenarios:**

```javascript
function complexScenario(param) {
    // What's accessible and when?
    
    console.log("1:", param);           // ?
    console.log("2:", declaredFunc);    // ?
    console.log("3:", varVariable);     // ?
    console.log("4:", letVariable);     // ?
    console.log("5:", expressionFunc);  // ?
    console.log("6:", arrowFunc);       // ?
    
    var varVariable = "var";
    let letVariable = "let";
    
    function declaredFunc() {
        return "declared";
    }
    
    var expressionFunc = function() {
        return "expression";
    };
    
    var arrowFunc = () => {
        return "arrow";
    };
}

try {
    complexScenario("parameter");
} catch(e) {
    console.log("Error:", e.message);
}

/*
OUTPUT AND EXPLANATION:

1: parameter
   ✓ Parameters are set during creation phase

2: [Function: declaredFunc]
   ✓ Function declarations are fully hoisted

3: undefined
   ✓ var is hoisted and initialized to undefined

4: ReferenceError: Cannot access 'letVariable' before initialization
   ✗ let is in TDZ during creation phase
   
(Execution stops here due to error)

If we commented out line 4:

5: undefined
   ✓ var expressionFunc is hoisted (variable part)
   ✗ But function expression is not hoisted

6: undefined
   ✓ var arrowFunc is hoisted (variable part)
   ✗ But arrow function is not hoisted

═══════════════════════════════════════════════════════════

CREATION PHASE MEMORY:
{
    VariableEnvironment: {
        param: "parameter",
        declaredFunc: <function object>,
        varVariable: undefined,
        expressionFunc: undefined,
        arrowFunc: undefined
    },
    LexicalEnvironment: {
        letVariable: <uninitialized>
    }
}
*/
```

### **5.3 Scope Chain Formation**

The **Scope Chain** is formed during the creation phase by linking outer environment references.

#### **Scope Chain Formation Process:**

```javascript
var globalVar = "global";

function level1(a) {
    var level1Var = "level1";
    
    function level2(b) {
        var level2Var = "level2";
        
        function level3(c) {
            var level3Var = "level3";
            
            // Scope chain allows access to all outer variables
            console.log(level3Var);  // Own scope
            console.log(level2Var);  // Parent scope
            console.log(level1Var);  // Grandparent scope
            console.log(globalVar);  // Global scope
            console.log(a, b, c);    // Parameters from all scopes
        }
        
        level3("c");
    }
    
    level2("b");
}

level1("a");

/*
═══════════════════════════════════════════════════════════
SCOPE CHAIN FORMATION
═══════════════════════════════════════════════════════════

STEP 1: Global Execution Context Created
─────────────────────────────────────────
Scope Chain: null
├─ globalVar: undefined
├─ level1: <function>
└─ outer: null

STEP 2: level1() Execution Context Created
───────────────────────────────────────────
Scope Chain: → Global
├─ a: "a"
├─ level1Var: undefined
├─ level2: <function>
└─ outer: → Global Scope

STEP 3: level2() Execution Context Created
───────────────────────────────────────────
Scope Chain: → level1 → Global
├─ b: "b"
├─ level2Var: undefined
├─ level3: <function>
└─ outer: → level1 Scope

STEP 4: level3() Execution Context Created
───────────────────────────────────────────
Scope Chain: → level2 → level1 → Global
├─ c: "c"
├─ level3Var: undefined
└─ outer: → level2 Scope

═══════════════════════════════════════════════════════════
COMPLETE SCOPE CHAIN VISUALIZATION
═══════════════════════════════════════════════════════════

level3 Execution Context
┌─────────────────────────────┐
│ c: "c"                      │
│ level3Var: undefined        │
│ outer: ───┐                 │
└───────────┼─────────────────┘
            │
            ↓
level2 Execution Context
┌─────────────────────────────┐
│ b: "b"                      │
│ level2Var: undefined        │
│ level3: <function>          │
│ outer: ───┐                 │
└───────────┼─────────────────┘
            │
            ↓
level1 Execution Context
┌─────────────────────────────┐
│ a: "a"                      │
│ level1Var: undefined        │
│ level2: <function>          │
│ outer: ───┐                 │
└───────────┼─────────────────┘
            │
            ↓
Global Execution Context
┌─────────────────────────────┐
│ globalVar: "global"         │
│ level1: <function>          │
│ outer: null                 │
└─────────────────────────────┘

═══════════════════════════════════════════════════════════
IDENTIFIER RESOLUTION (during execution)
═══════════════════════════════════════════════════════════

When level3 tries to access 'level1Var':

1. Search in level3 scope: NOT FOUND
2. Follow outer → Search in level2 scope: NOT FOUND
3. Follow outer → Search in level1 scope: FOUND! ✓
4. Return value: "level1"

When level3 tries to access 'a':

1. Search in level3 scope: NOT FOUND
2. Follow outer → Search in level2 scope: NOT FOUND
3. Follow outer → Search in level1 scope: FOUND! ✓
4. Return value: "a"

This chain is FIXED at function DEFINITION time (lexical scoping)!
*/
```

#### **Scope Chain with Closures:**

```javascript
function outer() {
    var outerVar = "outer";
    
    function middle() {
        var middleVar = "middle";
        
        function inner() {
            var innerVar = "inner";
            
            console.log(innerVar);   // inner scope
            console.log(middleVar);  // middle scope (via scope chain)
            console.log(outerVar);   // outer scope (via scope chain)
        }
        
        return inner;
    }
    
    return middle;
}

const middleFunc = outer();
const innerFunc = middleFunc();
innerFunc();

/*
EVEN AFTER outer() AND middle() HAVE RETURNED:

innerFunc still has access to their variables!

innerFunc's Scope Chain (preserved via closure):
┌──────────────────┐
│ inner scope      │
│ innerVar: "in"   │
│ outer: ───┐      │
└───────────┼──────┘
            │
            ↓
┌──────────────────┐
│ middle scope     │ ← STILL IN MEMORY (Closure!)
│ middleVar: "mid" │
│ outer: ───┐      │
└───────────┼──────┘
            │
            ↓
┌──────────────────┐
│ outer scope      │ ← STILL IN MEMORY (Closure!)
│ outerVar: "out"  │
│ outer: ───┐      │
└───────────┼──────┘
            │
            ↓
┌──────────────────┐
│ Global scope     │
│ outer: <func>    │
│ middleFunc: ...  │
│ innerFunc: ...   │
└──────────────────┘

The scope chain is preserved in memory as long as
innerFunc exists, allowing it to access outer variables.
*/
```

### **5.4 This Determination**

The value of `this` is determined during the **creation phase** based on how the function is called.

#### **This Determination Rules:**

```javascript
// Rule 1: Global Context
console.log(this);  // Window (browser) or Global (Node.js)

/*
Global Execution Context:
{
    ThisBinding: <global object>
}
*/

// Rule 2: Function Call (non-strict)
function regularFunction() {
    console.log(this);  // Global object
}
regularFunction();

/*
regularFunction Execution Context:
{
    ThisBinding: <global object>  // Default binding
}
*/

// Rule 3: Function Call (strict mode)
function strictFunction() {
    'use strict';
    console.log(this);  // undefined
}
strictFunction();

/*
strictFunction Execution Context:
{
    ThisBinding: undefined  // Strict mode default
}
*/

// Rule 4: Method Call
const obj = {
    name: "Object",
    method: function() {
        console.log(this);  // obj
        console.log(this.name);  // "Object"
    }
};
obj.method();

/*
method Execution Context:
{
    ThisBinding: obj  // Implicit binding
}
*/

// Rule 5: Constructor Call
function Person(name) {
    this.name = name;
    console.log(this);  // New object being created
}
const person = new Person("John");

/*
Person Execution Context (with 'new'):
{
    ThisBinding: <newly created object>  // New binding
}

Process:
1. New empty object created: {}
2. This bound to new object
3. Object's [[Prototype]] set to Person.prototype
4. Constructor executes with this = new object
5. If no explicit return, return this
*/

// Rule 6: Explicit Binding
function explicitBinding(greeting) {
    console.log(`${greeting}, ${this.name}`);
}

const context = { name: "Context" };

explicitBinding.call(context, "Hello");
// "Hello, Context"

explicitBinding.apply(context, ["Hi"]);
// "Hi, Context"

const boundFunc = explicitBinding.bind(context);
boundFunc("Hey");
// "Hey, Context"

/*
Execution Context with call/apply:
{
    ThisBinding: context  // Explicitly set
}

Execution Context with bind:
- Creates new function with 'this' permanently bound
{
    ThisBinding: context  // Cannot be changed!
}
*/

// Rule 7: Arrow Functions
const objWithArrow = {
    name: "Object",
    regularMethod: function() {
        console.log("Regular:", this.name);  // "Object"
        
        const arrowFunc = () => {
            console.log("Arrow:", this.name);  // "Object" (inherited)
        };
        
        arrowFunc();
        
        setTimeout(function() {
            console.log("Callback:", this.name);  // undefined
        }, 100);
        
        setTimeout(() => {
            console.log("Arrow Callback:", this.name);  // "Object"
        }, 200);
    }
};

objWithArrow.regularMethod();

/*
regularMethod Execution Context:
{
    ThisBinding: objWithArrow  // Implicit binding
}

arrowFunc Execution Context:
{
    ThisBinding: <INHERITED from regularMethod>  // Lexical this
}

setTimeout callback Execution Context:
{
    ThisBinding: <global>  // New context, default binding
}

setTimeout arrow callback Execution Context:
{
    ThisBinding: <INHERITED from regularMethod>  // Lexical this
}
*/
```

#### **This Determination Priority:**

```javascript
function demonstratePriority(name) {
    this.name = name;
}

const obj = { name: "Object" };

// Test 1: Regular call vs new
console.log("Test 1:");
demonstratePriority("Regular");  // this = global
const instance = new demonstratePriority("New");  // this = new object
console.log(window.name);      // "Regular" (if browser, non-strict)
console.log(instance.name);    // "New"

// Test 2: new vs bind
console.log("\nTest 2:");
const boundFunc = demonstratePriority.bind(obj);
boundFunc("Bound");            // this = obj
console.log(obj.name);         // "Bound"

const instanceFromBound = new boundFunc("New from Bound");
console.log(instanceFromBound.name);  // "New from Bound"
console.log(obj.name);                // Still "Bound"
// new overrides bind!

// Test 3: call/apply vs bind
console.log("\nTest 3:");
const boundToObj = demonstratePriority.bind({ name: "Bound Context" });
boundToObj.call({ name: "Call Context" }, "Called");
// this is still "Bound Context", call doesn't override bind!

/*
THIS BINDING PRIORITY (Highest to Lowest):

1. new binding
   new Func() → new object

2. Explicit binding
   func.call(obj) → obj
   func.apply(obj) → obj
   
3. Hard binding (bind)
   func.bind(obj) → obj (cannot be overridden except by new)

4. Implicit binding
   obj.method() → obj

5. Default binding
   func() → global (non-strict) or undefined (strict)

6. Arrow functions
   Use lexical this (from enclosing scope)
   CANNOT be changed by any of the above!
*/
```

### **5.5 Memory Allocation Patterns**

Understanding how memory is allocated during creation phase helps optimize code.

#### **Memory Allocation for Different Declaration Types:**

```javascript
function memoryAllocationDemo() {
    // Different declarations, different memory patterns
    
    var varPrimitive = 10;           // Stack
    var varObject = { x: 10 };       // Reference on stack, object on heap
    
    let letPrimitive = 20;           // Stack
    let letObject = { y: 20 };       // Reference on stack, object on heap
    
    const constPrimitive = 30;       // Stack
    const constObject = { z: 30 };   // Reference on stack, object on heap
    
    function declaredFunction() {}   // Function object on heap
    const arrowFunction = () => {};  // Function object on heap
}

/*
═══════════════════════════════════════════════════════════
MEMORY LAYOUT AFTER CREATION PHASE
═══════════════════════════════════════════════════════════

STACK (Execution Context):
┌─────────────────────────────────────────┐
│ Variable Environment                    │
├─────────────────────────────────────────┤
│ varPrimitive: undefined                 │
│ varObject: undefined                    │
│ declaredFunction: <ref to heap address> │→ Heap
├─────────────────────────────────────────┤
│ Lexical Environment                     │
├─────────────────────────────────────────┤
│ letPrimitive: <uninitialized>           │
│ letObject: <uninitialized>              │
│ constPrimitive: <uninitialized>         │
│ constObject: <uninitialized>            │
│ arrowFunction: <uninitialized>          │
└─────────────────────────────────────────┘

HEAP (Objects and Functions):
┌─────────────────────────────────────────┐
│ Function Object: declaredFunction       │
│ - [[Code]]: function body               │
│ - [[Scope]]: lexical environment ref    │
│ - prototype: {...}                      │
└─────────────────────────────────────────┘

(Other objects allocated during execution phase)

═══════════════════════════════════════════════════════════
MEMORY LAYOUT AFTER EXECUTION PHASE
═══════════════════════════════════════════════════════════

STACK:
┌─────────────────────────────────────────┐
│ Variable Environment                    │
├─────────────────────────────────────────┤
│ varPrimitive: 10                        │
│ varObject: <ref to 0x1000>              │→ Heap 0x1000
│ declaredFunction: <ref to 0x2000>       │→ Heap 0x2000
├─────────────────────────────────────────┤
│ Lexical Environment                     │
├─────────────────────────────────────────┤
│ letPrimitive: 20                        │
│ letObject: <ref to 0x1100>              │→ Heap 0x1100
│ constPrimitive: 30                      │
│ constObject: <ref to 0x1200>            │→ Heap 0x1200
│ arrowFunction: <ref to 0x2100>          │→ Heap 0x2100
└─────────────────────────────────────────┘

HEAP:
┌──────────────────────────────────┐
│ 0x1000: { x: 10 }                │ ← varObject
├──────────────────────────────────┤
│ 0x1100: { y: 20 }                │ ← letObject
├──────────────────────────────────┤
│ 0x1200: { z: 30 }                │ ← constObject
├──────────────────────────────────┤
│ 0x2000: Function Object          │ ← declaredFunction
│         (created in creation)    │
├──────────────────────────────────┤
│ 0x2100: Function Object          │ ← arrowFunction
│         (created in execution)   │
└──────────────────────────────────┘
*/
```

#### **Memory Allocation for Closures:**

```javascript
function createCounter() {
    let count = 0;  // This will be kept in memory!
    
    return function() {
        count++;
        return count;
    };
}

const counter1 = createCounter();
const counter2 = createCounter();

console.log(counter1());  // 1
console.log(counter1());  // 2
console.log(counter2());  // 1 (separate closure)
console.log(counter2());  // 2

/*
═══════════════════════════════════════════════════════════
CLOSURE MEMORY PATTERN
═══════════════════════════════════════════════════════════

After createCounter() is called twice:

HEAP:
┌──────────────────────────────────────────┐
│ Closure 1 (for counter1)                 │
│ ────────────────────────────────────     │
│ Lexical Environment:                     │
│   count: 2 (after two calls)             │
│                                          │
│ Function Object:                         │
│   [[Code]]: function body                │
│   [[Scope]]: → Closure 1 Lex Env         │
└──────────────────────────────────────────┘

┌──────────────────────────────────────────┐
│ Closure 2 (for counter2)                 │
│ ────────────────────────────────────     │
│ Lexical Environment:                     │
│   count: 2 (after two calls)             │
│                                          │
│ Function Object:                         │
│   [[Code]]: same function body           │
│   [[Scope]]: → Closure 2 Lex Env         │
└──────────────────────────────────────────┘

GLOBAL:
┌──────────────────────────────────────────┐
│ counter1: <ref to Closure 1 Function>   │
│ counter2: <ref to Closure 2 Function>   │
└──────────────────────────────────────────┘

Each closure maintains its own copy of the lexical environment!
*/
```

### **5.6 Differences Between var, let, and const**

#### **Complete Comparison During Creation Phase:**

```javascript
function compareDeclarations() {
    // Access before declaration
    console.log("var:", varVariable);        // undefined
    // console.log("let:", letVariable);     // ReferenceError
    // console.log("const:", constVariable); // ReferenceError
    
    // Declaration
    var varVariable = "var";
    let letVariable = "let";
    const constVariable = "const";
    
    // Reassignment
    varVariable = "new var";      // ✓ Allowed
    letVariable = "new let";      // ✓ Allowed
    // constVariable = "new const"; // ✗ TypeError
    
    // Redeclaration
    var varVariable = "redeclared var";      // ✓ Allowed
    // let letVariable = "redeclared let";   // ✗ SyntaxError
    // const constVariable = "redec const";  // ✗ SyntaxError
    
    // Scope
    if (true) {
        var varInBlock = "var in block";
        let letInBlock = "let in block";
        const constInBlock = "const in block";
    }
    
    console.log(varInBlock);    // ✓ "var in block" (function scoped)
    // console.log(letInBlock);   // ✗ ReferenceError (block scoped)
    // console.log(constInBlock); // ✗ ReferenceError (block scoped)
}

/*
═══════════════════════════════════════════════════════════
DETAILED COMPARISON TABLE
═══════════════════════════════════════════════════════════

╔═══════════════╦═══════════╦═══════════╦═══════════════╗
║   Feature     ║    var    ║    let    ║     const     ║
╠═══════════════╬═══════════╬═══════════╬═══════════════╣
║ Scope         ║ Function  ║   Block   ║    Block      ║
║ Hoisting      ║    Yes    ║    Yes    ║     Yes       ║
║ Initialized   ║ undefined ║    No     ║      No       ║
║ TDZ           ║    No     ║    Yes    ║     Yes       ║
║ Reassign      ║    Yes    ║    Yes    ║      No       ║
║ Redeclare     ║    Yes    ║    No     ║      No       ║
║ Global Object ║    Yes    ║    No     ║      No       ║
║ Environment   ║  Variable ║  Lexical  ║   Lexical     ║
╚═══════════════╩═══════════╩═══════════╩═══════════════╝

═══════════════════════════════════════════════════════════
CREATION PHASE BEHAVIOR
═══════════════════════════════════════════════════════════

var varVariable = "value";
───────────────────────────
Creation Phase:
  VariableEnvironment: { varVariable: undefined }
Execution Phase:
  VariableEnvironment: { varVariable: "value" }

let letVariable = "value";
───────────────────────────
Creation Phase:
  LexicalEnvironment: { letVariable: <uninitialized> }
  ← TDZ starts
Execution Phase (at declaration):
  LexicalEnvironment: { letVariable: "value" }
  ← TDZ ends

const constVariable = "value";
───────────────────────────────
Creation Phase:
  LexicalEnvironment: { constVariable: <uninitialized> }
  ← TDZ starts
Execution Phase (at declaration):
  LexicalEnvironment: { constVariable: "value" }
  ← TDZ ends
  ← Cannot be reassigned

═══════════════════════════════════════════════════════════
SCOPE DIFFERENCES
═══════════════════════════════════════════════════════════

function scopeDemo() {
    // Function scope
    var functionScoped = "var";
    
    if (true) {
        // Block scope
        let blockScoped = "let";
        const alsoBlockScoped = "const";
        var notBlockScoped = "var";
        
        console.log(functionScoped);  // ✓ Accessible
        console.log(blockScoped);     // ✓ Accessible
        console.log(alsoBlockScoped); // ✓ Accessible
    }
    
    console.log(functionScoped);   // ✓ Accessible
    console.log(notBlockScoped);   // ✓ Accessible (leaked!)
    // console.log(blockScoped);     // ✗ Not accessible
    // console.log(alsoBlockScoped); // ✗ Not accessible
}

Environment Structure:

Function Level:
{
    VariableEnvironment: {
        functionScoped: "var",
        notBlockScoped: "var"  ← Hoisted to function level!
    }
}
    │
    └─→ Block Level:
        {
            LexicalEnvironment: {
                blockScoped: "let",
                alsoBlockScoped: "const"
            }
        }
        
═══════════════════════════════════════════════════════════
HOISTING DIFFERENCES
═══════════════════════════════════════════════════════════

// var hoisting
console.log(hoistedVar);  // undefined
var hoistedVar = "value";

Interpreted as:
────────────────
var hoistedVar;           // Declaration hoisted
console.log(hoistedVar);  // undefined
hoistedVar = "value";     // Assignment stays

// let hoisting
console.log(hoistedLet);  // ReferenceError
let hoistedLet = "value";

What happens:
─────────────
// let hoistedLet;        ← Hoisted but uninitialized (TDZ)
console.log(hoistedLet);  // ReferenceError (in TDZ)
let hoistedLet = "value"; // TDZ ends here

// const hoisting
console.log(hoistedConst);  // ReferenceError
const hoistedConst = "value";

What happens:
─────────────
// const hoistedConst;        ← Hoisted but uninitialized (TDZ)
console.log(hoistedConst);  // ReferenceError (in TDZ)
const hoistedConst = "value"; // TDZ ends, must have initializer
*/
```

---

## **6. EXECUTION PHASE (CODE EXECUTION PHASE)**

### **6.1 Line-by-Line Execution**

After the creation phase, code executes line by line during the **execution phase**.

#### **Detailed Execution Flow:**

```javascript
function executionPhaseDemo(param) {
    console.log("Step 1: Start execution");
    console.log("param:", param);
    
    var varVariable = "var value";
    console.log("Step 2: varVariable assigned");
    
    let letVariable = "let value";
    console.log("Step 3: letVariable assigned");
    
    function innerFunction() {
        console.log("Step 5: Inner function executing");
    }
    
    console.log("Step 4: About to call inner");
    innerFunction();
    
    console.log("Step 6: Execution complete");
    return "done";
}

const result = executionPhaseDemo("test");
console.log("Result:", result);

/*
═══════════════════════════════════════════════════════════
COMPLETE EXECUTION TIMELINE
═══════════════════════════════════════════════════════════

CREATION PHASE:
──────────────
Time: Before any code runs
Context State:
{
    VariableEnvironment: {
        param: "test",
        varVariable: undefined,
        innerFunction: <function object>,
        arguments: { 0: "test", length: 1 }
    },
    LexicalEnvironment: {
        letVariable: <uninitialized>
    },
    ThisBinding: <global>
}

EXECUTION PHASE:
────────────────

Line 2: console.log("Step 1: Start execution");
─────────────────────────────────────────────────
Output: "Step 1: Start execution"
Context State: (unchanged)

Line 3: console.log("param:", param);
──────────────────────────────────────
Output: "param: test"
Context State: (unchanged - param already set)

Line 5: var varVariable = "var value";
────────────────────────────────────────
Memory Update:
  VariableEnvironment.varVariable: undefined → "var value"
Output: (none)

Line 6: console.log("Step 2: varVariable assigned");
──────────────────────────────────────────────────────
Output: "Step 2: varVariable assigned"

Line 8: let letVariable = "let value";
────────────────────────────────────────
Memory Update:
  LexicalEnvironment.letVariable: <uninitialized> → "let value"
  TDZ ends for letVariable
Output: (none)

Line 9: console.log("Step 3: letVariable assigned");
──────────────────────────────────────────────────────
Output: "Step 3: letVariable assigned"

Line 11-13: function innerFunction() { ... }
──────────────────────────────────────────────
Note: Already in memory from creation phase
Output: (none)

Line 15: console.log("Step 4: About to call inner");
──────────────────────────────────────────────────────
Output: "Step 4: About to call inner"

Line 16: innerFunction();
──────────────────────────
Call Stack Update:
  [innerFunction EC]
  [executionPhaseDemo EC]
  [Global EC]

NEW CONTEXT CREATED FOR innerFunction:
  Creation Phase → Execution Phase
  
Line 12 (inside innerFunction): console.log("Step 5...");
───────────────────────────────────────────────────────────
Output: "Step 5: Inner function executing"

innerFunction returns (implicit):
──────────────────────────────────
Call Stack Update:
  [executionPhaseDemo EC]
  [Global EC]

Line 18: console.log("Step 6: Execution complete");
─────────────────────────────────────────────────────
Output: "Step 6: Execution complete"

Line 19: return "done";
─────────────────────────
Return value: "done"
Context destroyed

Call Stack Update:
  [Global EC]

Line 22: const result = executionPhaseDemo("test");
─────────────────────────────────────────────────────
Memory Update:
  Global.LexicalEnvironment.result: <uninitialized> → "done"

Line 23: console.log("Result:", result);
─────────────────────────────────────────
Output: "Result: done"

═══════════════════════════════════════════════════════════
COMPLETE OUTPUT:
═══════════════════════════════════════════════════════════
Step 1: Start execution
param: test
Step 2: varVariable assigned
Step 3: letVariable assigned
Step 4: About to call inner
Step 5: Inner function executing
Step 6: Execution complete
Result: done
*/
```

### **6.2 Variable Assignment**

Variable assignment happens during execution phase, updating the values set in creation phase.

#### **Assignment Process:**

```javascript
function assignmentDemo() {
    // Creation phase: all declared but not assigned
    var a, b, c;
    let x, y, z;
    
    console.log("Before assignments:");
    console.log("a:", a, "b:", b, "c:", c);  // undefined, undefined, undefined
    console.log("x:", x, "y:", y, "z:", z);  // undefined, undefined, undefined
    
    // Execution phase: assignments happen
    a = 10;
    b = 20;
    c = 30;
    
    x = 40;
    y = 50;
    z = 60;
    
    console.log("After assignments:");
    console.log("a:", a, "b:", b, "c:", c);  // 10, 20, 30
    console.log("x:", x, "y:", y, "z:", z);  // 40, 50, 60
}

assignmentDemo();

/*
═══════════════════════════════════════════════════════════
ASSIGNMENT TIMELINE
═══════════════════════════════════════════════════════════

CREATION PHASE:
───────────────
VariableEnvironment: {
    a: undefined,
    b: undefined,
    c: undefined
}

LexicalEnvironment: {
    x: undefined,
    y: undefined,
    z: undefined
}

EXECUTION PHASE - Assignment Operations:
────────────────────────────────────────

Operation: a = 10
───────────────────
Before: { a: undefined }
After:  { a: 10 }
Steps:
  1. Evaluate right-hand side: 10
  2. Find 'a' in current environment
  3. Update binding: a = 10

Operation: b = 20
───────────────────
Before: { a: 10, b: undefined }
After:  { a: 10, b: 20 }

Operation: c = 30
───────────────────
Before: { a: 10, b: 20, c: undefined }
After:  { a: 10, b: 20, c: 30 }

Operation: x = 40
───────────────────
Before: { x: undefined }
After:  { x: 40 }

Operation: y = 50
───────────────────
Before: { x: 40, y: undefined }
After:  { x: 40, y: 50 }

Operation: z = 60
───────────────────
Before: { x: 40, y: 50, z: undefined }
After:  { x: 40, y: 50, z: 60 }
*/
```

#### **Complex Assignment Operations:**

```javascript
function complexAssignments() {
    // Multiple assignments
    var a, b, c;
    a = b = c = 10;  // Right-to-left evaluation
    console.log(a, b, c);  // 10, 10, 10
    
    // Destructuring assignment
    let [x, y, z] = [1, 2, 3];
    console.log(x, y, z);  // 1, 2, 3
    
    // Object destructuring
    let {name, age} = {name: "John", age: 30};
    console.log(name, age);  // "John", 30
    
    // Compound assignment
    let num = 10;
    num += 5;   // num = num + 5
    num *= 2;   // num = num * 2
    console.log(num);  // 30
    
    // Logical assignment (ES2021)
    let value = null;
    value ??= 10;  // Assign if null or undefined
    console.log(value);  // 10
}

complexAssignments();

/*
═══════════════════════════════════════════════════════════
ASSIGNMENT EVALUATION ORDER
═══════════════════════════════════════════════════════════

Statement: a = b = c = 10;
───────────────────────────

Step-by-step evaluation (right-to-left):

Step 1: c = 10
  Environment: { a: undefined, b: undefined, c: 10 }
  Returns: 10

Step 2: b = 10 (result of Step 1)
  Environment: { a: undefined, b: 10, c: 10 }
  Returns: 10

Step 3: a = 10 (result of Step 2)
  Environment: { a: 10, b: 10, c: 10 }
  Returns: 10

Statement: let [x, y, z] = [1, 2, 3];
───────────────────────────────────────

Step 1: Evaluate right side
  Create array: [1, 2, 3]

Step 2: Pattern matching
  x = array[0]  → 1
  y = array[1]  → 2
  z = array[2]  → 3

Step 3: Assignments
  LexicalEnvironment: { x: 1, y: 2, z: 3 }

Statement: let {name, age} = {name: "John", age: 30};
───────────────────────────────────────────────────────

Step 1: Evaluate right side
  Create object: { name: "John", age: 30 }

Step 2: Property extraction
  name = object.name  → "John"
  age = object.age    → 30

Step 3: Assignments
  LexicalEnvironment: { name: "John", age: 30 }
*/
```

### **6.3 Function Invocation**

Function calls create new execution contexts during the execution phase.

#### **Function Call Process:**

```javascript
function outer(x) {
    console.log("Outer start, x:", x);
    
    function inner(y) {
        console.log("Inner start, y:", y);
        console.log("Inner can access x:", x);
        return x + y;
    }
    
    const result = inner(20);
    console.log("Outer received result:", result);
    return result;
}

const finalResult = outer(10);
console.log("Final result:", finalResult);

/*
═══════════════════════════════════════════════════════════
FUNCTION INVOCATION TIMELINE
═══════════════════════════════════════════════════════════

TIME 0: Global Code Execution
──────────────────────────────
Call Stack: [Global EC]
Code: const finalResult = outer(10);
Action: Prepare to call outer()

TIME 1: outer(10) Called
────────────────────────
Call Stack: [outer EC, Global EC]

outer EC Creation Phase:
  VariableEnvironment: {
    x: 10,
    inner: <function object>,
    result: undefined,
    arguments: { 0: 10, length: 1 }
  }
  ThisBinding: <global>
  outer: <Global Environment>

outer EC Execution Phase:
  Line: console.log("Outer start, x:", x);
  Output: "Outer start, x: 10"
  
  Line: const result = inner(20);
  Action: Prepare to call inner()

TIME 2: inner(20) Called
─────────────────────────
Call Stack: [inner EC, outer EC, Global EC]

inner EC Creation Phase:
  VariableEnvironment: {
    y: 20,
    arguments: { 0: 20, length: 1 }
  }
  ThisBinding: <global>
  outer: <outer's Environment>  ← Scope chain!

inner EC Execution Phase:
  Line: console.log("Inner start, y:", y);
  Output: "Inner start, y: 20"
  
  Line: console.log("Inner can access x:", x);
  Resolution: x not in inner → check outer → Found!
  Output: "Inner can access x: 10"
  
  Line: return x + y;
  Evaluation: 10 + 20 = 30
  Return: 30
  
  Context destroyed

TIME 3: Return to outer EC
───────────────────────────
Call Stack: [outer EC, Global EC]

Continuing outer EC Execution:
  Line: const result = inner(20);
  Memory Update: result = 30
  
  Line: console.log("Outer received result:", result);
  Output: "Outer received result: 30"
  
  Line: return result;
  Return: 30
  
  Context destroyed

TIME 4: Return to Global EC
─────────────────────────────
Call Stack: [Global EC]

Continuing Global Execution:
  Line: const finalResult = outer(10);
  Memory Update: finalResult = 30
  
  Line: console.log("Final result:", finalResult);
  Output: "Final result: 30"

═══════════════════════════════════════════════════════════
COMPLETE OUTPUT:
═══════════════════════════════════════════════════════════
Outer start, x: 10
Inner start, y: 20
Inner can access x: 10
Outer received result: 30
Final result: 30
*/
```

#### **Different Function Call Types:**

```javascript
// 1. Regular function call
function regularCall(x) {
    console.log("Regular:", x, this);
    return x * 2;
}
const result1 = regularCall(5);

// 2. Method call
const obj = {
    value: 10,
    method: function(x) {
        console.log("Method:", x, this.value);
        return x + this.value;
    }
};
const result2 = obj.method(5);

// 3. Constructor call
function Constructor(value) {
    console.log("Constructor:", this);
    this.value = value;
}
const instance = new Constructor(5);

// 4. Indirect call (call/apply)
function indirectCall(x, y) {
    console.log("Indirect:", x, y, this.value);
    return x + y + this.value;
}
const context = { value: 10 };
const result3 = indirectCall.call(context, 5, 3);
const result4 = indirectCall.apply(context, [5, 3]);

// 5. Bound function
const boundFunc = indirectCall.bind(context, 5);
const result5 = boundFunc(3);

/*
═══════════════════════════════════════════════════════════
EXECUTION CONTEXT FOR EACH CALL TYPE
═══════════════════════════════════════════════════════════

1. regularCall(5)
─────────────────
Execution Context: {
    VariableEnvironment: { x: 5 },
    ThisBinding: <global> (or undefined in strict mode),
    outer: <Global Environment>
}
Output: "Regular: 5 <global>"
Return: 10

2. obj.method(5)
────────────────
Execution Context: {
    VariableEnvironment: { x: 5 },
    ThisBinding: obj,  ← Implicit binding
    outer: <Global Environment>
}
Output: "Method: 5 10"
Return: 15

3. new Constructor(5)
─────────────────────
Execution Context: {
    VariableEnvironment: { value: 5 },
    ThisBinding: <newly created object>,  ← New binding
    outer: <Global Environment>
}
Process:
  1. New empty object created: {}
  2. this = new object
  3. new object.[[Prototype]] = Constructor.prototype
  4. Constructor body executes
  5. Return new object (implicit)
Output: "Constructor: {}"
Return: { value: 5 }

4. indirectCall.call(context, 5, 3)
───────────────────────────────────
Execution Context: {
    VariableEnvironment: { x: 5, y: 3 },
    ThisBinding: context,  ← Explicit binding
    outer: <Global Environment>
}
Output: "Indirect: 5 3 10"
Return: 18

5. indirectCall.apply(context, [5, 3])
──────────────────────────────────────
Same as call, but arguments passed as array
Execution Context: Same as above
Output: "Indirect: 5 3 10"
Return: 18

6. boundFunc(3)
───────────────
Execution Context: {
    VariableEnvironment: { x: 5 (pre-bound), y: 3 },
    ThisBinding: context,  ← Permanently bound
    outer: <Global Environment>
}
Output: "Indirect: 5 3 10"
Return: 18
*/
```

### **6.4 Expression Evaluation**

Expressions are evaluated during execution phase following specific rules.

#### **Expression Evaluation Order:**

```javascript
function expressionDemo() {
    // 1. Arithmetic expressions
    const a = 2 + 3 * 4;  // Operator precedence
    console.log("a:", a);  // 14, not 20
    
    // 2. Logical expressions (short-circuit)
    const b = false && expensiveOperation();  // expensiveOperation not called
    console.log("b:", b);  // false
    
    const c = true || expensiveOperation();  // expensiveOperation not called
    console.log("c:", c);  // true
    
    // 3. Function call expressions
    const d = Math.max(1, 2, 3);
    console.log("d:", d);  // 3
    
    // 4. Conditional (ternary) expression
    const e = a > 10 ? "large" : "small";
    console.log("e:", e);  // "large"
    
    // 5. Object/Array expressions
    const f = { x: 1, y: 2 };
    const g = [1, 2, 3];
    
    function expensiveOperation() {
        console.log("Expensive operation called");
        return true;
    }
}

expressionDemo();

/*
═══════════════════════════════════════════════════════════
EXPRESSION EVALUATION DETAILS
═══════════════════════════════════════════════════════════

Expression: const a = 2 + 3 * 4;
─────────────────────────────────

Evaluation Steps:
1. Scan expression for operators
2. Apply precedence rules:
   * (multiplication) has higher precedence than + (addition)
3. Evaluate: 3 * 4 = 12
4. Evaluate: 2 + 12 = 14
5. Assign: a = 14

Operator Precedence (high to low):
  () [] .           // Grouping, member access
  ++ -- ! ~         // Unary
  * / %             // Multiplication, division, modulo
  + -               // Addition, subtraction
  < <= > >=         // Comparison
  == != === !==     // Equality
  &&                // Logical AND
  ||                // Logical OR
  ?:                // Conditional
  = += -= etc       // Assignment

Expression: const b = false && expensiveOperation();
─────────────────────────────────────────────────────

Evaluation Steps (Short-Circuit):
1. Evaluate left operand: false
2. && operator: if left is false, don't evaluate right
3. Return: false
4. Assign: b = false

expensiveOperation() is NEVER called!

Expression: const c = true || expensiveOperation();
────────────────────────────────────────────────────

Evaluation Steps (Short-Circuit):
1. Evaluate left operand: true
2. || operator: if left is true, don't evaluate right
3. Return: true
4. Assign: c = true

expensiveOperation() is NEVER called!

Expression: const d = Math.max(1, 2, 3);
─────────────────────────────────────────

Evaluation Steps:
1. Evaluate arguments left-to-right: 1, 2, 3
2. Call Math.max with arguments
3. New execution context created for Math.max
4. Math.max executes and returns 3
5. Assign: d = 3

Expression: const e = a > 10 ? "large" : "small";
──────────────────────────────────────────────────

Evaluation Steps:
1. Evaluate condition: a > 10
   a is 14, so 14 > 10 = true
2. Condition is true, evaluate first branch: "large"
3. Don't evaluate second branch: "small"
4. Assign: e = "large"

Expression: const f = { x: 1, y: 2 };
───────────────────────────────────────

Evaluation Steps:
1. Create new object in heap
2. Evaluate property values: 1, 2
3. Set properties: x = 1, y = 2
4. Create reference on stack
5. Assign: f = <reference to object>

Memory:
  Stack: f → <ref to 0x1000>
  Heap:  0x1000: { x: 1, y: 2 }
*/
```

#### **Complex Expression Evaluation:**

```javascript
function complexExpressions() {
    let x = 0;
    
    // Expression with side effects
    const a = (x = 5, x + 10);  // Comma operator
    console.log("a:", a, "x:", x);  // 15, 5
    
    // Nested function calls
    const b = parseInt(String(Math.random() * 100));
    console.log("b:", b);
    
    // Chained property access
    const obj = {
        nested: {
            deep: {
                value: 42
            }
        }
    };
    const c = obj.nested.deep.value;
    console.log("c:", c);  // 42
    
    // Computed property access
    const prop = "nested";
    const d = obj[prop]["deep"]["value"];
    console.log("d:", d);  // 42
    
    // Spread operator
    const arr1 = [1, 2, 3];
    const arr2 = [0, ...arr1, 4];
    console.log("arr2:", arr2);  // [0, 1, 2, 3, 4]
}

complexExpressions();

/*
═══════════════════════════════════════════════════════════
COMPLEX EVALUATION EXAMPLES
═══════════════════════════════════════════════════════════

Expression: const a = (x = 5, x + 10);
────────────────────────────────────────

Comma operator evaluates left-to-right, returns last value

Step 1: Evaluate x = 5
  Result: 5
  Side effect: x is now 5

Step 2: Evaluate x + 10
  x is 5, so 5 + 10 = 15
  Result: 15

Step 3: Comma operator returns last value
  Return: 15

Step 4: Assign: a = 15

Final State: a = 15, x = 5

Expression: const b = parseInt(String(Math.random() * 100));
─────────────────────────────────────────────────────────────

Evaluation is inside-out (innermost first):

Step 1: Math.random()
  New EC created for Math.random
  Returns: 0.12345... (random number)
  EC destroyed

Step 2: Math.random() * 100
  0.12345... * 100 = 12.345...
  Returns: 12.345...

Step 3: String(12.345...)
  New EC created for String constructor
  Converts to: "12.345..."
  Returns: "12.345..."
  EC destroyed

Step 4: parseInt("12.345...")
  New EC created for parseInt
  Parses integer part: 12
  Returns: 12
  EC destroyed

Step 5: Assign: b = 12

Expression: const c = obj.nested.deep.value;
─────────────────────────────────────────────

Member access evaluation (left-to-right):

Step 1: Resolve 'obj'
  Look up obj in current environment
  Found: <reference to object>

Step 2: obj.nested
  Access 'nested' property
  Result: <reference to nested object>

Step 3: obj.nested.deep
  Access 'deep' property on nested object
  Result: <reference to deep object>

Step 4: obj.nested.deep.value
  Access 'value' property on deep object
  Result: 42

Step 5: Assign: c = 42

Expression: const arr2 = [0, ...arr1, 4];
──────────────────────────────────────────

Spread operator evaluation:

Step 1: Create new array: []

Step 2: Add first element: [0]

Step 3: Spread arr1
  arr1 is [1, 2, 3]
  Add each element: [0, 1, 2, 3]

Step 4: Add last element: [0, 1, 2, 3, 4]

Step 5: Assign: arr2 = <reference to new array>

Memory:
  Heap:
    arr1: [1, 2, 3]
    arr2: [0, 1, 2, 3, 4]  ← New array, not same as arr1
*/
```

### **6.5 Statement Execution Order**

Statements execute in order during the execution phase, with control flow statements altering the order.

#### **Statement Types and Execution:**

```javascript
function statementDemo() {
    console.log("1. Expression Statement");
    
    // 2. Declaration Statement
    const x = 10;
    let y = 20;
    var z = 30;
    
    // 3. Conditional Statement
    if (x > 5) {
        console.log("2. If block executed");
    } else {
        console.log("2. Else block (not executed)");
    }
    
    // 4. Loop Statement
    for (let i = 0; i < 3; i++) {
        console.log("3. Loop iteration:", i);
    }
    
    // 5. Switch Statement
    switch (x) {
        case 10:
            console.log("4. Switch case 10");
            break;
        case 20:
            console.log("4. Switch case 20 (not executed)");
            break;
        default:
            console.log("4. Default case (not executed)");
    }
    
    // 6. Try-Catch Statement
    try {
        console.log("5. Try block");
        // throw new Error("Test");
    } catch (e) {
        console.log("5. Catch block (not executed)");
    } finally {
        console.log("6. Finally block");
    }
    
    // 7. Return Statement
    console.log("7. Before return");
    return "done";
    console.log("8. After return (not executed)");
}

statementDemo();

/*
═══════════════════════════════════════════════════════════
STATEMENT EXECUTION FLOW
═══════════════════════════════════════════════════════════

Sequential Execution:
─────────────────────
Statements execute one after another unless:
- Control flow statement (if, for, while, switch)
- Jump statement (return, break, continue, throw)
- Function call (creates new execution context)

EXECUTION TIMELINE:

Time 1: Line 2
  Statement: console.log("1. Expression Statement");
  Type: Expression Statement
  Action: Execute expression, discard result
  Output: "1. Expression Statement"

Time 2: Lines 5-7
  Statement: const x = 10; let y = 20; var z = 30;
  Type: Declaration Statements
  Action: Initialize variables (TDZ ends for let/const)
  Memory Update:
    LexicalEnvironment: { x: 10, y: 20 }
    VariableEnvironment: { z: 30 }

Time 3: Lines 10-14
  Statement: if (x > 5) { ... }
  Type: Conditional Statement
  
  Step 1: Evaluate condition
    x > 5 → 10 > 5 → true
  
  Step 2: Condition is true, execute if block
    New Block Execution Context created
    Execute: console.log("2. If block executed");
    Output: "2. If block executed"
    Block context destroyed
  
  Step 3: Skip else block
    Else block NOT executed

Time 4: Lines 17-19
  Statement: for (let i = 0; i < 3; i++)
  Type: Loop Statement
  
  Iteration 1:
    New Block Context: { i: 0 }
    Condition: 0 < 3 → true
    Execute body: console.log("3. Loop iteration:", 0);
    Output: "3. Loop iteration: 0"
    Update: i++ → i = 1
    Block context destroyed
  
  Iteration 2:
    New Block Context: { i: 1 }
    Condition: 1 < 3 → true
    Execute body: console.log("3. Loop iteration:", 1);
    Output: "3. Loop iteration: 1"
    Update: i++ → i = 2
    Block context destroyed
  
  Iteration 3:
    New Block Context: { i: 2 }
    Condition: 2 < 3 → true
    Execute body: console.log("3. Loop iteration:", 2);
    Output: "3. Loop iteration: 2"
    Update: i++ → i = 3
    Block context destroyed
  
  Check condition: 3 < 3 → false
  Exit loop

Time 5: Lines 22-31
  Statement: switch (x) { ... }
  Type: Switch Statement
  
  Step 1: Evaluate discriminant
    x → 10
  
  Step 2: Check cases (strict equality ===)
    case 10: 10 === 10 → true ✓
    Execute: console.log("4. Switch case 10");
    Output: "4. Switch case 10"
    
    Execute: break;
    Exit switch statement
  
  Step 3: Skip remaining cases
    case 20 and default NOT executed

Time 6: Lines 34-41
  Statement: try { ... } catch { ... } finally { ... }
  Type: Try-Catch Statement
  
  Step 1: Execute try block
    Execute: console.log("5. Try block");
    Output: "5. Try block"
    No error thrown, skip catch block
  
  Step 2: Skip catch block
    Catch block NOT executed
  
  Step 3: Execute finally block
    Finally block ALWAYS executes
    Execute: console.log("6. Finally block");
    Output: "6. Finally block"

Time 7: Lines 44-46
  Statement: return "done";
  Type: Return Statement
  
  Step 1: Execute console.log before return
    Output: "7. Before return"
  
  Step 2: Evaluate return expression
    "done"
  
  Step 3: Return from function
    Return value: "done"
    Function execution context destroyed
    Control returns to caller
  
  Step 4: Unreachable code
    Line 46: console.log("8. After return...");
    This line is NEVER executed (unreachable)

═══════════════════════════════════════════════════════════
COMPLETE OUTPUT:
═══════════════════════════════════════════════════════════
1. Expression Statement
2. If block executed
3. Loop iteration: 0
3. Loop iteration: 1
3. Loop iteration: 2
4. Switch case 10
5. Try block
6. Finally block
7. Before return
*/
```

#### **Control Flow and Execution Order:**

```javascript
function controlFlowDemo() {
    console.log("Start");
    
    // Early return
    for (let i = 0; i < 5; i++) {
        console.log("Iteration:", i);
        
        if (i === 2) {
            console.log("Returning early");
            return "early exit";
        }
    }
    
    console.log("This won't execute");
    return "normal exit";
}

const result = controlFlowDemo();
console.log("Result:", result);

/*
═══════════════════════════════════════════════════════════
EXECUTION FLOW WITH EARLY RETURN
═══════════════════════════════════════════════════════════

Iteration 0:
  console.log("Iteration:", 0);
  Output: "Iteration: 0"
  Condition i === 2: false
  Continue loop

Iteration 1:
  console.log("Iteration:", 1);
  Output: "Iteration: 1"
  Condition i === 2: false
  Continue loop

Iteration 2:
  console.log("Iteration:", 2);
  Output: "Iteration: 2"
  Condition i === 2: true ✓
  Execute: console.log("Returning early");
  Output: "Returning early"
  Execute: return "early exit";
  
  FUNCTION EXITS HERE
  - Loop terminated
  - Line 13 NOT executed
  - Line 14 NOT executed
  - Execution context destroyed
  - Return to caller

Back in Global Context:
  const result = controlFlowDemo();
  result = "early exit"
  console.log("Result:", result);
  Output: "Result: early exit"

═══════════════════════════════════════════════════════════
COMPLETE OUTPUT:
═══════════════════════════════════════════════════════════
Start
Iteration: 0
Iteration: 1
Iteration: 2
Returning early
Result: early exit
*/
```

---

# **PART 3: HOISTING MECHANISMS**

## **7. COMPLETE GUIDE TO HOISTING**

### **7.1 What is Hoisting?**

**Hoisting** is JavaScript's behavior of moving declarations to the top of their scope during the creation phase.

#### **Core Concept:**

```javascript
// What you write:
console.log(myVar);
var myVar = 5;

// How JavaScript interprets it:
var myVar;  // Declaration hoisted to top
console.log(myVar);  // undefined
myVar = 5;  // Assignment stays in place

/*
═══════════════════════════════════════════════════════════
HOISTING IS NOT PHYSICALLY MOVING CODE
═══════════════════════════════════════════════════════════

Hoisting is a MENTAL MODEL to explain the behavior.
What actually happens:

CREATION PHASE:
- Scan code for declarations
- Allocate memory for variables and functions
- Initialize var to undefined
- Store functions completely
- Leave let/const uninitialized (TDZ)

EXECUTION PHASE:
- Execute code line by line
- Assignments happen when reached
*/
```

#### **What Gets Hoisted:**

```javascript
function hoistingExample() {
    // What gets hoisted?
    
    console.log(a);  // undefined (var declaration hoisted)
    console.log(b);  // ReferenceError (let in TDZ)
    console.log(c);  // [Function] (function declaration hoisted)
    console.log(d);  // undefined (var, but function expression not hoisted)
    
    var a = 10;
    let b = 20;
    
    function c() {
        return "Function";
    }
    
    var d = function() {
        return "Expression";
    };
}

/*
═══════════════════════════════════════════════════════════
HOISTING CATEGORIES
═══════════════════════════════════════════════════════════

✓ HOISTED AND INITIALIZED:
  - var declarations        → undefined
  - function declarations   → complete function

✓ HOISTED BUT NOT INITIALIZED (TDZ):
  - let declarations        → TDZ
  - const declarations      → TDZ
  - class declarations      → TDZ

✗ NOT HOISTED:
  - Assignments
  - Function expressions
  - Arrow functions
  - Initializers
*/
```

### **7.2 Variable Hoisting (var)**

Variables declared with `var` are hoisted and initialized to `undefined`.

#### **Detailed var Hoisting:**

```javascript
function varHoisting() {
    console.log("1:", x);  // undefined
    console.log("2:", y);  // undefined
    console.log("3:", z);  // undefined
    
    var x;
    var y = 10;
    var z = function() { return "func"; };
    
    console.log("4:", x);  // undefined
    console.log("5:", y);  // 10
    console.log("6:", z);  // [Function]
}

varHoisting();

/*
═══════════════════════════════════════════════════════════
CREATION PHASE - VAR HOISTING
═══════════════════════════════════════════════════════════

Memory State After Creation Phase:
{
    VariableEnvironment: {
        x: undefined,  ← Declared, initialized to undefined
        y: undefined,  ← Declared, initialized to undefined
        z: undefined   ← Declared, initialized to undefined
    }
}

═══════════════════════════════════════════════════════════
EXECUTION PHASE - LINE BY LINE
═══════════════════════════════════════════════════════════

Line 2: console.log("1:", x);
  x exists in memory: undefined
  Output: "1: undefined"

Line 3: console.log("2:", y);
  y exists in memory: undefined
  Output: "2: undefined"

Line 4: console.log("3:", z);
  z exists in memory: undefined
  Output: "3: undefined"

Line 6: var x;
  No-op (already declared in creation phase)

Line 7: var y = 10;
  Assignment: y = 10
  Memory Update: y: undefined → 10

Line 8: var z = function() { ... };
  Assignment: z = <function object>
  Memory Update: z: undefined → <function object>

Line 10: console.log("4:", x);
  x is still undefined (no assignment)
  Output: "4: undefined"

Line 11: console.log("5:", y);
  y is now 10
  Output: "5: 10"

Line 12: console.log("6:", z);
  z is now a function
  Output: "6: [Function]"
*/
```

#### **var Hoisting with Multiple Declarations:**

```javascript
var x = 1;

function test() {
    console.log("1:", x);  // undefined (not 1!)
    
    var x = 2;
    
    console.log("2:", x);  // 2
}

test();
console.log("3:", x);  // 1

/*
═══════════════════════════════════════════════════════════
WHY IS OUTPUT 'undefined' INSTEAD OF 1?
═══════════════════════════════════════════════════════════

Function Execution Context Creation Phase:
{
    VariableEnvironment: {
        x: undefined  ← Local x declared, shadows global x
    },
    outer: <Global Environment>
}

The local 'var x' declaration is hoisted, creating a local
variable that shadows the global x.

EXECUTION PHASE:

Line: console.log("1:", x);
  Identifier Resolution:
    1. Look in function's VariableEnvironment: x = undefined ✓
    2. Don't look in global (local x found)
  Output: "1: undefined"

Line: var x = 2;
  Assignment: x = 2
  Memory Update: Function's x: undefined → 2

Line: console.log("2:", x);
  Output: "2: 2"

Back in Global Context:

Line: console.log("3:", x);
  Global x unchanged
  Output: "3: 1"
*/
```

#### **var Hoisting in Loops:**

```javascript
// Common mistake with var in loops
for (var i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log("Loop var:", i);
    }, 100);
}
// Output: 3, 3, 3 (not 0, 1, 2!)

/*
═══════════════════════════════════════════════════════════
WHY ALL 3's?
═══════════════════════════════════════════════════════════

var is FUNCTION-SCOPED, not block-scoped!

After loop completes:
  Global: { i: 3 }

All three setTimeout callbacks reference the SAME 'i':
  Callback 1: console.log(i) → Global i → 3
  Callback 2: console.log(i) → Global i → 3
  Callback 3: console.log(i) → Global i → 3

SOLUTION 1: Use let (block-scoped)
for (let i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log("Loop let:", i);
    }, 100);
}
// Output: 0, 1, 2 ✓

Each iteration creates new block scope with its own 'i'

SOLUTION 2: IIFE (Immediately Invoked Function Expression)
for (var i = 0; i < 3; i++) {
    (function(j) {
        setTimeout(function() {
            console.log("Loop IIFE:", j);
        }, 100);
    })(i);
}
// Output: 0, 1, 2 ✓

Each IIFE creates new function scope with its own 'j'
*/
```

### **7.3 Variable Hoisting (let and const)**

`let` and `const` are hoisted but remain uninitialized (Temporal Dead Zone).

#### **Detailed let/const Hoisting:**

```javascript
function letConstHoisting() {
    // Temporal Dead Zone (TDZ) starts here for x, y, z
    
    console.log("typeof x:", typeof x);  // ReferenceError
    
    // TDZ continues...
    
    let x = 10;  // TDZ ends for x
    const y = 20;  // TDZ ends for y
    
    console.log("x:", x);  // 10
    console.log("y:", y);  // 20
    
    // y = 30;  // TypeError: Assignment to constant variable
}

/*
═══════════════════════════════════════════════════════════
CREATION PHASE - LET/CONST HOISTING
═══════════════════════════════════════════════════════════

Memory State After Creation Phase:
{
    LexicalEnvironment: {
        x: <uninitialized>,  ← In TDZ
        y: <uninitialized>   ← In TDZ
    }
}

The variables ARE hoisted (memory allocated) but NOT initialized.
Any access before initialization causes ReferenceError.

═══════════════════════════════════════════════════════════
TEMPORAL DEAD ZONE (TDZ)
═══════════════════════════════════════════════════════════

TDZ is the period between:
  START: Entering scope (function/block start)
  END: Variable initialization (let/const declaration line)

Function Start
│
├─ TDZ for x ────────────────────┐
│                                 │
│  Any access to x here          │
│  throws ReferenceError          │
│                                 │
├─ let x = 10; ─────────────────┘ TDZ ends for x
│
├─ TDZ for y ────────────────────┐
│                                 │
├─ const y = 20; ───────────────┘ TDZ ends for y
│
Function End

═══════════════════════════════════════════════════════════
EXECUTION PHASE
═══════════════════════════════════════════════════════════

Line: console.log("typeof x:", typeof x);
  Variable Resolution:
    1. Look in LexicalEnvironment: x = <uninitialized>
    2. x is in TDZ!
  Throw: ReferenceError: Cannot access 'x' before initialization

If we comment out that line:

Line: let x = 10;
  Initialization: x = 10
  TDZ ends for x
  Memory Update: x: <uninitialized> → 10

Line: const y = 20;
  Initialization: y = 20
  TDZ ends for y
  Memory Update: y: <uninitialized> → 20

Line: console.log("x:", x);
  Output: "x: 10"

Line: console.log("y:", y);
  Output: "y: 20"

Line: y = 30;
  Attempt to reassign const
  Throw: TypeError: Assignment to constant variable
*/
```

#### **let/const vs var: Side-by-Side Comparison:**

```javascript
// VAR EXAMPLE
function varExample() {
    console.log("var before:", myVar);  // undefined
    var myVar = 10;
    console.log("var after:", myVar);   // 10
}

// LET EXAMPLE
function letExample() {
    // console.log("let before:", myLet);  // ReferenceError
    let myLet = 20;
    console.log("let after:", myLet);   // 20
}

// CONST EXAMPLE
function constExample() {
    // console.log("const before:", myConst);  // ReferenceError
    const myConst = 30;
    console.log("const after:", myConst);  // 30
    // myConst = 40;  // TypeError
}

/*
═══════════════════════════════════════════════════════════
HOISTING COMPARISON
═══════════════════════════════════════════════════════════

╔══════════════╦════════════╦════════════╦══════════════╗
║   Aspect     ║    var     ║    let     ║    const     ║
╠══════════════╬════════════╬════════════╬══════════════╣
║ Hoisted?     ║    Yes     ║    Yes     ║     Yes      ║
║ Initialized? ║ undefined  ║     No     ║      No      ║
║ TDZ?         ║     No     ║    Yes     ║     Yes      ║
║ Access Before║ undefined  ║ ReferError ║  ReferError  ║
║ Reassignable?║    Yes     ║    Yes     ║      No      ║
║ Redeclarable?║    Yes     ║     No     ║      No      ║
║ Scope        ║  Function  ║   Block    ║    Block     ║
║ Environment  ║  Variable  ║  Lexical   ║   Lexical    ║
╚══════════════╩════════════╩════════════╩══════════════╝

CREATION PHASE MEMORY:

varExample:
{
    VariableEnvironment: {
        myVar: undefined  ← Ready to use (returns undefined)
    }
}

letExample:
{
    LexicalEnvironment: {
        myLet: <uninitialized>  ← NOT ready (throws error)
    }
}

constExample:
{
    LexicalEnvironment: {
        myConst: <uninitialized>  ← NOT ready (throws error)
    }
}
*/
```

### **7.4 Function Declaration Hoisting**

Function declarations are fully hoisted - both name and implementation.

#### **Complete Function Declaration Hoisting:**

```javascript
// Can call before declaration!
console.log(greet());        // "Hello!"
console.log(add(5, 3));      // 8
console.log(multiply(4, 2)); // 8

function greet() {
    return "Hello!";
}

function add(a, b) {
    return a + b;
}

function multiply(x, y) {
    return x * y;
}

/*
═══════════════════════════════════════════════════════════
FUNCTION DECLARATION HOISTING
═══════════════════════════════════════════════════════════

CREATION PHASE:

Global Execution Context:
{
    VariableEnvironment: {
        greet: <function object>,     ← Fully stored
        add: <function object>,        ← Fully stored
        multiply: <function object>    ← Fully stored
    }
}

Function objects contain:
{
    [[Code]]: <function body>,
    [[Scope]]: <lexical environment reference>,
    [[FormalParameters]]: <parameter list>,
    prototype: <prototype object>
}

All functions are IMMEDIATELY available for use!

═══════════════════════════════════════════════════════════
EXECUTION PHASE:
═══════════════════════════════════════════════════════════

Line: console.log(greet());
  1. Resolve 'greet': Found in VariableEnvironment ✓
  2. Check if callable: Yes, it's a function ✓
  3. Create new execution context for greet()
  4. Execute function body
  5. Return "Hello!"
  Output: "Hello!"

Line: console.log(add(5, 3));
  1. Resolve 'add': Found ✓
  2. Create execution context: { a: 5, b: 3 }
  3. Execute: return 5 + 3
  4. Return 8
  Output: 8

Line: console.log(multiply(4, 2));
  1. Resolve 'multiply': Found ✓
  2. Create execution context: { x: 4, y: 2 }
  3. Execute: return 4 * 2
  4. Return 8
  Output: 8

Lines 6-14: Function declarations
  No-op (already in memory from creation phase)
*/
```

#### **Function Hoisting vs Variables:**

```javascript
console.log(typeof foo);  // "function"
console.log(typeof bar);  // "undefined"
console.log(typeof baz);  // ReferenceError

function foo() {
    return "foo";
}

var bar = function() {
    return "bar";
};

let baz = function() {
    return "baz";
};

/*
═══════════════════════════════════════════════════════════
CREATION PHASE ANALYSIS
═══════════════════════════════════════════════════════════

VariableEnvironment:
{
    foo: <function object>,  ← Function declaration: fully hoisted
    bar: undefined           ← var: hoisted, initialized to undefined
}

LexicalEnvironment:
{
    baz: <uninitialized>     ← let: hoisted but in TDZ
}

═══════════════════════════════════════════════════════════
EXECUTION PHASE:
═══════════════════════════════════════════════════════════

Line: console.log(typeof foo);
  foo is a function object
  Output: "function"

Line: console.log(typeof bar);
  bar is undefined
  Output: "undefined"

Line: console.log(typeof baz);
  baz is in TDZ
  Throw: ReferenceError
*/
```

#### **Nested Function Hoisting:**

```javascript
function outer() {
    console.log("1:", inner);  // [Function: inner]
    
    inner();  // "Inner function"
    
    function inner() {
        console.log("Inner function");
    }
    
    console.log("2:", inner);  // [Function: inner]
}

outer();

/*
═══════════════════════════════════════════════════════════
NESTED FUNCTION HOISTING
═══════════════════════════════════════════════════════════

When outer() is called:

CREATION PHASE:
outer Execution Context:
{
    VariableEnvironment: {
        inner: <function object>  ← Hoisted within outer's scope
    }
}

EXECUTION PHASE:

Line: console.log("1:", inner);
  inner already in memory
  Output: "1: [Function: inner]"

Line: inner();
  Call inner function
  Create new execution context for inner()
  Execute: console.log("Inner function");
  Output: "Inner function"
  Destroy inner's execution context

Line: function inner() { ... }
  No-op (already in memory)

Line: console.log("2:", inner);
  Output: "2: [Function: inner]"
*/
```

### **7.5 Function Expression Hoisting**

Function expressions follow variable hoisting rules, not function hoisting rules.

#### **Function Expression Behavior:**

```javascript
// console.log(expression1());  // TypeError: expression1 is not a function
// console.log(expression2());  // ReferenceError

var expression1 = function() {
    return "Expression 1";
};

let expression2 = function() {
    return "Expression 2";
};

console.log(expression1());  // "Expression 1"
console.log(expression2());  // "Expression 2"

/*
═══════════════════════════════════════════════════════════
FUNCTION EXPRESSION HOISTING
═══════════════════════════════════════════════════════════

CREATION PHASE:

VariableEnvironment:
{
    expression1: undefined  ← Variable hoisted, not function!
}

LexicalEnvironment:
{
    expression2: <uninitialized>  ← In TDZ
}

The function objects are NOT created yet!

═══════════════════════════════════════════════════════════
EXECUTION PHASE:
═══════════════════════════════════════════════════════════

Line: console.log(expression1());
  1. Resolve expression1: undefined
  2. Try to call undefined(): TypeError
  
  Why TypeError (not ReferenceError)?
  - expression1 exists (it's undefined)
  - But undefined is not callable
  - TypeError: expression1 is not a function

Line: console.log(expression2());
  1. Resolve expression2: <uninitialized>
  2. In TDZ!
  - ReferenceError: Cannot access before initialization

Line: var expression1 = function() { ... };
  1. Create function object in heap
  2. Assign reference to expression1
  Memory Update: expression1: undefined → <function object>

Line: let expression2 = function() { ... };
  1. Create function object in heap
  2. Initialize expression2 with reference
  3. TDZ ends
  Memory Update: expression2: <uninitialized> → <function object>

Line: console.log(expression1());
  1. Resolve expression1: <function object> ✓
  2. Call function
  3. Return "Expression 1"
  Output: "Expression 1"

Line: console.log(expression2());
  1. Resolve expression2: <function object> ✓
  2. Call function
  3. Return "Expression 2"
  Output: "Expression 2"
*/
```

#### **Named Function Expressions:**

```javascript
console.log(typeof myFunc);  // "undefined"
console.log(typeof funcName);  // "undefined"

var myFunc = function funcName() {
    console.log("Inside:", typeof funcName);  // "function"
    return "result";
};

console.log(myFunc());         // "Inside: function", then "result"
console.log(typeof myFunc);    // "function"
// console.log(funcName());    // ReferenceError

/*
═══════════════════════════════════════════════════════════
NAMED FUNCTION EXPRESSION
═══════════════════════════════════════════════════════════

var myFunc = function funcName() { ... };
                       ^^^^^^^^
                       This name is only visible INSIDE the function!

CREATION PHASE:
{
    VariableEnvironment: {
        myFunc: undefined  ← Only myFunc is hoisted, not funcName
    }
}

EXECUTION PHASE:

After assignment:
  myFunc: <function object>
  
Inside function:
  funcName is accessible (refers to the function itself)
  Useful for recursion!

Outside function:
  funcName is NOT accessible
  
Example: Recursion with named function expression
var factorial = function fact(n) {
    if (n <= 1) return 1;
    return n * fact(n - 1);  ← Can use funcName here!
};

console.log(factorial(5));  // 120 ✓
console.log(fact(5));        // ReferenceError ✗
*/
```

### **7.6 Arrow Function Hoisting**

Arrow functions follow the same hoisting rules as function expressions.

#### **Arrow Function Behavior:**

```javascript
// console.log(arrow1());  // TypeError
// console.log(arrow2());  // ReferenceError

var arrow1 = () => "Arrow 1";
let arrow2 = () => "Arrow 2";
const arrow3 = () => "Arrow 3";

console.log(arrow1());  // "Arrow 1"
console.log(arrow2());  // "Arrow 2"
console.log(arrow3());  // "Arrow 3"

/*
═══════════════════════════════════════════════════════════
ARROW FUNCTION HOISTING
═══════════════════════════════════════════════════════════

CREATION PHASE:

VariableEnvironment:
{
    arrow1: undefined  ← Variable hoisted only
}

LexicalEnvironment:
{
    arrow2: <uninitialized>,  ← TDZ
    arrow3: <uninitialized>   ← TDZ
}

Arrow functions are NOT hoisted!
Only the variable names are hoisted.

═══════════════════════════════════════════════════════════
KEY DIFFERENCES: Arrow vs Regular Functions
═══════════════════════════════════════════════════════════

╔════════════════════╦═══════════════╦═════════════════╗
║     Feature        ║   Regular     ║     Arrow       ║
╠════════════════════╬═══════════════╬═════════════════╣
║ Hoisted?           ║  Yes (decl)   ║      No         ║
║ Own 'this'?        ║     Yes       ║      No         ║
║ Own 'arguments'?   ║     Yes       ║      No         ║
║ Can be constructor?║     Yes       ║      No         ║
║ Own 'super'?       ║     Yes       ║      No         ║
║ Own 'new.target'?  ║     Yes       ║      No         ║
║ Has prototype?     ║     Yes       ║      No         ║
╚════════════════════╩═══════════════╩═════════════════╝

Example: Arrow function 'this' is lexical

const obj = {
    name: "Object",
    
    regularMethod: function() {
        console.log("Regular this:", this.name);  // "Object"
        
        const arrowInside = () => {
            console.log("Arrow this:", this.name);  // "Object"
        };
        arrowInside();
    },
    
    arrowMethod: () => {
        console.log("Arrow method this:", this.name);  // undefined
        // 'this' is from surrounding scope (global)
    }
};

obj.regularMethod();  // Both log "Object"
obj.arrowMethod();    // Logs undefined
*/
```

### **7.7 Class Hoisting**

Classes are hoisted but remain in the Temporal Dead Zone like `let` and `const`.

#### **Class Hoisting Behavior:**

```javascript
// console.log(MyClass);  // ReferenceError
// const instance = new MyClass();  // ReferenceError

class MyClass {
    constructor(name) {
        this.name = name;
    }
    
    greet() {
        console.log(`Hello, ${this.name}`);
    }
}

const instance = new MyClass("John");
instance.greet();  // "Hello, John"

/*
═══════════════════════════════════════════════════════════
CLASS HOISTING
═══════════════════════════════════════════════════════════

CREATION PHASE:

LexicalEnvironment:
{
    MyClass: <uninitialized>  ← In TDZ!
}

Classes are hoisted like let/const, not like function declarations!

═══════════════════════════════════════════════════════════
WHY ARE CLASSES IN TDZ?
═══════════════════════════════════════════════════════════

Reason: To catch errors early

If classes were initialized like function declarations:
  - Could use class before its superclass is defined
  - Could create inconsistent inheritance hierarchies
  - Harder to reason about code flow

TDZ ensures:
  - Classes are fully defined before use
  - Inheritance relationships are clear
  - Errors are caught at declaration time

═══════════════════════════════════════════════════════════
CLASS DECLARATION VS CLASS EXPRESSION
═══════════════════════════════════════════════════════════

// Class Declaration
class DeclarationClass {
    constructor() {}
}

// Class Expression
const ExpressionClass = class {
    constructor() {}
};

// Named Class Expression
const NamedClass = class InternalName {
    constructor() {
        console.log(InternalName);  // Accessible inside
    }
};
// console.log(InternalName);  // ReferenceError - not accessible outside

Both follow let/const hoisting rules (TDZ)!

═══════════════════════════════════════════════════════════
CLASS HOISTING WITH INHERITANCE
═══════════════════════════════════════════════════════════

// This works:
class Parent {
    constructor() {
        this.type = "parent";
    }
}

class Child extends Parent {
    constructor() {
        super();
        this.type = "child";
    }
}

// This doesn't work (TDZ):
class Child extends Parent {  // ReferenceError
    constructor() {
        super();
    }
}

class Parent {
    constructor() {}
}

Because Parent is still in TDZ when Child is declared!
*/
```

### **7.8 Import/Export Hoisting**

Module imports are hoisted to the top of the module scope.

#### **Import Hoisting:**

```javascript
// This works! Imports are hoisted
console.log(add(5, 3));  // 8

import { add } from './math.js';

// This also works!
multiply(4, 2);  // 8

import { multiply } from './math.js';

/*
═══════════════════════════════════════════════════════════
IMPORT HOISTING
═══════════════════════════════════════════════════════════

All import statements are hoisted to the top of the module!

How it's interpreted:
import { add } from './math.js';
import { multiply } from './math.js';

console.log(add(5, 3));
multiply(4, 2);

═══════════════════════════════════════════════════════════
IMPORT HOISTING RULES
═══════════════════════════════════════════════════════════

1. All imports are processed BEFORE any code runs
2. Import bindings are READ-ONLY (constant)
3. Import bindings are LIVE (changes in source reflect)
4. Imports are always at module scope

// math.js
export let count = 0;
export function increment() {
    count++;
}

// app.js
import { count, increment } from './math.js';

console.log(count);  // 0
increment();
console.log(count);  // 1 ← LIVE binding!

// count = 5;  // TypeError: Assignment to constant

═══════════════════════════════════════════════════════════
DEFAULT EXPORTS
═══════════════════════════════════════════════════════════

// utils.js
export default function() {
    return "default";
}

// app.js
// This works (hoisted):
console.log(myFunc());  // "default"

import myFunc from './utils.js';

═══════════════════════════════════════════════════════════
DYNAMIC IMPORTS (NOT HOISTED)
═══════════════════════════════════════════════════════════

// These are NOT hoisted (they're expressions):

if (condition) {
    import('./module.js')  // Returns a Promise
        .then(module => {
            module.doSomething();
        });
}

async function loadModule() {
    const module = await import('./module.js');
    module.doSomething();
}
*/
```

### **7.9 Hoisting Priority and Precedence**

When multiple declarations with the same name exist, there's a priority order.

#### **Declaration Priority:**

```javascript
console.log(foo);  // [Function: foo]

function foo() {
    return "function";
}

var foo = "variable";

console.log(foo);  // "variable"

/*
═══════════════════════════════════════════════════════════
HOISTING PRIORITY
═══════════════════════════════════════════════════════════

CREATION PHASE (Priority Order):

1. Function parameters (if in function scope)
2. Function declarations
3. Variable declarations (var)

Process:
Step 1: Scan for function declarations
  foo: <function object>

Step 2: Scan for variable declarations
  foo: already exists, skip creating new binding
  (Only ONE foo in memory)

Memory State:
{
    foo: <function object>  ← Function takes priority
}

EXECUTION PHASE:

Line: console.log(foo);
  foo is <function object>
  Output: [Function: foo]

Line: function foo() { ... }
  No-op (already in memory)

Line: var foo = "variable";
  Assignment: foo = "variable"
  Memory Update: foo: <function object> → "variable"

Line: console.log(foo);
  foo is now "variable"
  Output: "variable"

═══════════════════════════════════════════════════════════
RULE: Function Declarations Trump Variable Declarations
      But Assignments Still Happen!
═══════════════════════════════════════════════════════════
*/
```

#### **Complex Priority Example:**

```javascript
var a = 1;
function a() {}
console.log(typeof a);  // "number"

function b() {}
var b = 2;
console.log(typeof b);  // "number"

function c() {}
var c;
console.log(typeof c);  // "function"

/*
═══════════════════════════════════════════════════════════
DETAILED ANALYSIS
═══════════════════════════════════════════════════════════

Example 1: var a = 1; function a() {}
───────────────────────────────────────

CREATION PHASE:
1. Function declaration: a = <function object>
2. Variable declaration: a already exists, skip

EXECUTION PHASE:
Line: var a = 1;
  Assignment: a = 1
  Memory: a: <function object> → 1

Line: function a() {}
  No-op

Line: console.log(typeof a);
  a is 1 (number)
  Output: "number"

Example 2: function b() {} var b = 2;
───────────────────────────────────────

CREATION PHASE:
1. Function declaration: b = <function object>
2. Variable declaration: b already exists, skip

EXECUTION PHASE:
Line: function b() {}
  No-op

Line: var b = 2;
  Assignment: b = 2
  Memory: b: <function object> → 2

Line: console.log(typeof b);
  b is 2 (number)
  Output: "number"

Example 3: function c() {} var c;
───────────────────────────────────

CREATION PHASE:
1. Function declaration: c = <function object>
2. Variable declaration: c already exists, skip

EXECUTION PHASE:
Line: function c() {}
  No-op

Line: var c;
  Just declaration, no assignment
  Memory: c: <function object> (unchanged!)

Line: console.log(typeof c);
  c is still <function object>
  Output: "function"
*/
```

### **7.10 Common Hoisting Pitfalls**

#### **Pitfall 1: Variable Shadowing**

```javascript
var value = "global";

function test() {
    console.log(value);  // undefined (not "global"!)
    
    if (true) {
        var value = "local";
    }
    
    console.log(value);  // "local"
}

test();

/*
═══════════════════════════════════════════════════════════
PITFALL EXPLANATION
═══════════════════════════════════════════════════════════

var is FUNCTION-SCOPED, not block-scoped!

How JavaScript interprets this:

function test() {
    var value;  ← Hoisted to function top, shadows global!
    
    console.log(value);  // undefined (local value)
    
    if (true) {
        value = "local";  // Assignment to local value
    }
    
    console.log(value);  // "local"
}

The global 'value' is NEVER accessed inside test()!

═══════════════════════════════════════════════════════════
FIX: Use let/const (block-scoped)
═══════════════════════════════════════════════════════════

function testFixed() {
    console.log(value);  // "global" ✓
    
    if (true) {
        let value = "local";  // Block-scoped
        console.log(value);   // "local"
    }
    
    console.log(value);  // "global" ✓
}
*/
```

#### **Pitfall 2: Loop Variables**

```javascript
var funcs = [];

for (var i = 0; i < 3; i++) {
    funcs.push(function() {
        console.log(i);
    });
}

funcs[0]();  // 3 (not 0!)
funcs[1]();  // 3 (not 1!)
funcs[2]();  // 3 (not 2!)

/*
═══════════════════════════════════════════════════════════
PITFALL EXPLANATION
═══════════════════════════════════════════════════════════

var i is hoisted to function/global scope!

After loop completes:
  i = 3

All three functions close over the SAME 'i':

funcs[0]:  closure → i (= 3)
funcs[1]:  closure → i (= 3)
funcs[2]:  closure → i (= 3)

═══════════════════════════════════════════════════════════
FIX 1: Use let (block-scoped)
═══════════════════════════════════════════════════════════

var funcs = [];

for (let i = 0; i < 3; i++) {  ← let instead of var
    funcs.push(function() {
        console.log(i);
    });
}

funcs[0]();  // 0 ✓
funcs[1]();  // 1 ✓
funcs[2]();  // 2 ✓

Each iteration creates new block scope with its own 'i'!

═══════════════════════════════════════════════════════════
FIX 2: IIFE
═══════════════════════════════════════════════════════════

var funcs = [];

for (var i = 0; i < 3; i++) {
    (function(j) {  ← IIFE with parameter
        funcs.push(function() {
            console.log(j);
        });
    })(i);  ← Pass current i value
}

funcs[0]();  // 0 ✓
funcs[1]();  // 1 ✓
funcs[2]();  // 2 ✓
*/
```

#### **Pitfall 3: Conditional Function Declarations**

```javascript
console.log(typeof foo);  // ?

if (true) {
    function foo() {
        return "inside if";
    }
}

console.log(typeof foo);  // ?

/*
═══════════════════════════════════════════════════════════
PITFALL: NON-STANDARD BEHAVIOR
═══════════════════════════════════════════════════════════

Function declarations inside blocks are NOT standardized
in ES5 and earlier!

Different browsers behave differently:
- Some hoist to function scope
- Some treat as block-scoped
- Some hoist but initialize in block

ES6+ standardizes: Block-scoped (like let)

Best Practice: NEVER use function declarations in blocks!

═══════════════════════════════════════════════════════════
CORRECT APPROACH
═══════════════════════════════════════════════════════════

// Option 1: Function expression with let/const
let foo;
if (true) {
    foo = function() {
        return "inside if";
    };
}

// Option 2: Declare at function scope
function foo() {
    return "default";
}

if (condition) {
    foo = function() {
        return "overridden";
    };
}
*/
```

#### **Pitfall 4: Missing Declarations**

```javascript
function test() {
    value = 10;  // Forgot var/let/const!
    console.log(value);  // 10
}

test();
console.log(window.value);  // 10 (Oops! Global variable!)

/*
═══════════════════════════════════════════════════════════
PITFALL: ACCIDENTAL GLOBALS
═══════════════════════════════════════════════════════════

Without var/let/const, assignment creates GLOBAL variable!

Process:
1. Look for 'value' in current scope: NOT FOUND
2. Look in outer scopes: NOT FOUND
3. Reach global scope: NOT FOUND
4. Non-strict mode: CREATE GLOBAL VARIABLE
   Strict mode: ReferenceError ✓

═══════════════════════════════════════════════════════════
FIX: Always Use Declarations + Strict Mode
═══════════════════════════════════════════════════════════

'use strict';

function test() {
    value = 10;  // ReferenceError: value is not defined ✓
}

Or:

function test() {
    let value = 10;  // Local variable ✓
    console.log(value);
}

test();
console.log(window.value);  // undefined ✓
*/
```

---

## **8. TEMPORAL DEAD ZONE (TDZ)**

### **8.1 Understanding TDZ**

The **Temporal Dead Zone** is the time between entering a scope and a variable being initialized.

#### **What is TDZ?**

```javascript
function tdzExample() {
    // TDZ starts here for 'x'
    // ─────────────────────────────────
    
    console.log("Before declaration");
    
    // Still in TDZ for 'x'
    // console.log(x);  // ReferenceError
    
    // Still in TDZ for 'x'
    // let y = x;  // ReferenceError
    
    // TDZ ends here when initialization happens
    // ─────────────────────────────────
    let x = 10;
    
    console.log(x);  // 10 - Now accessible
}

tdzExample();

/*
═══════════════════════════════════════════════════════════
TDZ TIMELINE
═══════════════════════════════════════════════════════════

Function Entry (Scope Entry)
│
├─ CREATION PHASE
│  Memory allocated: x = <uninitialized>
│
├─ EXECUTION PHASE BEGINS
│
├─ TDZ STARTS ←─────────┐
│                        │
│  console.log("Before") │ Any access to 'x'
│  ✓ Works               │ throws ReferenceError
│                        │
│  console.log(x)        │
│  ✗ ReferenceError      │
│                        │
│  let y = x             │
│  ✗ ReferenceError      │
│                        │
├─ let x = 10; ←─────────┘ TDZ ENDS
│
│  console.log(x)
│  ✓ Works (x = 10)
│
Function Exit

═══════════════════════════════════════════════════════════
KEY INSIGHT
═══════════════════════════════════════════════════════════

TDZ is NOT about hoisting vs no hoisting!
- let/const ARE hoisted (memory allocated)
- But they're NOT initialized
- They remain in TDZ until declaration line is reached

var IS initialized (to undefined) during creation phase
let/const are NOT initialized during creation phase
*/
```

### **8.2 TDZ in Different Scenarios**

#### **Scenario 1: typeof in TDZ**

```javascript
// typeof with undeclared variable: safe
console.log(typeof undeclaredVariable);  // "undefined"

// typeof with TDZ variable: ReferenceError!
console.log(typeof declaredLater);  // ReferenceError!
let declaredLater = 10;

/*
═══════════════════════════════════════════════════════════
WHY DIFFERENT BEHAVIOR?
═══════════════════════════════════════════════════════════

undeclaredVariable:
  - Not in any environment
  - typeof returns "undefined" (safe)

declaredLater:
  - In LexicalEnvironment: <uninitialized>
  - In TDZ!
  - Any access (even typeof) throws error

This is INTENTIONAL design:
- Catch potential bugs early
- Make TDZ violations explicit
- Encourage declaring variables at top of scope
*/
```

#### **Scenario 2: Default Parameters and TDZ**

```javascript
function withDefaults(a = b, b = 2) {
    console.log(a, b);
}

withDefaults();  // ReferenceError!

/*
═══════════════════════════════════════════════════════════
EXPLANATION
═══════════════════════════════════════════════════════════

Parameter initialization happens left-to-right:

Step 1: Initialize 'a'
  a = b  ← But 'b' is in TDZ!
  ReferenceError: Cannot access 'b' before initialization

Parameters create their own scope (like let/const):

function withDefaults(a = b, b = 2) {
  // Parameter scope:
  // a: <uninitialized>
  // b: <uninitialized>
  
  // Try to initialize a with b (which is in TDZ)
  // ERROR!
}

═══════════════════════════════════════════════════════════
CORRECT ORDER
═══════════════════════════════════════════════════════════

function withDefaults(b = 2, a = b) {
    console.log(a, b);
}

withDefaults();  // 2, 2 ✓

Process:
1. Initialize b = 2
2. Initialize a = b (b is already initialized) ✓
*/
```

#### **Scenario 3: TDZ in Loops**

```javascript
// Example 1: for loop
for (let i = 0; i < 3; i++) {
    console.log(i);  // 0, 1, 2
}
// console.log(i);  // ReferenceError (block-scoped)

// Example 2: TDZ within loop body
for (let i = 0; i < 3; i++) {
    // console.log(x);  // ReferenceError (TDZ)
    let x = i * 2;
    console.log(x);  // 0, 2, 4
}

/*
═══════════════════════════════════════════════════════════
TDZ IN LOOP ITERATIONS
═══════════════════════════════════════════════════════════

Each iteration creates NEW block scope with NEW 'i':

Iteration 0:
┌──────────────────────────┐
│ Block Scope 0            │
│ i: 0 (initialized)       │
│ x: <uninitialized> ← TDZ │
│ ...                      │
│ let x = i * 2;           │
│ x: 0 (TDZ ends)          │
└──────────────────────────┘

Iteration 1:
┌──────────────────────────┐
│ Block Scope 1            │
│ i: 1 (initialized)       │
│ x: <uninitialized> ← TDZ │
│ ...                      │
│ let x = i * 2;           │
│ x: 2 (TDZ ends)          │
└──────────────────────────┘

Each 'x' has its own TDZ per iteration!
*/
```

#### **Scenario 4: Class TDZ**

```javascript
// console.log(MyClass);  // ReferenceError

class MyClass {
    constructor(value) {
        this.value = value;
    }
}

console.log(MyClass);  // [class MyClass]

// Inheritance with TDZ
class Child extends Parent {  // ReferenceError!
    constructor() {
        super();
    }
}

class Parent {
    constructor() {
        this.type = "parent";
    }
}

/*
═══════════════════════════════════════════════════════════
CLASS TDZ
═══════════════════════════════════════════════════════════

Classes are in TDZ just like let/const:

LexicalEnvironment:
{
    MyClass: <uninitialized>  ← TDZ
}

After declaration:
{
    MyClass: <class object>
}

═══════════════════════════════════════════════════════════
INHERITANCE ISSUE
═══════════════════════════════════════════════════════════

class Child extends Parent {  // Parent in TDZ!
    ...
}

class Parent {
    ...
}

Fix: Declare parent before child

class Parent {
    ...
}

class Child extends Parent {  ✓
    ...
}
*/
```

### **8.3 Why TDZ Exists**

#### **Reason 1: Catch Errors Early**

```javascript
// Without TDZ (like var):
function withVar() {
    console.log(count);  // undefined - bug goes unnoticed!
    // ... 100 lines of code ...
    var count = 10;
}

// With TDZ (let/const):
function withLet() {
    console.log(count);  // ReferenceError - bug caught immediately!
    // ... 100 lines of code ...
    let count = 10;
}

/*
TDZ makes bugs explicit and immediate:
- Accessing before initialization: ERROR
- Typos in variable names: ERROR
- Unintended early access: ERROR

This is BETTER for code quality!
*/
```

#### **Reason 2: const Semantics**

```javascript
// const must be initialized at declaration
const x = 10;  // ✓
// const y;     // ✗ SyntaxError

/*
If const wasn't in TDZ:

const x;  // What would x be? undefined?
x = 10;   // Can we assign to const?

TDZ enforces const semantics:
- Must initialize at declaration
- Value known before use
- No undefined state
*/
```

#### **Reason 3: Consistent Behavior**

```javascript
// let and const behave consistently
let x = 10;
const y = 20;

// Both:
// - Block-scoped
// - In TDZ before declaration
// - Cannot be redeclared
// - Not attached to global object

// Only difference: const can't be reassigned
x = 15;  // ✓
// y = 25;  // ✗ TypeError
```

### **8.4 TDZ with Function Parameters**

#### **Parameter Scope and TDZ:**

```javascript
function parameterTDZ(a = 1, b = a, c = d, d = 2) {
    console.log(a, b, c, d);
}

parameterTDZ();  // ReferenceError

/*
═══════════════════════════════════════════════════════════
PARAMETER INITIALIZATION ORDER
═══════════════════════════════════════════════════════════

Parameters initialize LEFT TO RIGHT:

Step 1: a = 1
  ✓ Literal value, no problem

Step 2: b = a
  ✓ 'a' already initialized

Step 3: c = d
  ✗ 'd' is in TDZ!
  ReferenceError

═══════════════════════════════════════════════════════════
PARAMETER SCOPE IS SEPARATE
═══════════════════════════════════════════════════════════

function example(x = y, y = 2) {
    console.log(x, y);
}

// Not the same as:
function example() {
    let x = y;  // Can't access y yet
    let y = 2;
}

Parameters have their own initialization scope!
*/
```

#### **Advanced Parameter TDZ:**

```javascript
let x = "outer";

function test(y = x, x = 5) {
    console.log(y, x);
}

test();  // ReferenceError

/*
═══════════════════════════════════════════════════════════
DETAILED ANALYSIS
═══════════════════════════════════════════════════════════

Parameter Scope:
┌─────────────────────────────────────┐
│ y: <uninitialized>                  │
│ x: <uninitialized>                  │
└─────────────────────────────────────┘
     │
     ↓ outer scope
┌─────────────────────────────────────┐
│ Function Scope                      │
│ (empty)                             │
└─────────────────────────────────────┘
     │
     ↓ outer scope
┌─────────────────────────────────────┐
│ Global Scope                        │
│ x: "outer"                          │
└─────────────────────────────────────┘

Initialization:
1. Initialize y = x
   - Look for x in parameter scope: <uninitialized> (TDZ!)
   - DON'T look in outer scopes yet!
   - ReferenceError

Why not use outer x?
- Parameter x shadows outer x
- Even though parameter x isn't initialized yet
- This is the SAME NAME SHADOWING rule as:

function test() {
    console.log(x);  // ReferenceError
    let x = 5;
}
let x = "outer";
test();

═══════════════════════════════════════════════════════════
CORRECT VERSION
═══════════════════════════════════════════════════════════

let outer = "outer";

function test(x = 5, y = outer) {
    console.log(y, x);
}

test();  // "outer", 5 ✓

Or use different parameter names:

function test(y = x, z = 5) {
    console.log(y, z);
}
let x = "outer";
test();  // "outer", 5 ✓
*/
```

### **8.5 TDZ in Loops**

#### **for Loop TDZ:**

```javascript
// Correct: let in for loop
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100);
}
// Output: 0, 1, 2

// Incorrect: var in for loop
for (var j = 0; j < 3; j++) {
    setTimeout(() => console.log(j), 100);
}
// Output: 3, 3, 3

/*
═══════════════════════════════════════════════════════════
HOW let CREATES NEW SCOPE PER ITERATION
═══════════════════════════════════════════════════════════

for (let i = 0; i < 3; i++) {
    // Each iteration:
}

Is similar to:
{
    let i = 0;
    {
        // Iteration 0: new binding for i = 0
        setTimeout(() => console.log(i), 100);
    }
    i++;
    {
        // Iteration 1: new binding for i = 1
        setTimeout(() => console.log(i), 100);
    }
    i++;
    {
        // Iteration 2: new binding for i = 2
        setTimeout(() => console.log(i), 100);
    }
}

═══════════════════════════════════════════════════════════
BLOCK SCOPE PER ITERATION
═══════════════════════════════════════════════════════════

Iteration 0:
┌──────────────────────────┐
│ i: 0                     │ ← Separate 'i'
│ setTimeout closes over   │
│ THIS specific i          │
└──────────────────────────┘

Iteration 1:
┌──────────────────────────┐
│ i: 1                     │ ← Different 'i'
│ setTimeout closes over   │
│ THIS specific i          │
└──────────────────────────┘

Iteration 2:
┌──────────────────────────┐
│ i: 2                     │ ← Yet another 'i'
│ setTimeout closes over   │
│ THIS specific i          │
└──────────────────────────┘

With var (function-scoped):
┌──────────────────────────┐
│ j: 3 (after loop)        │ ← SAME 'j'
│ All three setTimeouts    │
│ close over SAME j        │
└──────────────────────────┘
*/
```

### **8.6 TDZ Best Practices**

#### **Best Practice 1: Declare at Top of Scope**

```javascript
// Bad: Declarations scattered
function scattered() {
    console.log("Starting...");
    doSomething();
    let x = 10;
    doMore();
    const y = 20;
    finish();
}

// Good: Declarations at top
function organized() {
    let x = 10;
    const y = 20;
    
    console.log("Starting...");
    doSomething();
    doMore();
    finish();
}

/*
Benefits:
1. No TDZ surprises
2. Easy to see all variables at a glance
3. Clear initialization order
4. Follows scope-based thinking
*/
```

#### **Best Practice 2: Initialize When Declaring**

```javascript
// Bad: Declaration without initialization
let x;
// ... 50 lines of code ...
x = calculateValue();

// Good: Declare and initialize together
let x = calculateValue();

/*
Benefits:
1. Shorter TDZ (or none at all)
2. Clearer code intent
3. Easier to track variable state
4. Less chance of using uninitialized variable
*/
```

#### **Best Practice 3: Use const by Default**

```javascript
// Prefer const
const PI = 3.14159;
const user = { name: "John" };
const items = [1, 2, 3];

// Use let only when reassignment needed
let counter = 0;
counter++;

// Avoid var
// var oldStyle = "avoid";

/*
Benefits:
1. const has shortest TDZ (initialization required)
2. Signals immutable binding
3. Prevents accidental reassignment
4. More modern and maintainable code

Progression:
const > let > var
(best)  (ok)  (avoid)
*/
```

---

# **PART 4: SCOPE AND SCOPE CHAIN**

## **9. SCOPE IN JAVASCRIPT**

### **9.1 What is Scope?**

**Scope** determines the accessibility (visibility) of variables, functions, and objects in some particular part of your code during runtime.

#### **Fundamental Scope Concept:**

```javascript
// Scope defines: "Where can I access this variable?"

let globalVar = "I'm global";

function outer() {
    let outerVar = "I'm in outer";
    
    function inner() {
        let innerVar = "I'm in inner";
        
        console.log(innerVar);   // ✓ Can access (own scope)
        console.log(outerVar);   // ✓ Can access (parent scope)
        console.log(globalVar);  // ✓ Can access (global scope)
    }
    
    inner();
    console.log(innerVar);  // ✗ Cannot access (not in scope)
}

outer();
console.log(outerVar);  // ✗ Cannot access (not in scope)

/*
═══════════════════════════════════════════════════════════
SCOPE HIERARCHY
═══════════════════════════════════════════════════════════

Global Scope
├─ globalVar: "I'm global"
│
└─ outer() Scope
   ├─ outerVar: "I'm in outer"
   │
   └─ inner() Scope
      └─ innerVar: "I'm in inner"

Access Rules:
- Inner can access outer ✓
- Outer CANNOT access inner ✗
- All can access global ✓

This is called LEXICAL SCOPING
(scope determined by code structure)
*/
```

#### **Scope vs Context vs Environment:**

```javascript
/*
═══════════════════════════════════════════════════════════
THREE RELATED BUT DIFFERENT CONCEPTS
═══════════════════════════════════════════════════════════

1. SCOPE
   - WHAT variables are accessible
   - Determined at WRITE TIME (lexical)
   - About VISIBILITY
   
2. CONTEXT (this)
   - WHICH object a function belongs to
   - Determined at RUN TIME (dynamic)
   - About OBJECT REFERENCE
   
3. EXECUTION CONTEXT
   - ENVIRONMENT where code executes
   - Contains scope, this, variables
   - About EXECUTION ENVIRONMENT
*/

// Example showing all three:
const obj = {
    name: "Object",
    outer: function() {
        let outerVar = "outer";  // SCOPE: outer function
        
        function inner() {
            let innerVar = "inner";  // SCOPE: inner function
            
            console.log("Scope:", outerVar, innerVar);
            console.log("Context (this):", this);
            console.log("In Execution Context: inner()");
            
            // SCOPE: Can access outerVar (parent scope)
            // CONTEXT: 'this' is global (not obj)
            // EXECUTION CONTEXT: inner's execution environment
        }
        
        inner();
    }
};

obj.outer();

/*
Output Analysis:

Scope: outer inner
  ✓ Can access both variables via scope chain

Context (this): Window (or global)
  ✓ inner() called as regular function (not method)
  ✓ 'this' is not obj (that was outer's this)

In Execution Context: inner()
  ✓ Currently executing in inner's execution context
  ✓ Separate from outer's execution context
*/
```

### **9.2 Global Scope**

Variables declared outside any function or block are in the **global scope**.

#### **Global Scope Characteristics:**

```javascript
// These are all in GLOBAL SCOPE
var globalVar = "var global";
let globalLet = "let global";
const globalConst = "const global";

function globalFunction() {
    return "global function";
}

class GlobalClass {
    constructor() {
        this.type = "global class";
    }
}

// Accessing global scope
console.log(globalVar);      // ✓ Accessible
console.log(globalLet);      // ✓ Accessible
console.log(globalConst);    // ✓ Accessible
console.log(globalFunction()); // ✓ Accessible
console.log(new GlobalClass()); // ✓ Accessible

/*
═══════════════════════════════════════════════════════════
GLOBAL SCOPE IN DIFFERENT ENVIRONMENTS
═══════════════════════════════════════════════════════════

BROWSER:
--------
- Global object: window
- var creates properties on window
- let/const do NOT create properties on window

console.log(window.globalVar);   // "var global" ✓
console.log(window.globalLet);   // undefined ✗
console.log(window.globalConst); // undefined ✗

NODE.JS:
--------
- Global object: global
- But top-level code runs in module scope!
- Nothing automatically becomes global

// In Node.js module:
var x = 10;
console.log(global.x);  // undefined

// To make truly global in Node.js:
global.x = 10;
console.log(global.x);  // 10

WEB WORKER:
-----------
- Global object: self
- No access to DOM (no window)

console.log(self);
console.log(typeof window);  // "undefined"

UNIVERSAL:
----------
- globalThis (ES2020): works everywhere

console.log(globalThis);  // Window, global, or self
*/
```

#### **Global Scope and Variable Shadowing:**

```javascript
var x = "global x";
let y = "global y";

function test() {
    // Local variables SHADOW global variables
    var x = "local x";
    let y = "local y";
    
    console.log(x);  // "local x" (shadows global x)
    console.log(y);  // "local y" (shadows global y)
    
    // Accessing global variables when shadowed
    console.log(window.x);  // "global x" (if var in browser)
    // No direct way to access shadowed let/const!
}

test();

console.log(x);  // "global x"
console.log(y);  // "global y"

/*
═══════════════════════════════════════════════════════════
SHADOWING RULES
═══════════════════════════════════════════════════════════

When a local variable has the same name as outer variable:
1. Local variable SHADOWS (hides) outer variable
2. Inside function, only local variable is accessible
3. Outer variable unaffected
4. After function ends, outer variable accessible again

Scope Resolution:
─────────────────
function test() {
    let x = "local";
    console.log(x);
    
    // JavaScript looks for 'x':
    // 1. Current scope (function test): FOUND x = "local" ✓
    // 2. Stop searching (doesn't look in global scope)
}

Visual Representation:
──────────────────────
┌─────────────────────────────┐
│ Global Scope                │
│ x: "global x"               │
│ y: "global y"               │
│                             │
│ ┌─────────────────────────┐ │
│ │ test() Scope            │ │
│ │ x: "local x"  ← Shadows │ │
│ │ y: "local y"  ← Shadows │ │
│ │                         │ │
│ │ console.log(x)          │ │
│ │ → Finds local x first   │ │
│ │ → Global x hidden       │ │
│ └─────────────────────────┘ │
└─────────────────────────────┘
*/
```

#### **Global Scope Pollution (Anti-Pattern):**

```javascript
// BAD: Polluting global scope
var config = { /* ... */ };
var utils = { /* ... */ };
var data = [];
var counter = 0;
var isActive = false;

function helper1() { /* ... */ }
function helper2() { /* ... */ }
function helper3() { /* ... */ }

// Everything is global! Naming conflicts likely!

/*
═══════════════════════════════════════════════════════════
PROBLEMS WITH GLOBAL SCOPE POLLUTION
═══════════════════════════════════════════════════════════

1. NAMING CONFLICTS
   - Different libraries might use same names
   - Hard to track where variables are defined
   - Accidental overwrites

2. MEMORY ISSUES
   - Global variables never garbage collected
   - Persist for entire application lifetime
   - Memory leaks

3. MAINTAINABILITY
   - Hard to understand dependencies
   - Difficult to refactor
   - Tight coupling

4. TESTING
   - Hard to isolate and test
   - Global state causes side effects
   - Unpredictable behavior

═══════════════════════════════════════════════════════════
SOLUTIONS
═══════════════════════════════════════════════════════════
*/

// SOLUTION 1: Module Pattern
const MyApp = (function() {
    // Private variables (not global)
    let config = { /* ... */ };
    let data = [];
    let counter = 0;
    
    // Private functions
    function helper1() { /* ... */ }
    function helper2() { /* ... */ }
    
    // Public API (only this is global)
    return {
        init: function() { /* ... */ },
        getData: function() { return data; },
        increment: function() { counter++; }
    };
})();

// Only 'MyApp' is global
console.log(typeof MyApp);  // "object"
console.log(typeof config);  // "undefined" ✓

// SOLUTION 2: ES6 Modules
// app.js
export const config = { /* ... */ };
export function helper() { /* ... */ }

// main.js
import { config, helper } from './app.js';
// Variables are module-scoped, not global!

// SOLUTION 3: Namespacing
const MyNamespace = {
    config: { /* ... */ },
    utils: { /* ... */ },
    helpers: {
        helper1() { /* ... */ },
        helper2() { /* ... */ }
    }
};

// Only 'MyNamespace' is global
console.log(MyNamespace.config);
console.log(MyNamespace.helpers.helper1());
```

### **9.3 Function Scope**

Variables declared inside a function are in **function scope** (also called local scope).

#### **Function Scope Basics:**

```javascript
function functionScope() {
    // All these are function-scoped
    var functionVar = "function scoped";
    let functionLet = "also function scoped";
    const functionConst = "also function scoped";
    
    function innerFunction() {
        return "nested function";
    }
    
    console.log(functionVar);    // ✓ Accessible
    console.log(functionLet);    // ✓ Accessible
    console.log(functionConst);  // ✓ Accessible
    console.log(innerFunction()); // ✓ Accessible
}

functionScope();

// None accessible outside function
console.log(typeof functionVar);    // "undefined"
console.log(typeof functionLet);    // "undefined"
console.log(typeof functionConst);  // "undefined"
console.log(typeof innerFunction);  // "undefined"

/*
═══════════════════════════════════════════════════════════
FUNCTION SCOPE VISUALIZATION
═══════════════════════════════════════════════════════════

┌─────────────────────────────────────────┐
│ Global Scope                            │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ functionScope() Scope               │ │
│ │                                     │ │
│ │ functionVar: "function scoped"      │ │
│ │ functionLet: "also function scoped" │ │
│ │ functionConst: "also function..."   │ │
│ │ innerFunction: <function>           │ │
│ │                                     │ │
│ │ All variables ONLY accessible here  │ │
│ │ Not visible from Global Scope       │ │
│ └─────────────────────────────────────┘ │
│                                         │
└─────────────────────────────────────────┘

Key Point: var, let, and const ALL create function-scoped
           variables when declared in a function.
*/
```

#### **Function Scope with Nested Functions:**

```javascript
function outer() {
    var outerVar = "outer";
    
    function middle() {
        var middleVar = "middle";
        
        function inner() {
            var innerVar = "inner";
            
            // Can access all parent scopes
            console.log(innerVar);   // ✓ Own scope
            console.log(middleVar);  // ✓ Parent scope
            console.log(outerVar);   // ✓ Grandparent scope
        }
        
        inner();
        console.log(innerVar);  // ✗ ReferenceError
    }
    
    middle();
    console.log(middleVar);  // ✗ ReferenceError
}

outer();
console.log(outerVar);  // ✗ ReferenceError

/*
═══════════════════════════════════════════════════════════
NESTED FUNCTION SCOPE HIERARCHY
═══════════════════════════════════════════════════════════

┌──────────────────────────────────────────┐
│ outer() Scope                            │
│ outerVar: "outer"                        │
│                                          │
│ ┌──────────────────────────────────────┐ │
│ │ middle() Scope                       │ │
│ │ middleVar: "middle"                  │ │
│ │                                      │ │
│ │ ┌────────────────────────────────┐   │ │
│ │ │ inner() Scope                  │   │ │
│ │ │ innerVar: "inner"              │   │ │
│ │ │                                │   │ │
│ │ │ Access:                        │   │ │
│ │ │ ✓ innerVar (own)               │   │ │
│ │ │ ✓ middleVar (parent)           │   │ │
│ │ │ ✓ outerVar (grandparent)       │   │ │
│ │ └────────────────────────────────┘   │ │
│ │                                      │ │
│ │ Access:                              │ │
│ │ ✓ middleVar (own)                    │ │
│ │ ✓ outerVar (parent)                  │ │
│ │ ✗ innerVar (not accessible)          │ │
│ └──────────────────────────────────────┘ │
│                                          │
│ Access:                                  │
│ ✓ outerVar (own)                         │
│ ✗ middleVar (not accessible)             │
│ ✗ innerVar (not accessible)              │
└──────────────────────────────────────────┘

Rule: Child scopes can access parent scopes (up)
      Parent scopes CANNOT access child scopes (down)
*/
```

#### **Function Scope vs Block Scope (var vs let/const):**

```javascript
function scopeComparison() {
    // var is function-scoped
    if (true) {
        var functionScoped = "var leaks out";
    }
    console.log(functionScoped);  // ✓ "var leaks out"
    
    // let/const are block-scoped
    if (true) {
        let blockScoped = "let stays in";
        const alsoBlock = "const stays in";
    }
    // console.log(blockScoped);  // ✗ ReferenceError
    // console.log(alsoBlock);    // ✗ ReferenceError
}

scopeComparison();

/*
═══════════════════════════════════════════════════════════
SCOPE COMPARISON
═══════════════════════════════════════════════════════════

VAR (Function-scoped):
──────────────────────
function scopeComparison() {
    // var is hoisted to function top
    var functionScoped;
    
    if (true) {
        functionScoped = "var leaks out";
    }
    console.log(functionScoped);  // ✓ Accessible
}

Visual:
┌─────────────────────────────────┐
│ scopeComparison() Scope         │
│ functionScoped: "var leaks out" │ ← Hoisted here
│                                 │
│ ┌─────────────────────────────┐ │
│ │ if block                    │ │
│ │ (no new scope for var)      │ │
│ │ functionScoped assigned     │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘

LET/CONST (Block-scoped):
──────────────────────────
function scopeComparison() {
    if (true) {
        let blockScoped = "let stays in";
        const alsoBlock = "const stays in";
    }
    // Not accessible here!
}

Visual:
┌─────────────────────────────────┐
│ scopeComparison() Scope         │
│ (blockScoped not here!)         │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ if block scope              │ │
│ │ blockScoped: "let stays in" │ │
│ │ alsoBlock: "const stays in" │ │
│ │ Only accessible here!       │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
*/
```

#### **Function Parameters and Scope:**

```javascript
function withParameters(param1, param2) {
    console.log(param1);  // ✓ Parameters are function-scoped
    console.log(param2);  // ✓ Accessible anywhere in function
    
    var localVar = "local";
    
    if (true) {
        // Parameters accessible in nested blocks too
        console.log(param1);  // ✓ Accessible
        console.log(localVar); // ✓ Accessible
    }
    
    function nested() {
        // Parameters accessible in nested functions
        console.log(param1);  // ✓ Accessible
        console.log(param2);  // ✓ Accessible
    }
    
    nested();
}

withParameters("arg1", "arg2");
// console.log(param1);  // ✗ ReferenceError

/*
═══════════════════════════════════════════════════════════
PARAMETER SCOPE
═══════════════════════════════════════════════════════════

Parameters are treated as local variables:

function withParameters(param1, param2) {
    // Effectively like:
    // var param1 = "arg1";
    // var param2 = "arg2";
}

┌─────────────────────────────────────┐
│ withParameters() Scope              │
│ param1: "arg1"  ← Function-scoped   │
│ param2: "arg2"  ← Function-scoped   │
│ localVar: "local"                   │
│                                     │
│ ┌─────────────────────────────────┐ │
│ │ if block                        │ │
│ │ Can access param1, param2       │ │
│ └─────────────────────────────────┘ │
│                                     │
│ ┌─────────────────────────────────┐ │
│ │ nested() Scope                  │ │
│ │ Can access param1, param2       │ │
│ │ via scope chain                 │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
*/
```

### **9.4 Block Scope**

Variables declared with `let` and `const` are **block-scoped** (ES6+).

#### **Block Scope Basics:**

```javascript
{
    // This is a block
    let blockLet = "block scoped";
    const blockConst = "also block scoped";
    var notBlock = "function scoped"; // var ignores blocks!
    
    console.log(blockLet);    // ✓ Accessible
    console.log(blockConst);  // ✓ Accessible
    console.log(notBlock);    // ✓ Accessible
}

// console.log(blockLet);    // ✗ ReferenceError
// console.log(blockConst);  // ✗ ReferenceError
console.log(notBlock);    // ✓ "function scoped" (leaked!)

/*
═══════════════════════════════════════════════════════════
WHAT CREATES A BLOCK SCOPE?
═══════════════════════════════════════════════════════════

1. Curly braces { }
2. if statements
3. for loops
4. while loops
5. do-while loops
6. switch statements
7. try-catch blocks

Note: Function bodies also use { }, but they create
      FUNCTION SCOPE, not just block scope.
*/
```

#### **Block Scope in Different Statements:**

```javascript
// IF STATEMENT
if (true) {
    let ifLet = "if block";
    const ifConst = "if block";
}
// console.log(ifLet);  // ✗ ReferenceError

// FOR LOOP
for (let i = 0; i < 3; i++) {
    let loopLet = i;
    console.log(loopLet);  // 0, 1, 2
}
// console.log(i);       // ✗ ReferenceError
// console.log(loopLet); // ✗ ReferenceError

// WHILE LOOP
while (false) {
    let whileLet = "while";
}
// console.log(whileLet); // ✗ ReferenceError

// SWITCH STATEMENT
switch (true) {
    case true:
        let switchLet = "switch";
        console.log(switchLet);
        break;
}
// console.log(switchLet); // ✗ ReferenceError

// TRY-CATCH
try {
    let tryLet = "try";
    throw new Error();
} catch (e) {
    let catchLet = "catch";
    console.log(catchLet);
}
// console.log(tryLet);   // ✗ ReferenceError
// console.log(catchLet); // ✗ ReferenceError

// STANDALONE BLOCK
{
    let blockLet = "standalone";
}
// console.log(blockLet); // ✗ ReferenceError

/*
═══════════════════════════════════════════════════════════
BLOCK SCOPE HIERARCHY
═══════════════════════════════════════════════════════════

┌─────────────────────────────────┐
│ Global/Function Scope           │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ if block                    │ │
│ │ ifLet, ifConst              │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ for loop block              │ │
│ │ i, loopLet                  │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ try block                   │ │
│ │ tryLet                      │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ catch block                 │ │
│ │ e, catchLet                 │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
*/
```

#### **Block Scope in Loops (Detailed):**

```javascript
// FOR LOOP - Each iteration gets its own scope!
for (let i = 0; i < 3; i++) {
    setTimeout(() => {
        console.log("let i:", i);
    }, 100);
}
// Output: 0, 1, 2 ✓

// Compare with var (no block scope)
for (var j = 0; j < 3; j++) {
    setTimeout(() => {
        console.log("var j:", j);
    }, 100);
}
// Output: 3, 3, 3 ✗

/*
═══════════════════════════════════════════════════════════
WHY DIFFERENT BEHAVIOR?
═══════════════════════════════════════════════════════════

FOR LOOP WITH LET:
──────────────────
Each iteration creates NEW block scope:

Iteration 0:
┌─────────────────────────┐
│ Block Scope (iter 0)    │
│ i: 0                    │ ← Separate i
│ setTimeout closure      │
│ captures THIS i         │
└─────────────────────────┘

Iteration 1:
┌─────────────────────────┐
│ Block Scope (iter 1)    │
│ i: 1                    │ ← Different i
│ setTimeout closure      │
│ captures THIS i         │
└─────────────────────────┘

Iteration 2:
┌─────────────────────────┐
│ Block Scope (iter 2)    │
│ i: 2                    │ ← Yet another i
│ setTimeout closure      │
│ captures THIS i         │
└─────────────────────────┘

FOR LOOP WITH VAR:
──────────────────
No block scope, single j:

┌─────────────────────────┐
│ Function/Global Scope   │
│ j: 3 (after loop ends)  │ ← SAME j
│                         │
│ All three setTimeout    │
│ callbacks reference     │
│ THIS SAME j             │
└─────────────────────────┘
*/
```

#### **Nested Block Scopes:**

```javascript
function nestedBlocks() {
    let outer = "outer";
    
    {
        let middle = "middle";
        console.log(outer);  // ✓ Accessible
        
        {
            let inner = "inner";
            console.log(outer);   // ✓ Accessible
            console.log(middle);  // ✓ Accessible
            console.log(inner);   // ✓ Accessible
        }
        
        // console.log(inner);  // ✗ ReferenceError
    }
    
    // console.log(middle);  // ✗ ReferenceError
}

nestedBlocks();

/*
═══════════════════════════════════════════════════════════
NESTED BLOCK SCOPE VISUALIZATION
═══════════════════════════════════════════════════════════

┌─────────────────────────────────────────┐
│ nestedBlocks() Function Scope           │
│ outer: "outer"                          │
│                                         │
│ ┌─────────────────────────────────────┐ │
│ │ First Block Scope                   │ │
│ │ middle: "middle"                    │ │
│ │                                     │ │
│ │ ┌─────────────────────────────────┐ │ │
│ │ │ Second Block Scope              │ │ │
│ │ │ inner: "inner"                  │ │ │
│ │ │                                 │ │ │
│ │ │ Can access:                     │ │ │
│ │ │ ✓ inner (own)                   │ │ │
│ │ │ ✓ middle (parent block)         │ │ │
│ │ │ ✓ outer (function scope)        │ │ │
│ │ └─────────────────────────────────┘ │ │
│ │                                     │ │
│ │ Can access:                         │ │
│ │ ✓ middle (own)                      │ │
│ │ ✓ outer (function scope)            │ │
│ │ ✗ inner (child block, not visible) │ │
│ └─────────────────────────────────────┘ │
│                                         │
│ Can access:                             │
│ ✓ outer (own)                           │
│ ✗ middle (child block, not visible)    │
│ ✗ inner (grandchild block, not visible)│
└─────────────────────────────────────────┘
*/
```

#### **Block Scope with Switch Statements:**

```javascript
function switchScope(value) {
    switch (value) {
        case 1:
            let x = "case 1";
            console.log(x);
            break;
        
        case 2:
            // let x = "case 2";  // ✗ SyntaxError: Identifier 'x' has already been declared
            console.log(x);  // Actually would access case 1's x! (if no break)
            break;
    }
}

// SOLUTION: Wrap cases in blocks
function switchScopeSolution(value) {
    switch (value) {
        case 1: {
            let x = "case 1";
            console.log(x);
            break;
        }
        
        case 2: {
            let x = "case 2";  // ✓ Different block, different scope
            console.log(x);
            break;
        }
    }
}

switchScope(1);
switchScopeSolution(2);

/*
═══════════════════════════════════════════════════════════
SWITCH STATEMENT SCOPE ISSUE
═══════════════════════════════════════════════════════════

WITHOUT BLOCKS:
───────────────
switch (value) {
    case 1:
        let x = "case 1";  ← Declaration in switch scope
        break;
    
    case 2:
        let x = "case 2";  ← SAME scope! Redeclaration error!
        break;
}

Scope:
┌─────────────────────────┐
│ Switch Statement Scope  │
│ x: (declared twice!)    │ ✗
│                         │
│ case 1: ...             │
│ case 2: ...             │
└─────────────────────────┘

WITH BLOCKS:
────────────
switch (value) {
    case 1: {
        let x = "case 1";  ← Declaration in case 1 block
        break;
    }
    
    case 2: {
        let x = "case 2";  ← Declaration in case 2 block ✓
        break;
    }
}

Scope:
┌─────────────────────────┐
│ Switch Statement Scope  │
│                         │
│ ┌─────────────────────┐ │
│ │ case 1 block        │ │
│ │ x: "case 1"         │ │
│ └─────────────────────┘ │
│                         │
│ ┌─────────────────────┐ │
│ │ case 2 block        │ │
│ │ x: "case 2"         │ │
│ └─────────────────────┘ │
└─────────────────────────┘
*/
```

### **9.5 Lexical Scope**

**Lexical scope** (also called static scope) means that scope is determined by the code structure, not by runtime execution.

#### **Lexical Scope Fundamentals:**

```javascript
let x = "global";

function outer() {
    let x = "outer";
    
    function inner() {
        console.log(x);  // Which 'x' ?
    }
    
    return inner;
}

function caller() {
    let x = "caller";
    const fn = outer();
    fn();  // What does this print?
}

caller();  // Output: "outer"

/*
═══════════════════════════════════════════════════════════
LEXICAL SCOPING EXPLAINED
═══════════════════════════════════════════════════════════

Key Principle: Scope is determined by WHERE the function is
               DEFINED, not WHERE it is CALLED.

inner() is DEFINED inside outer(), so it looks for 'x' in:
1. inner()'s own scope → not found
2. outer()'s scope → FOUND 'x' = "outer" ✓

inner() is CALLED inside caller(), but that doesn't matter!
It doesn't look in caller()'s scope.

Visual:
Code Structure (where defined):
┌─────────────────────────────┐
│ Global                      │
│ x: "global"                 │
│                             │
│ ┌─────────────────────────┐ │
│ │ outer()                 │ │
│ │ x: "outer"              │ │
│ │                         │ │
│ │ ┌─────────────────────┐ │ │
│ │ │ inner()             │ │ │
│ │ │ console.log(x)      │ │ │
│ │ │ Looks in outer ─────┼─┼┼→ "outer"
│ │ └─────────────────────┘ │ │
│ └─────────────────────────┘ │
│                             │
│ caller() (separate chain)   │
│ x: "caller" (NOT accessed)  │
└─────────────────────────────┘

This is LEXICAL (static) scoping.
If JavaScript used DYNAMIC scoping, inner() would print "caller".
*/
```

#### **Lexical Scope vs Dynamic Scope:**

```javascript
let value = "global";

function outer() {
    let value = "outer";
    
    function inner() {
        console.log(value);
    }
    
    return inner;
}

function middle() {
    let value = "middle";
    const fn = outer();
    fn();
}

middle();

/*
═══════════════════════════════════════════════════════════
LEXICAL SCOPE (JavaScript)
═══════════════════════════════════════════════════════════

Output: "outer"

Why? inner() looks for 'value' in:
1. inner()'s scope → not found
2. outer()'s scope (WHERE DEFINED) → FOUND "outer" ✓

Doesn't look in middle()'s scope (WHERE CALLED)

═══════════════════════════════════════════════════════════
DYNAMIC SCOPE (NOT JavaScript)
═══════════════════════════════════════════════════════════

Hypothetical output: "middle"

With dynamic scoping, inner() would look for 'value' in:
1. inner()'s scope → not found
2. middle()'s scope (WHERE CALLED) → FOUND "middle"

Languages with dynamic scoping: Some Lisp dialects, Bash

═══════════════════════════════════════════════════════════
COMPARISON TABLE
═══════════════════════════════════════════════════════════

╔════════════════╦══════════════════╦══════════════════╗
║    Aspect      ║  Lexical Scope   ║  Dynamic Scope   ║
╠════════════════╬══════════════════╬══════════════════╣
║ Determined by  ║ Code structure   ║ Call stack       ║
║ When           ║ Compile/parse    ║ Runtime          ║
║ Looks in       ║ Parent scopes    ║ Caller scopes    ║
║ Predictable    ║ Yes              ║ No               ║
║ Closure-safe   ║ Yes              ║ No               ║
║ Used by        ║ JavaScript, C,   ║ Bash, some Lisps ║
║                ║ Python, Java     ║                  ║
╚════════════════╩══════════════════╩══════════════════╝
*/
```

#### **Lexical Scope and Closures:**

```javascript
function makeCounter() {
    let count = 0;
    
    return {
        increment: function() {
            count++;
            return count;
        },
        decrement: function() {
            count--;
            return count;
        },
        getCount: function() {
            return count;
        }
    };
}

const counter1 = makeCounter();
const counter2 = makeCounter();

console.log(counter1.increment());  // 1
console.log(counter1.increment());  // 2
console.log(counter2.increment());  // 1
console.log(counter1.getCount());   // 2
console.log(counter2.getCount());   // 1

/*
═══════════════════════════════════════════════════════════
LEXICAL SCOPE ENABLES CLOSURES
═══════════════════════════════════════════════════════════

Each call to makeCounter() creates a NEW lexical environment:

counter1's environment:
┌──────────────────────────────┐
│ makeCounter() Scope          │
│ count: 2                     │ ← Preserved!
│                              │
│ Three functions close over   │
│ THIS specific 'count'        │
└──────────────────────────────┘

counter2's environment:
┌──────────────────────────────┐
│ makeCounter() Scope          │
│ count: 1                     │ ← Different count!
│                              │
│ Three functions close over   │
│ THIS specific 'count'        │
└──────────────────────────────┘

The returned functions maintain access to their LEXICAL
environment (where they were defined), not the environment
where they're called from.

This is only possible because of LEXICAL scoping!
*/
```

#### **Lexical Scope Chain:**

```javascript
let global = "global";

function level1() {
    let var1 = "level1";
    
    function level2() {
        let var2 = "level2";
        
        function level3() {
            let var3 = "level3";
            
            // All accessible via lexical scope chain
            console.log(var3);    // Own scope
            console.log(var2);    // Parent scope
            console.log(var1);    // Grandparent scope
            console.log(global);  // Global scope
        }
        
        level3();
    }
    
    level2();
}

level1();

/*
═══════════════════════════════════════════════════════════
LEXICAL SCOPE CHAIN
═══════════════════════════════════════════════════════════

When level3() executes and tries to resolve 'var1':

Step 1: Look in level3()'s scope
  { var3: "level3" }
  var1 not found → continue to parent

Step 2: Look in level2()'s scope (lexical parent)
  { var2: "level2" }
  var1 not found → continue to parent

Step 3: Look in level1()'s scope (lexical grandparent)
  { var1: "level1" }
  var1 FOUND! ✓
  Return "level1"

Visual Scope Chain:
┌────────────────────────────────────┐
│ Global Scope                       │
│ global: "global"                   │
│                                    │
│ ┌────────────────────────────────┐ │
│ │ level1() Scope                 │ │
│ │ var1: "level1"                 │ │
│ │ [[Scope]]: → Global            │ │
│ │                                │ │
│ │ ┌────────────────────────────┐ │ │
│ │ │ level2() Scope             │ │ │
│ │ │ var2: "level2"             │ │ │
│ │ │ [[Scope]]: → level1()      │ │ │
│ │ │                            │ │ │
│ │ │ ┌────────────────────────┐ │ │ │
│ │ │ │ level3() Scope         │ │ │ │
│ │ │ │ var3: "level3"         │ │ │ │
│ │ │ │ [[Scope]]: → level2()  │ │ │ │
│ │ │ │                        │ │ │ │
│ │ │ │ Resolution path:       │ │ │ │
│ │ │ │ var3 → level3() ✓      │ │ │ │
│ │ │ │ var2 → level2() ✓      │ │ │ │
│ │ │ │ var1 → level1() ✓      │ │ │ │
│ │ │ │ global → Global ✓      │ │ │ │
│ │ │ └────────────────────────┘ │ │ │
│ │ └────────────────────────────┘ │ │
│ └────────────────────────────────┘ │
└────────────────────────────────────┘

Each function stores a reference to its lexical parent scope
in an internal [[Scope]] property.
*/
```

### **9.6 Dynamic Scope (and why JS doesn't have it)**

JavaScript does NOT use dynamic scope, but understanding it helps clarify lexical scope.

#### **Dynamic Scope Example (Hypothetical):**

```javascript
// How JavaScript ACTUALLY works (lexical scope):
let value = "global";

function printValue() {
    console.log(value);
}

function first() {
    let value = "first";
    printValue();
}

function second() {
    let value = "second";
    printValue();
}

first();   // "global" (lexical scope)
second();  // "global" (lexical scope)

/*
═══════════════════════════════════════════════════════════
IF JAVASCRIPT HAD DYNAMIC SCOPE (hypothetical):
═══════════════════════════════════════════════════════════

first();   // Would print "first"
second();  // Would print "second"

Why? With dynamic scope:
- printValue() would look for 'value' in its CALLER's scope
- first() calls printValue() → 'value' = "first"
- second() calls printValue() → 'value' = "second"

But JavaScript uses LEXICAL scope:
- printValue() looks for 'value' where it's DEFINED
- printValue() defined in global scope
- Uses global 'value'

═══════════════════════════════════════════════════════════
WHY LEXICAL SCOPE IS BETTER
═══════════════════════════════════════════════════════════

1. PREDICTABLE
   - Scope determined by code structure (visible)
   - Same result no matter who calls function

2. CLOSURE-FRIENDLY
   - Functions remember where they're defined
   - Can maintain private state

3. OPTIMIZABLE
   - Compiler knows scope at parse time
   - Can optimize variable access

4. MAINTAINABLE
   - Easy to understand variable flow
   - No hidden dependencies on call stack

═══════════════════════════════════════════════════════════
'this' IS DYNAMIC (Kind of)
═══════════════════════════════════════════════════════════

JavaScript DOES have one dynamic aspect: 'this'

function showThis() {
    console.log(this.name);
}

const obj1 = { name: "Object 1", showThis };
const obj2 = { name: "Object 2", showThis };

obj1.showThis();  // "Object 1" (dynamic)
obj2.showThis();  // "Object 2" (dynamic)

'this' is determined by HOW function is called (dynamic)
But variable resolution uses WHERE function is defined (lexical)
*/
```

### **9.7 Module Scope**

ES6 modules have their own scope, separate from global scope.

#### **Module Scope Basics:**

```javascript
// module.js
let moduleVar = "module scoped";
const moduleConst = "also module scoped";

function moduleFunction() {
    return "module function";
}

class ModuleClass {
    constructor() {
        this.type = "module class";
    }
}

// These are NOT global!
console.log(window.moduleVar);  // undefined
console.log(window.moduleFunction);  // undefined

// Only exports are accessible outside
export { moduleVar, moduleFunction, ModuleClass };

// Or
export default ModuleClass;

/*
═══════════════════════════════════════════════════════════
MODULE SCOPE VS GLOBAL SCOPE
═══════════════════════════════════════════════════════════

TRADITIONAL SCRIPT (<script src="...">):
────────────────────────────────────────
- Code runs in global scope
- var creates global variables
- Variables attach to window

<script>
    var x = 10;
    console.log(window.x);  // 10
    console.log(this);      // window
</script>

ES6 MODULE (<script type="module">):
────────────────────────────────────
- Code runs in module scope
- Variables do NOT become global
- Strict mode by default

<script type="module">
    var x = 10;
    console.log(window.x);  // undefined
    console.log(this);      // undefined
</script>

═══════════════════════════════════════════════════════════
MODULE SCOPE VISUALIZATION
═══════════════════════════════════════════════════════════

┌─────────────────────────────────────┐
│ Global Scope                        │
│ (window/global object)              │
│                                     │
│ No direct access to modules!       │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ Module A Scope                      │
│ - Private variables                 │
│ - Private functions                 │
│ - export { ... }                    │
│                                     │
│ Can only share via exports          │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ Module B Scope                      │
│ - Private variables                 │
│ - import { ... } from A             │
│ - export { ... }                    │
└─────────────────────────────────────┘
*/
```

#### **Module Scope Examples:**

```javascript
// math.js
let privateCount = 0;  // Not exported, truly private

export function increment() {
    privateCount++;
    return privateCount;
}

export function getCount() {
    return privateCount;
}

// Constants and utilities
export const PI = 3.14159;
export const E = 2.71828;

const internalHelper = () => {
    // This is private to the module
};

export function publicFunction() {
    internalHelper();  // Can use private function
}

// Default export
export default class Math {
    static add(a, b) {
        return a + b;
    }
}

/*
═══════════════════════════════════════════════════════════
MODULE SCOPE FEATURES
═══════════════════════════════════════════════════════════

1. ENCAPSULATION
   - privateCount is TRULY private
   - No way to access from outside
   - Better than IIFE pattern

2. EXPLICIT EXPORTS
   - Only exported items are visible
   - Clear API surface
   - Prevents accidental globals

3. STRICT MODE
   - Always in strict mode
   - No need for 'use strict'
   - Catches more errors

4. TOP-LEVEL 'this' is undefined
   - Not window/global
   - Prevents accidental global access

5. IMPORTS ARE READ-ONLY
   - Cannot reassign imported values
   - Live binding (changes reflect)
*/

// app.js
import MathClass, { increment, getCount, PI } from './math.js';

console.log(increment());  // 1
console.log(increment());  // 2
console.log(getCount());   // 2
console.log(PI);           // 3.14159

// Cannot access private variables
console.log(typeof privateCount);  // "undefined"
console.log(typeof internalHelper);  // "undefined"

// Imports are read-only
// PI = 3;  // TypeError: Assignment to constant variable
// increment = () => {};  // TypeError

/*
═══════════════════════════════════════════════════════════
IMPORTING AND MODULE SCOPE
═══════════════════════════════════════════════════════════

Scope after import:
┌─────────────────────────────────────┐
│ app.js Module Scope                 │
│                                     │
│ Imported (read-only):               │
│ - MathClass                         │
│ - increment                         │
│ - getCount                          │
│ - PI                                │
│                                     │
│ NOT imported (not accessible):     │
│ - privateCount                      │
│ - internalHelper                    │
└─────────────────────────────────────┘

Live Binding:
When increment() modifies privateCount in math.js,
getCount() immediately reflects the change (live binding)
*/
```

#### **Module Scope and Hoisting:**

```javascript
// Imports are hoisted
console.log(add(5, 3));  // 8 ✓

import { add } from './math.js';

// But module code is only evaluated once
import { PI } from './math.js';
import { PI as PI2 } from './math.js';

console.log(PI === PI2);  // true (same value)

/*
═══════════════════════════════════════════════════════════
MODULE EVALUATION
═══════════════════════════════════════════════════════════

1. IMPORT HOISTING
   - All imports hoisted to top
   - Can use before import statement

2. SINGLE EVALUATION
   - Module code runs only once
   - First import triggers evaluation
   - Subsequent imports reuse same instance

3. IMPORT ORDER
   - Depth-first order
   - Dependencies evaluated first

Example:
// main.js imports a.js
// a.js imports b.js
// b.js imports c.js

Evaluation order:
1. c.js
2. b.js
3. a.js
4. main.js

═══════════════════════════════════════════════════════════
MODULE SCOPE BEST PRACTICES
═══════════════════════════════════════════════════════════

1. Export minimal API
   - Only export what's necessary
   - Keep implementation private

2. Use named exports for utilities
   - import { specific, items }
   - Tree-shaking friendly

3. Use default export for main thing
   - import MainThing from './module'
   - Clear primary purpose

4. Avoid export default for multiple exports
   - Use named exports instead
   - Better for refactoring

5. Keep modules focused
   - Single responsibility
   - Easy to understand and test
*/
```

---

## **10. THE SCOPE CHAIN**

### **10.1 How Scope Chain Works**

The **scope chain** is the mechanism JavaScript uses to resolve variable names by looking up through nested scopes.

#### **Scope Chain Fundamentals:**

```javascript
let global = "global";

function outer() {
    let outerVar = "outer";
    
    function inner() {
        let innerVar = "inner";
        
        console.log(innerVar);   // Found in inner scope
        console.log(outerVar);   // Found in outer scope (via chain)
        console.log(global);     // Found in global scope (via chain)
        // console.log(nonExistent); // ReferenceError (not in any scope)
    }
    
    inner();
}

outer();

/*
═══════════════════════════════════════════════════════════
SCOPE CHAIN LOOKUP PROCESS
═══════════════════════════════════════════════════════════

When inner() tries to resolve 'outerVar':

┌─────────────────────────────────────┐
│ Step 1: Look in current scope       │
│ inner() scope: { innerVar: "..." } │
│ outerVar not found → Go to parent   │
└─────────────────────────────────────┘
            ↓
┌─────────────────────────────────────┐
│ Step 2: Look in parent scope        │
│ outer() scope: { outerVar: "..." } │
│ outerVar FOUND! Return "outer" ✓    │
└─────────────────────────────────────┘

When inner() tries to resolve 'global':

┌─────────────────────────────────────┐
│ Step 1: Look in inner() scope       │
│ global not found → Go to parent     │
└─────────────────────────────────────┘
            ↓
┌─────────────────────────────────────┐
│ Step 2: Look in outer() scope       │
│ global not found → Go to parent     │
└─────────────────────────────────────┘
            ↓
┌─────────────────────────────────────┐
│ Step 3: Look in global scope        │
│ global FOUND! Return "global" ✓     │
└─────────────────────────────────────┘

When inner() tries to resolve 'nonExistent':

Steps 1-3: Not found in any scope
Step 4: Reached end of scope chain
Result: ReferenceError ✗
*/
```

#### **Scope Chain Internal Structure:**

```javascript
function demonstrateChain() {
    let level1 = "L1";
    
    function nested1() {
        let level2 = "L2";
        
        function nested2() {
            let level3 = "L3";
            
            console.log(level3, level2, level1);
        }
        
        nested2();
    }
    
    nested1();
}

demonstrateChain();

/*
═══════════════════════════════════════════════════════════
INTERNAL SCOPE CHAIN STRUCTURE
═══════════════════════════════════════════════════════════

Each function has an internal [[Scope]] property:

nested2 execution context:
{
    LexicalEnvironment: {
        EnvironmentRecord: { level3: "L3" },
        outer: → nested1's Lexical Environment
    }
}
         ↓
nested1's Lexical Environment:
{
    EnvironmentRecord: { level2: "L2" },
    outer: → demonstrateChain's Lexical Environment
}
         ↓
demonstrateChain's Lexical Environment:
{
    EnvironmentRecord: { level1: "L1" },
    outer: → Global Lexical Environment
}
         ↓
Global Lexical Environment:
{
    EnvironmentRecord: { demonstrateChain: <function>, ... },
    outer: → null
}

This chain of 'outer' references IS the scope chain!

When nested2() accesses 'level1':
1. Look in nested2's EnvironmentRecord: Not found
2. Follow outer → Look in nested1's Record: Not found
3. Follow outer → Look in demonstrateChain's Record: FOUND! ✓
*/
```

### **10.2 Scope Chain Resolution**

#### **Step-by-Step Resolution Example:**

```javascript
let globalX = "global X";

function first() {
    let firstX = "first X";
    let firstY = "first Y";
    
    function second() {
        let secondX = "second X";
        let secondZ = "second Z";
        
        function third() {
            let thirdW = "third W";
            
            // Resolve each variable
            console.log("thirdW:", thirdW);     // Step 1
            console.log("secondZ:", secondZ);   // Steps 1-2
            console.log("secondX:", secondX);   // Steps 1-2
            console.log("firstY:", firstY);     // Steps 1-3
            console.log("firstX:", firstX);     // Steps 1-3
            console.log("globalX:", globalX);   // Steps 1-4
        }
        
        third();
    }
    
    second();
}

first();

/*
═══════════════════════════════════════════════════════════
DETAILED RESOLUTION PROCESS
═══════════════════════════════════════════════════════════

Resolving 'thirdW':
───────────────────
Step 1: third() scope
  { thirdW: "third W" }
  FOUND! ✓ Return immediately

Resolving 'secondZ':
────────────────────
Step 1: third() scope
  { thirdW: "third W" }
  secondZ not found → continue
  
Step 2: second() scope
  { secondX: "second X", secondZ: "second Z" }
  FOUND! ✓ Return "second Z"

Resolving 'secondX':
────────────────────
Step 1: third() scope → not found
Step 2: second() scope
  { secondX: "second X", secondZ: "second Z" }
  FOUND! ✓ Return "second X"

Resolving 'firstY':
───────────────────
Step 1: third() scope → not found
Step 2: second() scope → not found
Step 3: first() scope
  { firstX: "first X", firstY: "first Y" }
  FOUND! ✓ Return "first Y"

Resolving 'firstX':
───────────────────
Step 1: third() scope → not found
Step 2: second() scope → not found
Step 3: first() scope
  { firstX: "first X", firstY: "first Y" }
  FOUND! ✓ Return "first X"

Note: Even though second() has 'secondX',
      first() has 'firstX' - no confusion!
      Each scope is distinct.

Resolving 'globalX':
────────────────────
Step 1: third() scope → not found
Step 2: second() scope → not found
Step 3: first() scope → not found
Step 4: Global scope
  { globalX: "global X" }
  FOUND! ✓ Return "global X"

═══════════════════════════════════════════════════════════
PERFORMANCE IMPLICATION
═══════════════════════════════════════════════════════════

Variables in:
- Own scope: 1 lookup (fastest)
- Parent scope: 2 lookups
- Grandparent scope: 3 lookups
- Global scope: N lookups (slowest)

For frequently accessed outer variables:
Consider caching in local scope for performance.

// Instead of:
function deep() {
    for (let i = 0; i < 1000; i++) {
        console.log(outerVariable);  // Many lookups!
    }
}

// Consider:
function deep() {
    const local = outerVariable;  // One lookup
    for (let i = 0; i < 1000; i++) {
        console.log(local);  // Fast!
    }
}
*/
```

#### **Scope Chain with Variable Shadowing:**

```javascript
let x = "global";

function level1() {
    let x = "level1";
    console.log("In level1:", x);
    
    function level2() {
        let x = "level2";
        console.log("In level2:", x);
        
        function level3() {
            let x = "level3";
            console.log("In level3:", x);
        }
        
        level3();
    }
    
    level2();
}

level1();

/*
Output:
In level1: level1
In level2: level2
In level3: level3

═══════════════════════════════════════════════════════════
SHADOWING IN SCOPE CHAIN
═══════════════════════════════════════════════════════════

Each level's 'x' SHADOWS the outer 'x':

┌─────────────────────────────────────┐
│ Global Scope                        │
│ x: "global"                         │ ← Never accessed!
│                                     │
│ ┌─────────────────────────────────┐ │
│ │ level1() Scope                  │ │
│ │ x: "level1"  ← Shadows global   │ │
│ │                                 │ │
│ │ ┌─────────────────────────────┐ │ │
│ │ │ level2() Scope              │ │ │
│ │ │ x: "level2" ← Shadows L1    │ │ │
│ │ │                             │ │ │
│ │ │ ┌─────────────────────────┐ │ │ │
│ │ │ │ level3() Scope          │ │ │ │
│ │ │ │ x: "level3" ← Shadows L2│ │ │ │
│ │ │ │                         │ │ │ │
│ │ │ │ console.log(x)          │ │ │ │
│ │ │ │ Looks in level3 → STOP  │ │ │ │
│ │ │ │ Found "level3" ✓        │ │ │ │
│ │ │ └─────────────────────────┘ │ │ │
│ │ └─────────────────────────────┘ │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘

Scope chain resolution STOPS at first match.
Inner 'x' shadows all outer 'x' variables.

To access outer variables when shadowed:
- No direct way for same name!
- window.x works for global var (not let/const)
- Best practice: Use different names
*/
```

### **10.3 Identifier Resolution Process**

#### **Complete Identifier Resolution Algorithm:**

```javascript
let global1 = "global1";
let global2 = "global2";

function outer() {
    let outer1 = "outer1";
    let global2 = "outer shadows global2";
    
    function inner() {
        let inner1 = "inner1";
        let outer1 = "inner shadows outer1";
        
        // Resolution examples
        console.log(inner1);   // Own scope
        console.log(outer1);   // Own scope (shadows outer's outer1)
        console.log(global2);  // Parent scope (shadows global's global2)
        console.log(global1);  // Grandparent scope
    }
    
    inner();
}

outer();

/*
═══════════════════════════════════════════════════════════
IDENTIFIER RESOLUTION ALGORITHM
═══════════════════════════════════════════════════════════

When resolving identifier 'name':

1. GET CURRENT EXECUTION CONTEXT
   └─ Get its Lexical Environment

2. SEARCH CURRENT ENVIRONMENT
   └─ Look in EnvironmentRecord
      ├─ If found → RETURN value
      └─ If not found → GO TO STEP 3

3. GET OUTER ENVIRONMENT
   └─ Follow 'outer' reference
      ├─ If outer is null → GO TO STEP 5
      └─ If outer exists → GO TO STEP 2

4. REPEAT STEP 2-3
   └─ Until found or reach null

5. NOT FOUND
   └─ Throw ReferenceError

═══════════════════════════════════════════════════════════
RESOLUTION EXAMPLES FROM CODE ABOVE
═══════════════════════════════════════════════════════════

Resolving 'inner1':
───────────────────
Current Context: inner()
Current Environment: inner's LexicalEnvironment
  └─ EnvironmentRecord: { inner1: "inner1", outer1: "..." }
     └─ FOUND 'inner1' ✓
        └─ RETURN "inner1"

Resolving 'outer1':
───────────────────
Current Context: inner()
Current Environment: inner's LexicalEnvironment
  └─ EnvironmentRecord: { inner1: "...", outer1: "inner shadows..." }
     └─ FOUND 'outer1' ✓ (shadows outer's outer1!)
        └─ RETURN "inner shadows outer1"

Note: Search stops at first match!
      outer's outer1 is never reached.

Resolving 'global2':
────────────────────
Current Context: inner()

Attempt 1:
  Environment: inner's LexicalEnvironment
  └─ EnvironmentRecord: { inner1: "...", outer1: "..." }
     └─ NOT FOUND → Follow outer reference

Attempt 2:
  Environment: outer's LexicalEnvironment
  └─ EnvironmentRecord: { outer1: "...", global2: "..." }
     └─ FOUND 'global2' ✓
        └─ RETURN "outer shadows global2"

Resolving 'global1':
────────────────────
Current Context: inner()

Attempt 1:
  Environment: inner's LexicalEnvironment
  └─ NOT FOUND → Follow outer

Attempt 2:
  Environment: outer's LexicalEnvironment
  └─ NOT FOUND → Follow outer

Attempt 3:
  Environment: Global LexicalEnvironment
  └─ EnvironmentRecord: { global1: "global1", global2: "global2" }
     └─ FOUND 'global1' ✓
        └─ RETURN "global1"
*/
```

#### **Identifier Resolution with Different Declaration Types:**

```javascript
function mixedDeclarations() {
    var varVariable = "var";
    let letVariable = "let";
    const constVariable = "const";
    
    function declaredFunc() {
        return "declared";
    }
    
    const expressionFunc = function() {
        return "expression";
    };
    
    const arrowFunc = () => {
        return "arrow";
    };
    
    // All resolved through scope chain
    console.log(varVariable);
    console.log(letVariable);
    console.log(constVariable);
    console.log(declaredFunc());
    console.log(expressionFunc());
    console.log(arrowFunc());
}

mixedDeclarations();

/*
═══════════════════════════════════════════════════════════
RESOLUTION BY DECLARATION TYPE
═══════════════════════════════════════════════════════════

mixedDeclarations() Execution Context:
{
    VariableEnvironment: {
        EnvironmentRecord: {
            varVariable: "var",
            declaredFunc: <function object>
        },
        outer: → Global Environment
    },
    
    LexicalEnvironment: {
        EnvironmentRecord: {
            letVariable: "let",
            constVariable: "const",
            expressionFunc: <function object>,
            arrowFunc: <function object>
        },
        outer: → Global Environment
    }
}

Identifier Resolution Process:
───────────────────────────────

For 'varVariable':
1. Check LexicalEnvironment → NOT FOUND
2. Check VariableEnvironment → FOUND ✓

For 'letVariable':
1. Check LexicalEnvironment → FOUND ✓

For 'declaredFunc':
1. Check LexicalEnvironment → NOT FOUND
2. Check VariableEnvironment → FOUND ✓

For 'expressionFunc':
1. Check LexicalEnvironment → FOUND ✓

Note: JavaScript checks BOTH environments in current scope
      before moving to outer scope.

Order:
1. Current LexicalEnvironment
2. Current VariableEnvironment
3. Outer LexicalEnvironment
4. Outer VariableEnvironment
5. Continue up the chain...
*/
```

### **10.4 Scope Chain with Nested Functions**

#### **Complex Nesting Example:**

```javascript
let a = "global a";

function fn1() {
    let b = "fn1 b";
    
    function fn2() {
        let c = "fn2 c";
        
        function fn3() {
            let d = "fn3 d";
            
            function fn4() {
                let e = "fn4 e";
                
                // All accessible via scope chain!
                console.log("e:", e);  // Own
                console.log("d:", d);  // Parent (fn3)
                console.log("c:", c);  // Grandparent (fn2)
                console.log("b:", b);  // Great-grandparent (fn1)
                console.log("a:", a);  // Global
            }
            
            fn4();
        }
        
        fn3();
    }
    
    fn2();
}

fn1();

/*
═══════════════════════════════════════════════════════════
SCOPE CHAIN WITH MULTIPLE NESTING LEVELS
═══════════════════════════════════════════════════════════

Scope Chain for fn4():

fn4() Scope
│ e: "fn4 e"
│ outer ──→ fn3() Scope
           │ d: "fn3 d"
           │ outer ──→ fn2() Scope
                      │ c: "fn2 c"
                      │ outer ──→ fn1() Scope
                                 │ b: "fn1 b"
                                 │ outer ──→ Global Scope
                                            │ a: "global a"
                                            │ outer: null

When fn4() accesses 'b':
├─ fn4() scope: e → not 'b'
├─ fn3() scope: d → not 'b'
├─ fn2() scope: c → not 'b'
├─ fn1() scope: b → FOUND! ✓
└─ Return "fn1 b"

Each function maintains a reference to its parent scope,
creating a chain that allows access to all outer variables.

═══════════════════════════════════════════════════════════
MEMORY AND PERFORMANCE
═══════════════════════════════════════════════════════════

Deep nesting implications:
1. Longer scope chains → slower lookups
2. More memory (keeping parent scopes alive)
3. Harder to reason about code

Best practices:
1. Keep nesting shallow when possible
2. Cache frequently-accessed outer variables
3. Consider passing values as parameters

// Instead of:
function deep() {
    function deeper() {
        function deepest() {
            console.log(outerVariable);  // Long lookup
        }
    }
}

// Consider:
function deep() {
    function deeper(value) {
        function deepest() {
            console.log(value);  // Parameter, fast
        }
    }
}
*/
```

#### **Scope Chain with Closures:**

```javascript
function outerFunction() {
    let outerVar = "outer";
    let counter = 0;
    
    function innerFunction() {
        counter++;
        let innerVar = "inner";
        
        return function() {
            console.log("Outer:", outerVar);
            console.log("Inner:", innerVar);
            console.log("Counter:", counter);
        };
    }
    
    return innerFunction;
}

const inner = outerFunction();
const closure1 = inner();
const closure2 = inner();

closure1();  // Counter: 1
closure2();  // Counter: 2

/*
═══════════════════════════════════════════════════════════
CLOSURE SCOPE CHAIN
═══════════════════════════════════════════════════════════

When outerFunction() is called:
┌──────────────────────────────────┐
│ outerFunction() Scope            │
│ outerVar: "outer"                │
│ counter: 0                       │
│ innerFunction: <function>        │
└──────────────────────────────────┘

When innerFunction() is called (first time):
┌──────────────────────────────────┐
│ innerFunction() Scope (Call 1)   │
│ innerVar: "inner"                │
│ counter: 0 → 1 (incremented)     │
│ Returns function that closes     │
│ over THIS innerVar               │
│                                  │
│ outer ──→ outerFunction() Scope  │
└──────────────────────────────────┘

When innerFunction() is called (second time):
┌──────────────────────────────────┐
│ innerFunction() Scope (Call 2)   │
│ innerVar: "inner" (new one!)     │
│ counter: 1 → 2 (incremented)     │
│ Returns function that closes     │
│ over THIS innerVar               │
│                                  │
│ outer ──→ outerFunction() Scope  │
│          (SAME outerFunction)    │
└──────────────────────────────────┘

closure1's Scope Chain:
└─ Returned function scope
   └─ innerFunction() Call 1 scope
      └─ outerFunction() scope
         └─ Global scope

closure2's Scope Chain:
└─ Returned function scope
   └─ innerFunction() Call 2 scope
      └─ outerFunction() scope (SAME!)
         └─ Global scope

Both closures share outerFunction()'s scope,
but each has its own innerFunction() scope!

Result:
- counter is shared (in outerFunction's scope)
- innerVar is separate (in innerFunction's scope)
*/
```

### **10.5 Scope Chain and Performance**

#### **Performance Considerations:**

```javascript
// SLOW: Accessing variable deep in scope chain
let globalConfig = { /* large object */ };

function level1() {
    function level2() {
        function level3() {
            function level4() {
                function level5() {
                    // Many lookups to reach globalConfig!
                    for (let i = 0; i < 1000; i++) {
                        console.log(globalConfig.someProperty);
                    }
                }
                level5();
            }
            level4();
        }
        level3();
    }
    level2();
}

// FAST: Cache in local scope
let globalConfig = { /* large object */ };

function level1() {
    // Cache at higher level
    const config = globalConfig;
    
    function level2() {
        function level3() {
            function level4() {
                function level5() {
                    // Now only 2 lookups instead of 6!
                    for (let i = 0; i < 1000; i++) {
                        console.log(config.someProperty);
                    }
                }
                level5();
            }
            level4();
        }
        level3();
    }
    level2();
}

/*
═══════════════════════════════════════════════════════════
SCOPE CHAIN PERFORMANCE IMPACT
═══════════════════════════════════════════════════════════

Lookup Costs:
─────────────
Own scope:        1 lookup   (fastest)
Parent scope:     2 lookups
Grandparent:      3 lookups
Great-grandp.:    4 lookups
Global:           N lookups  (slowest)

In loops, this multiplies:
- 1000 iterations × 6 lookups = 6000 lookups (slow)
- 1000 iterations × 2 lookups = 2000 lookups (faster)

Modern JavaScript engines optimize this, but:
- Still measurable difference
- Good practice for hot code paths
- Makes code clearer too

═══════════════════════════════════════════════════════════
OPTIMIZATION TECHNIQUES
═══════════════════════════════════════════════════════════
*/

// 1. CACHE FREQUENTLY ACCESSED VARIABLES
function optimized1() {
    const local = expensiveGlobalVar;
    for (let i = 0; i < 1000000; i++) {
        process(local);
    }
}

// 2. USE PARAMETERS INSTEAD OF CLOSURES
function optimized2(value) {
    return function(input) {
        return value + input;  // Parameter, not closure variable
    };
}

// 3. MINIMIZE SCOPE DEPTH
// Bad: Deep nesting
function bad() {
    return function() {
        return function() {
            return function() {
                return globalVar;  // 4+ lookups!
            };
        };
    };
}

// Good: Flatten
function good() {
    const cached = globalVar;
    return () => cached;  // 1 lookup!
}

// 4. USE let/const IN APPROPRIATE SCOPE
// Bad: var leaks to function scope
function bad2() {
    for (var i = 0; i < 1000; i++) {
        var result = compute(i);  // Hoisted to function scope!
    }
}

// Good: let is block-scoped
function good2() {
    for (let i = 0; i < 1000; i++) {
        const result = compute(i);  // Block-scoped, better
    }
}

/*
═══════════════════════════════════════════════════════════
WHEN TO OPTIMIZE
═══════════════════════════════════════════════════════════

Optimize when:
✓ Hot code paths (executed frequently)
✓ Performance-critical sections
✓ Deep scope chains
✓ Large loops

Don't optimize prematurely:
✗ One-time initialization code
✗ Readable closure pattern
✗ Maintainability > micro-optimization
✗ Modern engines are very good

Always measure before optimizing!
*/
```

### **10.6 Common Scope Chain Mistakes**

#### **Mistake 1: Accidental Global Variables**

```javascript
function mistake1() {
    // Forgot let/const/var!
    accidentalGlobal = "Oops";
}

mistake1();
console.log(window.accidentalGlobal);  // "Oops" (global!)

/*
═══════════════════════════════════════════════════════════
WHAT HAPPENED?
═══════════════════════════════════════════════════════════

Resolution Process:
1. Look in mistake1() scope → not found
2. Look in global scope → not found
3. Non-strict mode: CREATE GLOBAL VARIABLE
   Strict mode: ReferenceError ✓

Fix: Always use declarations!

'use strict';
function fixed() {
    accidentalGlobal = "Oops";  // ReferenceError ✓
}
*/
```

#### **Mistake 2: Closure in Loops (var)**

```javascript
// Mistake: Using var in loop
var functions = [];
for (var i = 0; i < 3; i++) {
    functions.push(function() {
        console.log(i);
    });
}

functions[0]();  // 3 (expected 0!)
functions[1]();  // 3 (expected 1!)
functions[2]();  // 3 (expected 2!)

/*
═══════════════════════════════════════════════════════════
WHAT WENT WRONG?
═══════════════════════════════════════════════════════════

var is function-scoped, not block-scoped:

After loop completes:
┌──────────────────────────────┐
│ Outer Scope                  │
│ i: 3                         │ ← SAME i for all functions
│ functions: [fn1, fn2, fn3]   │
└──────────────────────────────┘

All three functions close over the SAME i!

═══════════════════════════════════════════════════════════
FIXES
═══════════════════════════════════════════════════════════
*/

// Fix 1: Use let (block-scoped)
var functions = [];
for (let i = 0; i < 3; i++) {
    functions.push(function() {
        console.log(i);
    });
}

functions[0]();  // 0 ✓
functions[1]();  // 1 ✓
functions[2]();  // 2 ✓

// Fix 2: IIFE
var functions = [];
for (var i = 0; i < 3; i++) {
    (function(j) {
        functions.push(function() {
            console.log(j);
        });
    })(i);
}

// Fix 3: Use forEach
var functions = [];
[0, 1, 2].forEach(function(i) {
    functions.push(function() {
        console.log(i);
    });
});
```

#### **Mistake 3: Overreliance on Global Scope**

```javascript
// Bad: Everything global
var data = [];
var config = {};
var utils = {};

function processData() {
    // Uses global data
}

function updateConfig() {
    // Modifies global config
}

/*
═══════════════════════════════════════════════════════════
PROBLEMS
═══════════════════════════════════════════════════════════

1. Naming conflicts
2. Hard to test
3. No encapsulation
4. Tight coupling
5. Memory never freed

═══════════════════════════════════════════════════════════
BETTER APPROACHES
═══════════════════════════════════════════════════════════
*/

// Better 1: Module pattern
const MyModule = (function() {
    // Private
    let data = [];
    let config = {};
    
    // Public API
    return {
        processData() {
            // Uses private data
        },
        updateConfig(newConfig) {
            config = newConfig;
        }
    };
})();

// Better 2: ES6 Modules
// data.js
let data = [];
export function processData() {
    // Uses module-scoped data
}

// Better 3: Classes
class DataProcessor {
    constructor() {
        this.data = [];
        this.config = {};
    }
    
    processData() {
        // Uses instance properties
    }
}
```

# **PART 5: THE 'THIS' KEYWORD**

## **11. UNDERSTANDING 'THIS'**

### **11.1 What is 'this'?**

**`this`** is a special keyword that refers to the context object in which the current code is executing. Unlike variables that are resolved through the scope chain, `this` is determined by **how a function is called**.

#### **Fundamental 'this' Concept:**

```javascript
/*
═══════════════════════════════════════════════════════════
KEY PRINCIPLE: 'this' is determined by the CALL SITE
═══════════════════════════════════════════════════════════

'this' is NOT:
✗ Where the function is defined (that's scope)
✗ Where the function is declared
✗ A property of the function

'this' IS:
✓ Determined at runtime
✓ Based on how function is called
✓ The context object for the function call
✓ Can change with each function call
*/

const obj = {
    name: "Object",
    showThis: function() {
        console.log(this);
        console.log(this.name);
    }
};

// Same function, different 'this' values:
obj.showThis();              // this = obj, prints "Object"

const detached = obj.showThis;
detached();                  // this = global/undefined

obj.showThis.call({name: "X"});  // this = {name: "X"}

/*
═══════════════════════════════════════════════════════════
'THIS' VS SCOPE VARIABLES
═══════════════════════════════════════════════════════════

const outer = {
    outerName: "Outer",
    method: function() {
        const innerName = "Inner";
        
        function inner() {
            console.log(innerName);    // ✓ Scope chain
            console.log(this.outerName); // ✗ 'this' is not 'outer'!
        }
        
        inner();
    }
};

outer.method();

Output:
"Inner"      ← Found via scope chain
undefined    ← 'this' is global, not outer

Explanation:
- innerName: Resolved through scope chain (lexical)
- this: Determined by how inner() is called (dynamic)
- inner() called as regular function → this = global
- NOT called as method → this ≠ outer
*/
```

#### **The Five Rules of 'this':**

```javascript
/*
═══════════════════════════════════════════════════════════
RULE 1: DEFAULT BINDING (Global Context)
═══════════════════════════════════════════════════════════
*/

function defaultBinding() {
    console.log(this);
}

defaultBinding();  // Window (non-strict) or undefined (strict)

/*
When function is called without any context:
- Non-strict mode: this = global object
- Strict mode: this = undefined

Call Site: defaultBinding()
           ↑ No context

Execution Context:
{
    ThisBinding: <global object> or undefined
}
*/

/*
═══════════════════════════════════════════════════════════
RULE 2: IMPLICIT BINDING (Method Call)
═══════════════════════════════════════════════════════════
*/

const person = {
    name: "John",
    greet: function() {
        console.log(this.name);
    }
};

person.greet();  // "John"

/*
When function is called as object method:
- this = the object

Call Site: person.greet()
           ↑      ↑
         context  method

The object to the left of the dot becomes 'this'

Execution Context:
{
    ThisBinding: person
}
*/

/*
═══════════════════════════════════════════════════════════
RULE 3: EXPLICIT BINDING (call, apply, bind)
═══════════════════════════════════════════════════════════
*/

function explicitBinding() {
    console.log(this.name);
}

const context = { name: "Context" };

explicitBinding.call(context);   // "Context"
explicitBinding.apply(context);  // "Context"

const bound = explicitBinding.bind(context);
bound();  // "Context"

/*
When function is called with call/apply/bind:
- this = the provided object

Execution Context:
{
    ThisBinding: context  // Explicitly set
}
*/

/*
═══════════════════════════════════════════════════════════
RULE 4: NEW BINDING (Constructor)
═══════════════════════════════════════════════════════════
*/

function Person(name) {
    this.name = name;
    console.log(this);
}

const john = new Person("John");

/*
When function is called with 'new':
- Creates new empty object
- this = new object
- Sets prototype
- Returns the object

Process:
1. {} created
2. this = {}
3. {}.[[Prototype]] = Person.prototype
4. Person executes with this = {}
5. Return {} (implicit)

Execution Context:
{
    ThisBinding: <newly created object>
}
*/

/*
═══════════════════════════════════════════════════════════
RULE 5: ARROW FUNCTIONS (Lexical 'this')
═══════════════════════════════════════════════════════════
*/

const obj = {
    name: "Object",
    regular: function() {
        console.log("Regular:", this.name);
        
        const arrow = () => {
            console.log("Arrow:", this.name);
        };
        
        arrow();
    }
};

obj.regular();
// Regular: Object
// Arrow: Object

/*
Arrow functions DON'T have their own 'this':
- Inherit 'this' from enclosing scope (lexically)
- 'this' cannot be changed

The arrow function's 'this' is determined at DEFINITION time,
not CALL time.

Execution Context for arrow:
{
    ThisBinding: <inherited from regular()>
}
*/
```

### **11.2 This in Global Context**

#### **Browser Environment:**

```javascript
console.log(this);  // Window object

var globalVar = "global";
this.anotherVar = "another";

console.log(window.globalVar);   // "global"
console.log(window.anotherVar);  // "another"
console.log(this.globalVar);     // "global"
console.log(this.anotherVar);    // "another"

/*
═══════════════════════════════════════════════════════════
BROWSER GLOBAL CONTEXT
═══════════════════════════════════════════════════════════

In browser:
- Global context: this = window
- var creates properties on window
- let/const do NOT create properties on window

┌─────────────────────────────────┐
│ Global Execution Context        │
│ ThisBinding: window             │
│                                 │
│ VariableEnvironment:            │
│   globalVar: "global"           │
│                                 │
│ window object:                  │
│   globalVar: "global"  ← var    │
│   anotherVar: "another" ← this  │
└─────────────────────────────────┘

let globalLet = "let";
console.log(window.globalLet);  // undefined
console.log(this.globalLet);    // undefined
*/

// Strict mode in global context
'use strict';
console.log(this);  // Still Window in global context

function strictFunction() {
    'use strict';
    console.log(this);  // undefined
}

strictFunction();

/*
Strict mode changes:
- Global context: this = window (unchanged)
- Function context: this = undefined (changed!)
*/
```

#### **Node.js Environment:**

```javascript
// In Node.js module:
console.log(this);  // {} (empty object, module.exports)
console.log(this === module.exports);  // true

var globalVar = "global";
console.log(global.globalVar);  // undefined (not on global!)

// To make truly global:
global.myGlobal = "truly global";

function checkThis() {
    console.log(this);  // undefined (in strict mode by default)
}

checkThis();

/*
═══════════════════════════════════════════════════════════
NODE.JS GLOBAL CONTEXT
═══════════════════════════════════════════════════════════

Node.js differences:
1. Top-level code runs in MODULE scope (not global)
2. 'this' at top level = module.exports
3. 'global' is the global object (like window)
4. var doesn't create global properties

┌─────────────────────────────────┐
│ Module Scope                    │
│ ThisBinding: module.exports     │
│                                 │
│ Variables are module-scoped:    │
│   globalVar: "global"           │
│                                 │
│ global object:                  │
│   (doesn't have globalVar)      │
└─────────────────────────────────┘
*/
```

#### **Universal Access (globalThis):**

```javascript
// ES2020: globalThis works everywhere
console.log(globalThis);

// Browser: globalThis === window
// Node.js: globalThis === global
// Web Worker: globalThis === self

function universal() {
    console.log(globalThis);  // Always the global object
}

/*
═══════════════════════════════════════════════════════════
GLOBALHIS (ES2020)
═══════════════════════════════════════════════════════════

Before globalThis:
const global = typeof window !== 'undefined' ? window :
               typeof global !== 'undefined' ? global :
               typeof self !== 'undefined' ? self : {};

After globalThis:
const global = globalThis;  // Always works!

Benefits:
✓ Universal across all environments
✓ No environment detection needed
✓ More maintainable code
✓ Future-proof
*/
```

### **11.3 This in Function Context**

#### **Regular Function Calls:**

```javascript
function regularFunction() {
    console.log("Non-strict:", this);
}

regularFunction();  // Window (non-strict)

function strictFunction() {
    'use strict';
    console.log("Strict:", this);
}

strictFunction();  // undefined (strict)

/*
═══════════════════════════════════════════════════════════
FUNCTION CALL 'THIS' DETERMINATION
═══════════════════════════════════════════════════════════

Call Site Analysis:
regularFunction()
↑ No context object

Resolution:
1. Is it strict mode? No
2. Is there a context object? No
3. Default binding: this = global object

┌─────────────────────────────────┐
│ regularFunction EC              │
│ ThisBinding: window             │
└─────────────────────────────────┘

Call Site Analysis:
strictFunction()
↑ No context object

Resolution:
1. Is it strict mode? Yes
2. Is there a context object? No
3. Default binding (strict): this = undefined

┌─────────────────────────────────┐
│ strictFunction EC               │
│ ThisBinding: undefined          │
└─────────────────────────────────┘
*/
```

#### **Nested Function 'this':**

```javascript
const obj = {
    name: "Object",
    method: function() {
        console.log("Method this:", this.name);  // "Object"
        
        function nestedFunction() {
            console.log("Nested this:", this.name);  // undefined
        }
        
        nestedFunction();  // Regular function call!
    }
};

obj.method();

/*
═══════════════════════════════════════════════════════════
COMMON MISTAKE: LOST 'THIS' IN NESTED FUNCTIONS
═══════════════════════════════════════════════════════════

Call Site Analysis:

1. obj.method()
   ↑   ↑ Method call
   context

   method's this = obj ✓

2. nestedFunction()
   ↑ Regular function call, no context

   nestedFunction's this = global/undefined ✗

Visual:
┌─────────────────────────────────┐
│ method() EC                     │
│ ThisBinding: obj                │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ nestedFunction() EC         │ │
│ │ ThisBinding: global/undef   │ │
│ │ (NOT inherited from method!)│ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘

Each function has its own 'this'!

═══════════════════════════════════════════════════════════
SOLUTIONS
═══════════════════════════════════════════════════════════
*/

// Solution 1: Save 'this' reference
const obj1 = {
    name: "Object",
    method: function() {
        const self = this;  // Save reference
        
        function nestedFunction() {
            console.log("Nested this:", self.name);  // "Object" ✓
        }
        
        nestedFunction();
    }
};

// Solution 2: Arrow function
const obj2 = {
    name: "Object",
    method: function() {
        const nestedFunction = () => {
            console.log("Nested this:", this.name);  // "Object" ✓
        };
        
        nestedFunction();
    }
};

// Solution 3: bind
const obj3 = {
    name: "Object",
    method: function() {
        function nestedFunction() {
            console.log("Nested this:", this.name);
        }
        
        nestedFunction.call(this);  // or .bind(this)()
    }
};
```

### **11.4 This in Method Context**

#### **Object Method Calls:**

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
    fullName: function() {
        return this.firstName + " " + this.lastName;
    },
    greet: function() {
        console.log("Hello, " + this.fullName());
    }
};

person.greet();  // "Hello, John Doe"

/*
═══════════════════════════════════════════════════════════
METHOD CALL 'THIS'
═══════════════════════════════════════════════════════════

Call Site: person.greet()
           ↑      ↑
         object  method

Rule: Object to the left of the dot becomes 'this'

greet() Execution Context:
{
    ThisBinding: person
}

Inside greet:
- this = person
- this.fullName() = person.fullName()
- Inside fullName(), this is also person
*/
```

#### **Implicit Binding Loss:**

```javascript
const person = {
    name: "John",
    greet: function() {
        console.log("Hello, " + this.name);
    }
};

// Works fine
person.greet();  // "Hello, John"

// Context loss!
const greetFunction = person.greet;
greetFunction();  // "Hello, undefined"

// Also context loss in callbacks
setTimeout(person.greet, 1000);  // "Hello, undefined"

/*
═══════════════════════════════════════════════════════════
WHY CONTEXT LOSS?
═══════════════════════════════════════════════════════════

person.greet()
↑      ↑
object method → this = person ✓

greetFunction()
↑ No object context → this = global/undefined ✗

Visual:
┌──────────────────────────────────────┐
│ greetFunction = person.greet         │
│ ↑ Reference to function, NOT method  │
│                                      │
│ When called: greetFunction()         │
│ No object context!                   │
│ this = global/undefined              │
└──────────────────────────────────────┘

═══════════════════════════════════════════════════════════
FIXES
═══════════════════════════════════════════════════════════
*/

// Fix 1: Wrapper function
setTimeout(function() {
    person.greet();  // Called as method ✓
}, 1000);

// Fix 2: Arrow function
setTimeout(() => person.greet(), 1000);

// Fix 3: bind
const boundGreet = person.greet.bind(person);
setTimeout(boundGreet, 1000);  // "Hello, John" ✓

// Fix 4: Class with arrow function property
class Person {
    constructor(name) {
        this.name = name;
        // Arrow function as property
        this.greet = () => {
            console.log("Hello, " + this.name);
        };
    }
}

const john = new Person("John");
setTimeout(john.greet, 1000);  // "Hello, John" ✓
// Arrow function 'this' is bound at creation
```

#### **Chained Method Calls:**

```javascript
const calculator = {
    value: 0,
    add: function(num) {
        this.value += num;
        return this;  // Return this for chaining
    },
    subtract: function(num) {
        this.value -= num;
        return this;
    },
    multiply: function(num) {
        this.value *= num;
        return this;
    },
    getValue: function() {
        return this.value;
    }
};

const result = calculator
    .add(10)
    .subtract(5)
    .multiply(2)
    .getValue();

console.log(result);  // 10

/*
═══════════════════════════════════════════════════════════
METHOD CHAINING AND 'THIS'
═══════════════════════════════════════════════════════════

Step-by-step execution:

1. calculator.add(10)
   - this = calculator
   - this.value = 0 + 10 = 10
   - return this (calculator)

2. (return value).subtract(5)
   - calculator.subtract(5)
   - this = calculator
   - this.value = 10 - 5 = 5
   - return this (calculator)

3. (return value).multiply(2)
   - calculator.multiply(2)
   - this = calculator
   - this.value = 5 * 2 = 10
   - return this (calculator)

4. (return value).getValue()
   - calculator.getValue()
   - return this.value (10)

Each method call maintains 'this' = calculator
*/
```

### **11.5 This in Constructor Functions**

#### **Constructor Function 'this':**

```javascript
function Person(firstName, lastName) {
    // 'new' creates empty object and sets 'this' to it
    this.firstName = firstName;
    this.lastName = lastName;
    
    this.fullName = function() {
        return this.firstName + " " + this.lastName;
    };
    
    // Implicit: return this;
}

const john = new Person("John", "Doe");
console.log(john.fullName());  // "John Doe"

/*
═══════════════════════════════════════════════════════════
WHAT HAPPENS WITH 'NEW'
═══════════════════════════════════════════════════════════

new Person("John", "Doe")

Step 1: Create empty object
  {} created

Step 2: Set prototype
  {}.__proto__ = Person.prototype

Step 3: Bind 'this'
  this = {}

Step 4: Execute constructor
  this.firstName = "John"
  this.lastName = "Doe"
  this.fullName = function() { ... }
  
  Object now: {
    firstName: "John",
    lastName: "Doe",
    fullName: [Function]
  }

Step 5: Return
  return this (implicit)
  
Result: john = {
  firstName: "John",
  lastName: "Doe",
  fullName: [Function]
}

═══════════════════════════════════════════════════════════
CONSTRUCTOR WITHOUT 'NEW' (MISTAKE)
═══════════════════════════════════════════════════════════
*/

function PersonNoNew(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

// Forgot 'new'!
const mistake = PersonNoNew("John", "Doe");

console.log(mistake);  // undefined
console.log(window.firstName);  // "John" (Oops! Global!)
console.log(window.lastName);   // "Doe" (Oops! Global!)

/*
Without 'new':
- No object created
- this = global/undefined
- Properties set on global object!
- Function returns undefined

═══════════════════════════════════════════════════════════
PROTECTION AGAINST MISSING 'NEW'
═══════════════════════════════════════════════════════════
*/

function SafePerson(firstName, lastName) {
    // Check if called with 'new'
    if (!(this instanceof SafePerson)) {
        return new SafePerson(firstName, lastName);
    }
    
    this.firstName = firstName;
    this.lastName = lastName;
}

const safe1 = new SafePerson("John", "Doe");  // Works
const safe2 = SafePerson("Jane", "Doe");      // Also works!

// Or use ES6 new.target
function ModernPerson(firstName, lastName) {
    if (!new.target) {
        throw new Error("Must be called with new");
    }
    
    this.firstName = firstName;
    this.lastName = lastName;
}
```

#### **Constructor with Explicit Return:**

```javascript
function PersonWithReturn(name) {
    this.name = name;
    
    // Return object: overrides 'this'
    return {
        name: "Overridden",
        type: "custom"
    };
}

const p1 = new PersonWithReturn("John");
console.log(p1.name);  // "Overridden"
console.log(p1.type);  // "custom"

function PersonWithPrimitiveReturn(name) {
    this.name = name;
    
    // Return primitive: ignored, returns 'this'
    return "ignored";
}

const p2 = new PersonWithPrimitiveReturn("John");
console.log(p2.name);  // "John"
console.log(p2);       // PersonWithPrimitiveReturn { name: "John" }

/*
═══════════════════════════════════════════════════════════
RETURN RULES WITH 'NEW'
═══════════════════════════════════════════════════════════

If constructor explicitly returns:
1. Object → returned object used (this ignored)
2. Primitive → return ignored, this used
3. Nothing → this returned (normal case)

Examples:

return { x: 1 };        // Object → returns { x: 1 }
return [1, 2, 3];       // Object → returns [1, 2, 3]
return function() {};   // Object → returns function

return "string";        // Primitive → returns this
return 123;             // Primitive → returns this
return true;            // Primitive → returns this
return null;            // Special: returns this
return undefined;       // Returns this

// (nothing)            // Returns this
*/
```

### **11.6 This in Arrow Functions**

#### **Arrow Function Lexical 'this':**

```javascript
const obj = {
    name: "Object",
    
    regularMethod: function() {
        console.log("Regular:", this.name);  // "Object"
        
        // Arrow function inherits 'this'
        const arrow = () => {
            console.log("Arrow:", this.name);  // "Object"
        };
        
        arrow();
        
        // Even if we try to change 'this'
        arrow.call({ name: "Other" });  // Still "Object"
    },
    
    arrowMethod: () => {
        console.log("Arrow method:", this.name);  // undefined
    }
};

obj.regularMethod();
obj.arrowMethod();

/*
═══════════════════════════════════════════════════════════
ARROW FUNCTION 'THIS' RULES
═══════════════════════════════════════════════════════════

1. Arrow functions DON'T have their own 'this'
2. They inherit 'this' from enclosing lexical scope
3. 'this' is determined at DEFINITION time, not CALL time
4. Cannot be changed with call/apply/bind
5. Cannot be used as constructors

Visual:

┌─────────────────────────────────┐
│ obj.regularMethod() EC          │
│ ThisBinding: obj                │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ arrow() EC                  │ │
│ │ ThisBinding: INHERITED      │ │
│ │ (from regularMethod)        │ │
│ │ = obj                       │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘

Arrow function defined in regularMethod:
- Captures 'this' from regularMethod
- this = obj (from regularMethod's context)
- Immutable (cannot be changed)

Arrow function as object method:
- Defined at object literal level
- Enclosing scope is global/module
- this = global/undefined
- NOT what you usually want!
*/
```

#### **Arrow Functions in Different Contexts:**

```javascript
// Context 1: Global arrow function
const globalArrow = () => {
    console.log(this);
};

globalArrow();  // Window (browser) or {} (Node.js module)

/*
Enclosing scope: Global
'this' inherited from: Global context
*/

// Context 2: Arrow in regular function
function regularFunction() {
    const arrow = () => {
        console.log(this);
    };
    
    arrow();
}

regularFunction();  // Global/undefined

/*
Enclosing scope: regularFunction
'this' inherited from: regularFunction's this
regularFunction called as regular function → this = global/undefined
*/

// Context 3: Arrow in method
const obj = {
    method: function() {
        const arrow = () => {
            console.log(this);
        };
        
        arrow();
    }
};

obj.method();  // obj

/*
Enclosing scope: method function
'this' inherited from: method's this
method called as obj.method() → this = obj
*/

// Context 4: Arrow in constructor
function Constructor() {
    this.value = 42;
    
    this.arrow = () => {
        console.log(this.value);
    };
}

const instance = new Constructor();
instance.arrow();  // 42

const detached = instance.arrow;
detached();  // Still 42! (this permanently bound)

/*
Enclosing scope: Constructor function
'this' inherited from: Constructor's this
Constructor called with new → this = new instance
Arrow function bound to that instance forever!
*/

/*
═══════════════════════════════════════════════════════════
ARROW FUNCTION BENEFITS
═══════════════════════════════════════════════════════════
*/

// Benefit 1: Callbacks retain context
class Timer {
    constructor() {
        this.seconds = 0;
    }
    
    start() {
        // Arrow function in callback
        setInterval(() => {
            this.seconds++;
            console.log(this.seconds);
        }, 1000);
    }
}

const timer = new Timer();
timer.start();  // 1, 2, 3, ... (works!)

// Benefit 2: Event handlers
class Button {
    constructor(label) {
        this.label = label;
        this.clicks = 0;
    }
    
    handleClick = () => {
        this.clicks++;
        console.log(`${this.label}: ${this.clicks}`);
    }
}

const btn = new Button("Submit");
document.querySelector('button').onclick = btn.handleClick;
// Click works! 'this' is always btn instance

// Benefit 3: Array methods
const numbers = [1, 2, 3, 4, 5];

const multiplier = {
    factor: 2,
    
    multiply: function() {
        return numbers.map(n => n * this.factor);
    }
};

console.log(multiplier.multiply());  // [2, 4, 6, 8, 10]
// Arrow function: 'this' = multiplier ✓

/*
═══════════════════════════════════════════════════════════
ARROW FUNCTION LIMITATIONS
═══════════════════════════════════════════════════════════
*/

// Limitation 1: Cannot be constructor
const ArrowConstructor = (name) => {
    this.name = name;
};

// new ArrowConstructor("John");  // TypeError

// Limitation 2: No 'arguments' object
const arrowArgs = () => {
    console.log(arguments);  // ReferenceError
};

// Use rest parameters instead:
const arrowRest = (...args) => {
    console.log(args);  // Works!
};

// Limitation 3: No prototype
const arrow = () => {};
console.log(arrow.prototype);  // undefined

// Limitation 4: Cannot use 'super'
class Parent {
    constructor() {
        this.type = "parent";
    }
}

class Child extends Parent {
    constructor() {
        super();
        // const method = () => {
        //     super.constructor();  // SyntaxError
        // };
    }
}
```

### **11.7 This in Event Handlers**

#### **DOM Event Handlers:**

```javascript
// Example HTML: <button id="myButton">Click me</button>

const button = document.getElementById('myButton');

// Regular function: 'this' = element
button.addEventListener('click', function(event) {
    console.log(this);  // <button> element
    console.log(this.textContent);  // "Click me"
    this.style.backgroundColor = 'blue';
});

// Arrow function: 'this' from enclosing scope
button.addEventListener('click', (event) => {
    console.log(this);  // Window/undefined (not button!)
    // this.style.backgroundColor = 'blue';  // Error!
    
    // Use event.currentTarget instead:
    event.currentTarget.style.backgroundColor = 'blue';
});

/*
═══════════════════════════════════════════════════════════
EVENT HANDLER 'THIS' RULES
═══════════════════════════════════════════════════════════

Regular function:
- this = element that handler is attached to
- this = event.currentTarget
- Set by browser's event dispatch

Arrow function:
- this = inherited from enclosing scope
- NOT the element
- Use event.currentTarget to access element
*/
```

#### **Event Handlers in Classes:**

```javascript
class ClickCounter {
    constructor(buttonId) {
        this.count = 0;
        this.button = document.getElementById(buttonId);
        
        // Method 1: Arrow function property (recommended)
        this.handleClickArrow = () => {
            this.count++;
            console.log(`Arrow: ${this.count}`);
        };
        
        // Attach handlers
        this.attachHandlers();
    }
    
    // Method 2: Regular method
    handleClickRegular(event) {
        this.count++;
        console.log(`Regular: ${this.count}`);
    }
    
    attachHandlers() {
        // This works (arrow function)
        this.button.addEventListener('click', this.handleClickArrow);
        
        // This doesn't work (lost context)
        // this.button.addEventListener('click', this.handleClickRegular);
        
        // Fix 1: Bind in constructor
        // this.handleClickRegular = this.handleClickRegular.bind(this);
        // this.button.addEventListener('click', this.handleClickRegular);
        
        // Fix 2: Arrow wrapper
        // this.button.addEventListener('click', (e) => {
        //     this.handleClickRegular(e);
        // });
        
        // Fix 3: Bind inline
        // this.button.addEventListener('click', 
        //     this.handleClickRegular.bind(this));
    }
}

const counter = new ClickCounter('myButton');

/*
═══════════════════════════════════════════════════════════
CLASS EVENT HANDLERS BEST PRACTICES
═══════════════════════════════════════════════════════════

✓ RECOMMENDED: Arrow function as class property
class Component {
    handleClick = () => {
        // 'this' always bound to instance
    }
}

Pros:
- Automatically bound
- Clean syntax
- Easy to remove listener
- No memory leaks from repeated binding

Cons:
- Each instance gets own function copy
- Slightly more memory per instance

✗ AVOID: Regular method without binding
class Component {
    handleClick() {
        // 'this' context lost!
    }
    
    attach() {
        button.onclick = this.handleClick;  // Wrong!
    }
}

✓ ACCEPTABLE: Bind in constructor
class Component {
    constructor() {
        this.handleClick = this.handleClick.bind(this);
    }
    
    handleClick() {
        // 'this' bound to instance
    }
}
*/
```

### **11.8 This in Strict Mode vs Non-Strict Mode**

#### **Strict Mode Impact on 'this':**

```javascript
// Non-strict mode
function nonStrict() {
    console.log(this);
}

nonStrict();  // Window (global object)

// Strict mode
function strict() {
    'use strict';
    console.log(this);
}

strict();  // undefined

/*
═══════════════════════════════════════════════════════════
STRICT MODE CHANGES TO 'THIS'
═══════════════════════════════════════════════════════════

╔════════════════════╦══════════════╦══════════════╗
║   Context          ║  Non-Strict  ║    Strict    ║
╠════════════════════╬══════════════╬══════════════╣
║ Global             ║ Global obj   ║  Global obj  ║
║ Regular function   ║ Global obj   ║  undefined   ║
║ Method             ║ Object       ║  Object      ║
║ Constructor (new)  ║ New obj      ║  New obj     ║
║ call/apply/bind    ║ Provided obj ║  Provided obj║
║ Arrow function     ║ Lexical      ║  Lexical     ║
╚════════════════════╩══════════════╩══════════════╝

Key difference:
- Regular function calls: undefined (strict) vs global (non-strict)
*/
```

#### **Detailed Strict Mode Examples:**

```javascript
'use strict';

// Example 1: Function calls
function func() {
    console.log(this);
}

func();  // undefined (not global!)

// Example 2: Still works with context
const obj = {
    method: func
};

obj.method();  // obj (still works!)

// Example 3: Prevents accidental globals
function createGlobal() {
    // Non-strict: creates global variable
    // Strict: ReferenceError
    // accidentalGlobal = "oops";
}

// Example 4: call with primitive
function showThis() {
    console.log(this);
    console.log(typeof this);
}

// Non-strict mode
showThis.call(5);      // Number {5} (boxed)
showThis.call("str");  // String {"str"} (boxed)
showThis.call(true);   // Boolean {true} (boxed)

// Strict mode
('use strict');
showThis.call(5);      // 5 (not boxed)
showThis.call("str");  // "str" (not boxed)
showThis.call(true);   // true (not boxed)
showThis.call(null);   // null (not converted)
showThis.call(undefined); // undefined (not converted)

/*
═══════════════════════════════════════════════════════════
BOXING IN NON-STRICT MODE
═══════════════════════════════════════════════════════════

Non-strict mode automatically boxes primitives:

showThis.call(5)
↓ Boxing
showThis.call(new Number(5))

This is called "boxing" or "wrapping"

Strict mode: NO BOXING
- Primitives stay primitives
- null/undefined stay null/undefined
- More predictable behavior
*/
```

---

## **12. CONTROLLING 'THIS'**

### **12.1 call() Method**

The **`call()`** method calls a function with a specified `this` value and arguments provided individually.

#### **call() Basics:**

```javascript
function greet(greeting, punctuation) {
    console.log(greeting + ", " + this.name + punctuation);
}

const person1 = { name: "John" };
const person2 = { name: "Jane" };

// Call with different contexts
greet.call(person1, "Hello", "!");  // "Hello, John!"
greet.call(person2, "Hi", ".");     // "Hi, Jane."

/*
═══════════════════════════════════════════════════════════
CALL() SYNTAX
═══════════════════════════════════════════════════════════

function.call(thisArg, arg1, arg2, ...)

Parameters:
- thisArg: Value of 'this' inside function
- arg1, arg2, ...: Arguments passed to function

Returns:
- Result of calling function

Process:
1. Set function's 'this' to thisArg
2. Execute function with provided arguments
3. Return function's return value

greet.call(person1, "Hello", "!")

Step 1: Create execution context
  ThisBinding: person1

Step 2: Pass arguments
  greeting: "Hello"
  punctuation: "!"

Step 3: Execute function body
  console.log("Hello, " + person1.name + "!")
  Output: "Hello, John!"
*/
```

#### **call() Detailed Examples:**

```javascript
// Example 1: Method borrowing
const person = {
    name: "John",
    greet: function() {
        console.log("Hello, " + this.name);
    }
};

const anotherPerson = { name: "Jane" };

// Borrow person's method
person.greet.call(anotherPerson);  // "Hello, Jane"

/*
Method borrowing:
- Take method from one object
- Use it with another object
- 'this' set to the other object
*/

// Example 2: Constructor chaining
function Animal(name) {
    this.name = name;
    this.type = "animal";
}

function Dog(name, breed) {
    // Call parent constructor
    Animal.call(this, name);
    this.breed = breed;
}

const dog = new Dog("Buddy", "Golden Retriever");
console.log(dog.name);   // "Buddy"
console.log(dog.type);   // "animal"
console.log(dog.breed);  // "Golden Retriever"

/*
Constructor chaining process:

1. new Dog() creates empty object
2. this = empty object
3. Animal.call(this, name) calls Animal with this = empty object
4. Animal sets this.name and this.type
5. Dog sets this.breed
6. Return this

Result: {
    name: "Buddy",
    type: "animal",
    breed: "Golden Retriever"
}
*/

// Example 3: Array-like object manipulation
function logArguments() {
    // 'arguments' is array-like, not real array
    console.log(Array.isArray(arguments));  // false
    
    // Borrow Array methods
    const args = Array.prototype.slice.call(arguments);
    console.log(Array.isArray(args));  // true
    
    // Or use Array.from (modern)
    const args2 = Array.from(arguments);
    
    return args;
}

logArguments(1, 2, 3, 4);

/*
Array method borrowing:
- arguments is array-like (has length, indexed)
- NOT a real array (no array methods)
- Borrow array methods with call
- Array.prototype.slice.call(arguments)
  → calls slice with this = arguments
  → returns real array
*/

// Example 4: Finding max in array-like
function findMax() {
    return Math.max.call(null, ...arguments);
    // Or: Math.max.apply(null, arguments)
}

console.log(findMax(1, 5, 3, 9, 2));  // 9

/*
Math.max.call(null, 1, 5, 3, 9, 2)
- Math.max doesn't use 'this', so null is fine
- Arguments passed individually
- Returns 9
*/
```

#### **call() Advanced Patterns:**

```javascript
// Pattern 1: Generic utility functions
const arrayUtils = {
    forEach: function(callback, thisArg) {
        for (let i = 0; i < this.length; i++) {
            callback.call(thisArg, this[i], i, this);
        }
    },
    
    map: function(callback, thisArg) {
        const result = [];
        for (let i = 0; i < this.length; i++) {
            result.push(callback.call(thisArg, this[i], i, this));
        }
        return result;
    }
};

// Use with array-like object
const arrayLike = {
    0: 'a',
    1: 'b',
    2: 'c',
    length: 3
};

arrayUtils.forEach.call(arrayLike, function(item) {
    console.log(item);
});
// Output: a, b, c

// Pattern 2: Polymorphism
function processData(data) {
    // Different processing based on type
    const processors = {
        string: function() {
            return this.toUpperCase();
        },
        number: function() {
            return this * 2;
        },
        boolean: function() {
            return !this;
        }
    };
    
    const processor = processors[typeof data];
    return processor ? processor.call(data) : data;
}

console.log(processData("hello"));  // "HELLO"
console.log(processData(5));        // 10
console.log(processData(true));     // false

// Pattern 3: Function composition with context
function compose(...fns) {
    return function(...args) {
        return fns.reduceRight((result, fn) => {
            return Array.isArray(result)
                ? fn.call(this, ...result)
                : fn.call(this, result);
        }, args);
    };
}

const obj = { multiplier: 2 };

const double = function(x) {
    return x * this.multiplier;
};

const addTen = function(x) {
    return x + 10;
};

const composed = compose(addTen, double);
console.log(composed.call(obj, 5));  // (5 * 2) + 10 = 20
```

### **12.2 apply() Method**

The **`apply()`** method is similar to `call()`, but accepts arguments as an array.

#### **apply() Basics:**

```javascript
function greet(greeting, punctuation) {
    console.log(greeting + ", " + this.name + punctuation);
}

const person = { name: "John" };

// apply with array of arguments
greet.apply(person, ["Hello", "!"]);  // "Hello, John!"

// call with individual arguments
greet.call(person, "Hello", "!");     // "Hello, John!"

/*
═══════════════════════════════════════════════════════════
APPLY() VS CALL()
═══════════════════════════════════════════════════════════

Syntax:
function.call(thisArg, arg1, arg2, ...)
function.apply(thisArg, [arg1, arg2, ...])

The ONLY difference:
- call: arguments passed individually
- apply: arguments passed as array

When to use each:
- call: When you know arguments ahead of time
- apply: When arguments are already in an array
*/
```

#### **apply() Use Cases:**

```javascript
// Use Case 1: Math.max with array
const numbers = [5, 6, 2, 3, 7];

// Can't do: Math.max(numbers) → NaN
// Need: Math.max(5, 6, 2, 3, 7)

const max = Math.max.apply(null, numbers);
console.log(max);  // 7

// Modern alternative: spread operator
const max2 = Math.max(...numbers);
console.log(max2);  // 7

/*
apply is perfect when:
- Function expects individual arguments
- You have arguments in an array
- Before ES6 spread operator

Math.max.apply(null, [5, 6, 2, 3, 7])
↓ Equivalent to
Math.max(5, 6, 2, 3, 7)
*/

// Use Case 2: Array concatenation (legacy)
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];

// Old way:
Array.prototype.push.apply(array1, array2);
console.log(array1);  // [1, 2, 3, 4, 5, 6]

// Modern way:
array1.push(...array2);

/*
Array.prototype.push.apply(array1, array2)
↓ Equivalent to
array1.push(4, 5, 6)
*/

// Use Case 3: Constructor with array of arguments
function Person(firstName, lastName, age) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.age = age;
}

const args = ["John", "Doe", 30];

// Can't use apply with 'new' directly!
// const person = new Person.apply(null, args); // Error!

// Solution 1: bind
const BoundPerson = Person.bind(null, ...args);
const person = new BoundPerson();

// Solution 2: Factory function
function createPerson(...args) {
    return new Person(...args);
}

const person2 = createPerson(...args);

console.log(person);   // Person { firstName: "John", lastName: "Doe", age: 30 }
console.log(person2);  // Person { firstName: "John", lastName: "Doe", age: 30 }
```

#### **apply() with Variable Arguments:**

```javascript
// Example: Logging utility
const logger = {
    prefix: "[LOG]",
    
    log: function() {
        const args = Array.prototype.slice.call(arguments);
        const message = this.prefix + " " + args.join(" ");
        console.log(message);
    }
};

// Use apply to pass variable arguments
function logWithTimestamp() {
    const timestamp = new Date().toISOString();
    const args = [timestamp].concat(Array.prototype.slice.call(arguments));
    
    logger.log.apply(logger, args);
}

logWithTimestamp("User logged in");
// [LOG] 2024-01-01T12:00:00.000Z User logged in

logWithTimestamp("Error occurred:", "File not found");
// [LOG] 2024-01-01T12:00:00.000Z Error occurred: File not found

// Example: Flexible calculator
const calculator = {
    operation: "add",
    
    calculate: function() {
        const numbers = Array.prototype.slice.call(arguments);
        
        switch(this.operation) {
            case "add":
                return numbers.reduce((a, b) => a + b, 0);
            case "multiply":
                return numbers.reduce((a, b) => a * b, 1);
            case "max":
                return Math.max.apply(null, numbers);
            case "min":
                return Math.min.apply(null, numbers);
        }
    }
};

const numbers = [1, 2, 3, 4, 5];

calculator.operation = "add";
console.log(calculator.calculate.apply(calculator, numbers));  // 15

calculator.operation = "multiply";
console.log(calculator.calculate.apply(calculator, numbers));  // 120

calculator.operation = "max";
console.log(calculator.calculate.apply(calculator, numbers));  // 5
```

### **12.3 bind() Method**

The **`bind()`** method creates a new function with a permanently bound `this` value and optional preset arguments.

#### **bind() Basics:**

```javascript
function greet(greeting, punctuation) {
    console.log(greeting + ", " + this.name + punctuation);
}

const person = { name: "John" };

// Create bound function
const greetJohn = greet.bind(person);

greetJohn("Hello", "!");  // "Hello, John!"
greetJohn("Hi", ".");     // "Hi, John."

// 'this' is permanently bound
greetJohn.call({ name: "Jane" }, "Hey", "?");  // Still "Hey, John!"

/*
═══════════════════════════════════════════════════════════
BIND() CHARACTERISTICS
═══════════════════════════════════════════════════════════

Key differences from call/apply:
1. Returns NEW function (doesn't execute immediately)
2. 'this' is PERMANENTLY bound (cannot be changed)
3. Can preset arguments (partial application)

Syntax:
const boundFn = function.bind(thisArg, arg1, arg2, ...)

Process:
1. Create new function
2. Set its internal [[BoundThis]] to thisArg
3. Set its internal [[BoundArgs]] to provided args
4. When called, use [[BoundThis]] and prepend [[BoundArgs]]

greet.bind(person)
↓ Creates
function boundGreet() {
    return greet.apply(person, arguments);
}
*/
```

#### **bind() Use Cases:**

```javascript
// Use Case 1: Event handlers
class Button {
    constructor(label) {
        this.label = label;
        this.clicks = 0;
    }
    
    handleClick() {
        this.clicks++;
        console.log(`${this.label} clicked ${this.clicks} times`);
    }
    
    attachToElement(element) {
        // Without bind: 'this' would be the element
        element.addEventListener('click', this.handleClick.bind(this));
    }
}

const submitButton = new Button("Submit");
// submitButton.attachToElement(document.getElementById('submit'));

/*
Without bind:
element.addEventListener('click', this.handleClick)
→ When clicked: this = element ✗

With bind:
element.addEventListener('click', this.handleClick.bind(this))
→ When clicked: this = Button instance ✓
*/

// Use Case 2: setTimeout/setInterval
const timer = {
    seconds: 0,
    
    start: function() {
        // Without bind:
        // setInterval(this.tick, 1000); // 'this' would be global
        
        // With bind:
        setInterval(this.tick.bind(this), 1000);
    },
    
    tick: function() {
        this.seconds++;
        console.log(this.seconds);
    }
};

// timer.start();  // 1, 2, 3, ...

// Use Case 3: Callback functions
const processor = {
    prefix: "Processed: ",
    
    processArray: function(array) {
        return array.map(this.addPrefix.bind(this));
    },
    
    addPrefix: function(item) {
        return this.prefix + item;
    }
};

const result = processor.processArray(["A", "B", "C"]);
console.log(result);  // ["Processed: A", "Processed: B", "Processed: C"]

/*
Without bind:
array.map(this.addPrefix)
→ addPrefix called with this = undefined ✗

With bind:
array.map(this.addPrefix.bind(this))
→ addPrefix called with this = processor ✓
*/

// Use Case 4: Method extraction
const person = {
    name: "John",
    greet: function() {
        console.log("Hello, " + this.name);
    }
};

// Extract method
const greet = person.greet;
greet();  // "Hello, undefined" ✗

// Extract with bind
const greetBound = person.greet.bind(person);
greetBound();  // "Hello, John" ✓

// Use in different context
setTimeout(person.greet, 1000);        // "Hello, undefined" ✗
setTimeout(person.greet.bind(person), 1000); // "Hello, John" ✓
```

#### **Partial Application with bind():**

```javascript
// Partial application: preset some arguments
function multiply(a, b) {
    return a * b;
}

// Create specialized versions
const double = multiply.bind(null, 2);
const triple = multiply.bind(null, 3);

console.log(double(5));  // 10 (2 * 5)
console.log(triple(5));  // 15 (3 * 5)

/*
multiply.bind(null, 2)
Creates: function(b) { return multiply(2, b); }

When double(5) is called:
→ multiply(2, 5)
→ return 10
*/

// Example: Logging with prefix
function log(level, message) {
    console.log(`[${level}] ${message}`);
}

const info = log.bind(null, "INFO");
const error = log.bind(null, "ERROR");
const warn = log.bind(null, "WARN");

info("Application started");   // [INFO] Application started
error("File not found");        // [ERROR] File not found
warn("Deprecated API used");    // [WARN] Deprecated API used

// Example: Preset multiple arguments
function greet(greeting, name, punctuation) {
    console.log(`${greeting}, ${name}${punctuation}`);
}

const greetJohn = greet.bind(null, "Hello", "John");
greetJohn("!");  // "Hello, John!"
greetJohn(".");  // "Hello, John."

const sayHello = greet.bind(null, "Hello");
sayHello("Jane", "!");  // "Hello, Jane!"
sayHello("Bob", "?");   // "Hello, Bob?"

/*
Argument merging:

greet.bind(null, "Hello", "John")
→ greetJohn("!")
→ greet("Hello", "John", "!")

greet.bind(null, "Hello")
→ sayHello("Jane", "!")
→ greet("Hello", "Jane", "!")
*/
```

#### **bind() Advanced Patterns:**

```javascript
// Pattern 1: Currying with bind
function volume(length, width, height) {
    return length * width * height;
}

const volumeWith10 = volume.bind(null, 10);
const volumeWith10And20 = volumeWith10.bind(null, 20);

console.log(volumeWith10And20(30));  // 6000 (10 * 20 * 30)

/*
Currying chain:
volume(l, w, h)
→ volumeWith10(w, h) = volume(10, w, h)
→ volumeWith10And20(h) = volume(10, 20, h)
→ volumeWith10And20(30) = volume(10, 20, 30) = 6000
*/

// Pattern 2: Method binding in constructor
class Component {
    constructor(name) {
        this.name = name;
        
        // Bind all methods in constructor
        this.handleClick = this.handleClick.bind(this);
        this.handleHover = this.handleHover.bind(this);
    }
    
    handleClick() {
        console.log(`${this.name} clicked`);
    }
    
    handleHover() {
        console.log(`${this.name} hovered`);
    }
}

const comp = new Component("Button");
const click = comp.handleClick;
click();  // "Button clicked" ✓ (bound in constructor)

// Pattern 3: Polyfill for bind (educational)
if (!Function.prototype.bind) {
    Function.prototype.bind = function(thisArg) {
        const fn = this;
        const args = Array.prototype.slice.call(arguments, 1);
        
        return function() {
            const allArgs = args.concat(
                Array.prototype.slice.call(arguments)
            );
            return fn.apply(thisArg, allArgs);
        };
    };
}

/*
How bind polyfill works:

function multiply(a, b) { return a * b; }
const double = multiply.bind(null, 2);

Creates:
function boundMultiply() {
    const allArgs = [2].concat(Array.from(arguments));
    return multiply.apply(null, allArgs);
}

double(5) → boundMultiply(5)
→ allArgs = [2, 5]
→ multiply.apply(null, [2, 5])
→ multiply(2, 5)
→ 10
*/

// Pattern 4: bind with 'new' (special behavior)
function Point(x, y) {
    this.x = x;
    this.y = y;
}

const BoundPoint = Point.bind(null, 10);

const p1 = new BoundPoint(20);
console.log(p1.x);  // 10 (preset)
console.log(p1.y);  // 20 (provided)

/*
Special behavior with 'new':
- Bound 'this' is IGNORED
- new creates its own 'this'
- Preset arguments still used

new BoundPoint(20)
↓
new Point(10, 20)
↓
{ x: 10, y: 20 }
*/
```

### **12.4 Comparing call, apply, and bind**

#### **Comprehensive Comparison:**

```javascript
function greet(greeting, punctuation) {
    console.log(`${greeting}, ${this.name}${punctuation}`);
}

const person = { name: "John" };

// CALL: Execute immediately, arguments individually
greet.call(person, "Hello", "!");
// Output: "Hello, John!"

// APPLY: Execute immediately, arguments as array
greet.apply(person, ["Hello", "!"]);
// Output: "Hello, John!"

// BIND: Return new function, doesn't execute
const greetJohn = greet.bind(person);
greetJohn("Hello", "!");
// Output: "Hello, John!"

/*
═══════════════════════════════════════════════════════════
COMPARISON TABLE
═══════════════════════════════════════════════════════════

╔════════════════╦═══════════╦═══════════╦═══════════╗
║   Feature      ║   call    ║   apply   ║   bind    ║
╠════════════════╬═══════════╬═══════════╬═══════════╣
║ Executes?      ║    Yes    ║    Yes    ║    No     ║
║ Returns        ║  Result   ║  Result   ║  Function ║
║ Arguments      ║Individual ║   Array   ║Individual ║
║ 'this' binding ║ Temporary ║ Temporary ║ Permanent ║
║ Can preset args║    No     ║    No     ║    Yes    ║
║ Use case       ║One-time   ║Array args ║Reuse      ║
╚════════════════╩═══════════╩═══════════╩═══════════╝

═══════════════════════════════════════════════════════════
WHEN TO USE EACH
═══════════════════════════════════════════════════════════

USE CALL WHEN:
✓ You want to execute immediately
✓ You know arguments individually
✓ One-time context change

USE APPLY WHEN:
✓ You want to execute immediately
✓ Arguments are in an array
✓ Spreading array to function

USE BIND WHEN:
✓ You want to reuse the function
✓ Event handlers / callbacks
✓ Partial application
✓ Permanent 'this' binding
*/
```

#### **Performance Comparison:**

```javascript
// Performance test (simplified)
const obj = { name: "Test" };

function test() {
    return this.name;
}

console.time("call");
for (let i = 0; i < 1000000; i++) {
    test.call(obj);
}
console.timeEnd("call");

console.time("apply");
for (let i = 0; i < 1000000; i++) {
    test.apply(obj);
}
console.timeEnd("apply");

console.time("bind");
const bound = test.bind(obj);
for (let i = 0; i < 1000000; i++) {
    bound();
}
console.timeEnd("bind");

/*
Typical results (relative):
call:  ~fast
apply: ~slightly slower (array handling)
bind:  ~fastest for repeated calls (bound once, called many times)

Performance notes:
1. call is generally fastest for single use
2. apply has slight overhead from array processing
3. bind creates new function (one-time cost)
   but very fast for subsequent calls
4. For repeated calls with same context: bind is best
5. For one-time calls: call is sufficient
*/
```

#### **Real-World Comparison Examples:**

```javascript
// Scenario 1: Math operations with arrays
const numbers = [1, 2, 3, 4, 5];

// With apply (traditional)
const max1 = Math.max.apply(null, numbers);

// With call (needs spreading)
// const max2 = Math.max.call(null, ...numbers); // Same as regular call

// With bind (unnecessary here)
// const maxBound = Math.max.bind(null);
// const max3 = maxBound(...numbers);

// Modern: spread operator
const max4 = Math.max(...numbers);

console.log(max1);  // 5
console.log(max4);  // 5

// WINNER: apply (or spread) - perfect for array to arguments

// Scenario 2: Event handler
class ClickCounter {
    constructor() {
        this.count = 0;
    }
    
    increment() {
        this.count++;
        console.log(this.count);
    }
    
    attachWithCall(element) {
        // Won't work - call executes immediately!
        // element.onclick = this.increment.call(this);
    }
    
    attachWithApply(element) {
        // Won't work - apply executes immediately!
        // element.onclick = this.increment.apply(this);
    }
    
    attachWithBind(element) {
        // Works! bind returns function for later
        element.onclick = this.increment.bind(this);
    }
}

// WINNER: bind - perfect for callbacks

// Scenario 3: Constructor chaining
function Animal(name) {
    this.name = name;
}

function Dog(name, breed) {
    // With call (common)
    Animal.call(this, name);
    this.breed = breed;
}

function Cat(name, color) {
    // With apply (if args in array)
    const args = [name];
    Animal.apply(this, args);
    this.color = color;
}

// WINNER: call - cleaner for constructor chaining

// Scenario 4: Partial application
function greet(greeting, name, punctuation) {
    console.log(`${greeting}, ${name}${punctuation}`);
}

// With bind (perfect for partial application)
const greetHello = greet.bind(null, "Hello");
greetHello("John", "!");  // "Hello, John!"
greetHello("Jane", ".");  // "Hello, Jane."

// With call/apply (need wrapper)
function greetHelloCall(name, punctuation) {
    greet.call(null, "Hello", name, punctuation);
}

// WINNER: bind - built-in partial application

// Scenario 5: Array method borrowing
const arrayLike = {
    0: 'a',
    1: 'b',
    2: 'c',
    length: 3
};

// With call
const arr1 = Array.prototype.slice.call(arrayLike);

// With apply
const arr2 = Array.prototype.slice.apply(arrayLike);

// Modern: Array.from
const arr3 = Array.from(arrayLike);

console.log(arr1);  // ['a', 'b', 'c']
console.log(arr2);  // ['a', 'b', 'c']
console.log(arr3);  // ['a', 'b', 'c']

// WINNER: call or Array.from - call is traditional, Array.from is modern
```

### **12.5 When to Use Each Method**

#### **Decision Tree:**

```javascript
/*
═══════════════════════════════════════════════════════════
DECISION TREE: CHOOSING call, apply, OR bind
═══════════════════════════════════════════════════════════

START
  │
  ├─ Need to execute NOW?
  │  │
  │  ├─ YES
  │  │  │
  │  │  ├─ Arguments in array?
  │  │  │  │
  │  │  │  ├─ YES → use APPLY
  │  │  │  │  Example: Math.max.apply(null, numbersArray)
  │  │  │  │
  │  │  │  └─ NO → use CALL
  │  │  │     Example: greet.call(person, "Hello", "!")
  │  │  │
  │  │  └─ (or use modern spread operator)
  │  │
  │  └─ NO (need function for later)
  │     │
  │     └─ Use BIND
  │        Examples:
  │        - Event handlers
  │        - Callbacks
  │        - Partial application
  │        - Reusable bound functions
  │
END
*/
```

#### **Practical Guidelines:**

```javascript
// GUIDELINE 1: Event Handlers → bind
class Component {
    constructor() {
        this.handleClick = this.handleClick.bind(this);
        // ✓ Bound once in constructor
    }
    
    handleClick() {
        console.log(this);
    }
}

// GUIDELINE 2: Constructor Chaining → call
function Parent(name) {
    this.name = name;
}

function Child(name, age) {
    Parent.call(this, name);  // ✓ Clear and simple
    this.age = age;
}

// GUIDELINE 3: Array Operations → apply (or spread)
const numbers = [1, 2, 3, 4, 5];

// Traditional
const max = Math.max.apply(null, numbers);  // ✓ Works

// Modern (preferred)
const max2 = Math.max(...numbers);  // ✓ Cleaner

// GUIDELINE 4: Method Borrowing → call
const arrayLike = { 0: 'a', 1: 'b', length: 2 };

// With call
const arr = Array.prototype.slice.call(arrayLike);  // ✓ Traditional

// Modern (preferred)
const arr2 = Array.from(arrayLike);  // ✓ Cleaner

// GUIDELINE 5: Callbacks with Context → bind
const obj = {
    name: "Object",
    method: function() {
        console.log(this.name);
    }
};

// Callback without bind
setTimeout(obj.method, 1000);  // ✗ Context lost

// Callback with bind
setTimeout(obj.method.bind(obj), 1000);  // ✓ Context preserved

// GUIDELINE 6: Partial Application → bind
function log(level, message) {
    console.log(`[${level}] ${message}`);
}

const info = log.bind(null, "INFO");  // ✓ Perfect use case
info("Server started");  // [INFO] Server started

// GUIDELINE 7: One-time Context Change → call
function showName() {
    console.log(this.name);
}

const person = { name: "John" };
showName.call(person);  // ✓ Simple one-time use
```

#### **Modern Alternatives:**

```javascript
// ALTERNATIVE 1: Arrow functions instead of bind
class Component {
    constructor() {
        this.name = "Component";
    }
    
    // Old way: Regular method + bind
    handleClickOld() {
        console.log(this.name);
    }
    // Attach: element.onclick = this.handleClickOld.bind(this);
    
    // New way: Arrow function property
    handleClickNew = () => {
        console.log(this.name);
    }
    // Attach: element.onclick = this.handleClickNew;
}

// ALTERNATIVE 2: Spread operator instead of apply
const numbers = [1, 2, 3, 4, 5];

// Old way
const max1 = Math.max.apply(null, numbers);

// New way
const max2 = Math.max(...numbers);

// ALTERNATIVE 3: Array.from instead of slice.call
const arrayLike = { 0: 'a', 1: 'b', length: 2 };

// Old way
const arr1 = Array.prototype.slice.call(arrayLike);

// New way
const arr2 = Array.from(arrayLike);

// ALTERNATIVE 4: Rest parameters instead of arguments
// Old way
function oldSum() {
    const args = Array.prototype.slice.call(arguments);
    return args.reduce((a, b) => a + b, 0);
}

// New way
function newSum(...numbers) {
    return numbers.reduce((a, b) => a + b, 0);
}

/*
Modern JavaScript reduces need for call/apply/bind:
✓ Arrow functions (lexical this)
✓ Spread operator (array to arguments)
✓ Array.from (array-like to array)
✓ Rest parameters (arguments handling)
✓ Class field syntax (auto-bound methods)

But call/apply/bind still useful for:
✓ Constructor chaining
✓ Method borrowing
✓ Dynamic context changes
✓ Partial application
✓ Legacy code compatibility
*/
```

---


# **PART 6: CLOSURES AND EXECUTION CONTEXT (CONTINUED)**

## **13. CLOSURES DEEP DIVE (CONTINUED)**

### **13.8 IIFE and Closures (Continued)**

#### **IIFE for Initialization (Continued):**

```javascript
// Initialize application with IIFE
const app = (function() {
    console.log("App initializing...");
    
    // Setup code runs immediately
    const config = { version: "1.0", debug: true };
    const startTime = Date.now();
    
    console.log("App initialized!");
    
    // Return public interface
    return {
        version: config.version,
        
        getUptime: function() {
            return Date.now() - startTime;
        },
        
        isDebug: function() {
            return config.debug;
        }
    };
})();

// Already initialized when code runs!
console.log(app.version);     // "1.0"
console.log(app.getUptime()); // milliseconds since init

/*
Benefits of IIFE for initialization:
1. Code runs immediately
2. Initialization variables (config, startTime) are private
3. Only public API exposed
4. No global pollution
5. Self-contained module
*/
```

#### **IIFE vs Modules (Modern Comparison):**

```javascript
// OLD: IIFE Pattern
const oldModule = (function() {
    let privateVar = "private";
    
    return {
        getPrivate: function() {
            return privateVar;
        }
    };
})();

// MODERN: ES6 Modules
// module.js
let privateVar = "private";

export function getPrivate() {
    return privateVar;
}

// main.js
import { getPrivate } from './module.js';

/*
Comparison:

IIFE:
✓ Works in all environments
✓ Immediate execution
✓ No build tool needed
✗ All code in one file
✗ Manual dependency management
✗ All or nothing exports

ES6 Modules:
✓ Better syntax
✓ Named exports/imports
✓ Tree shaking support
✓ Built-in dependency management
✗ Needs modern environment or transpiler
✗ Async loading

When to use IIFE (still relevant):
- Legacy browser support
- Quick scripts/demos
- Inline initialization
- No build process
*/
```

---

## **14. ADVANCED CLOSURE PATTERNS**

### **14.1 Module Pattern**

The Module Pattern uses closures to create private and public members.

#### **Basic Module Pattern:**

```javascript
const CounterModule = (function() {
    // Private variables
    let count = 0;
    let maxCount = 100;
    let listeners = [];
    
    // Private methods
    function notifyListeners() {
        listeners.forEach(listener => {
            listener(count);
        });
    }
    
    function validateCount(value) {
        return typeof value === 'number' && value >= 0 && value <= maxCount;
    }
    
    // Public API
    return {
        increment: function() {
            if (count < maxCount) {
                count++;
                notifyListeners();
                return count;
            }
            throw new Error("Max count reached");
        },
        
        decrement: function() {
            if (count > 0) {
                count--;
                notifyListeners();
                return count;
            }
            throw new Error("Count cannot be negative");
        },
        
        getCount: function() {
            return count;
        },
        
        setCount: function(value) {
            if (validateCount(value)) {
                count = value;
                notifyListeners();
                return count;
            }
            throw new Error("Invalid count value");
        },
        
        subscribe: function(listener) {
            if (typeof listener === 'function') {
                listeners.push(listener);
            }
        },
        
        reset: function() {
            count = 0;
            notifyListeners();
        }
    };
})();

// Usage
CounterModule.subscribe(function(count) {
    console.log("Count changed to:", count);
});

CounterModule.increment();  // Count changed to: 1
CounterModule.increment();  // Count changed to: 2
CounterModule.setCount(50); // Count changed to: 50
CounterModule.reset();      // Count changed to: 0

/*
═══════════════════════════════════════════════════════════
MODULE PATTERN STRUCTURE
═══════════════════════════════════════════════════════════

┌─────────────────────────────────────────┐
│ CounterModule (Public API)              │
│ - increment()                           │
│ - decrement()                           │
│ - getCount()                            │
│ - setCount()                            │
│ - subscribe()                           │
│ - reset()                               │
│                                         │
│ All methods [[Scope]]: ───────┐         │
└───────────────────────────────┼─────────┘
                                ↓
                    ┌─────────────────────────┐
                    │ Module Lexical Env      │
                    │ (Private)               │
                    │                         │
                    │ count: 0                │
                    │ maxCount: 100           │
                    │ listeners: []           │
                    │ notifyListeners: <fn>   │
                    │ validateCount: <fn>     │
                    └─────────────────────────┘

Benefits:
1. ✓ Encapsulation (private/public separation)
2. ✓ Data protection (validation)
3. ✓ Single instance (singleton)
4. ✓ Clean API
5. ✓ Observable pattern (listeners)
*/
```

#### **Revealing Module Pattern:**

```javascript
const DataStore = (function() {
    // Private state
    let data = new Map();
    let changeLog = [];
    
    // Private methods
    function logChange(operation, key, value) {
        changeLog.push({
            operation: operation,
            key: key,
            value: value,
            timestamp: Date.now()
        });
    }
    
    function validateKey(key) {
        if (typeof key !== 'string' || key.length === 0) {
            throw new Error("Invalid key");
        }
    }
    
    // Public methods (named privately)
    function set(key, value) {
        validateKey(key);
        data.set(key, value);
        logChange('set', key, value);
    }
    
    function get(key) {
        validateKey(key);
        return data.get(key);
    }
    
    function remove(key) {
        validateKey(key);
        const value = data.get(key);
        data.delete(key);
        logChange('remove', key, value);
    }
    
    function clear() {
        data.clear();
        logChange('clear', null, null);
    }
    
    function getHistory() {
        return [...changeLog];  // Return copy
    }
    
    function size() {
        return data.size;
    }
    
    // Reveal public interface
    return {
        set: set,
        get: get,
        remove: remove,
        clear: clear,
        getHistory: getHistory,
        size: size
    };
})();

// Usage
DataStore.set('name', 'John');
DataStore.set('age', 30);
console.log(DataStore.get('name'));  // "John"
console.log(DataStore.size());       // 2
DataStore.remove('age');
console.log(DataStore.getHistory());
// [
//   { operation: 'set', key: 'name', value: 'John', timestamp: ... },
//   { operation: 'set', key: 'age', value: 30, timestamp: ... },
//   { operation: 'remove', key: 'age', value: 30, timestamp: ... }
// ]

/*
Revealing Module Pattern vs Regular Module Pattern:

REVEALING MODULE:
- All functions defined with clear names
- Easy to see what's public/private
- Return statement clearly shows public API
- Better for maintainability

REGULAR MODULE:
- Public methods defined in return object
- Private methods don't need separate declaration
- Can be more concise

Choose based on preference and code style.
*/
```

#### **Module with Configuration:**

```javascript
const Logger = (function(config) {
    // Configuration with defaults
    const settings = Object.assign({
        prefix: '[LOG]',
        timestamp: true,
        level: 'info',
        maxLogs: 100
    }, config);
    
    // Private state
    let logs = [];
    const levels = {
        debug: 0,
        info: 1,
        warn: 2,
        error: 3
    };
    
    // Private methods
    function shouldLog(level) {
        return levels[level] >= levels[settings.level];
    }
    
    function formatMessage(level, message) {
        let formatted = settings.prefix + ' ';
        
        if (settings.timestamp) {
            formatted += new Date().toISOString() + ' ';
        }
        
        formatted += '[' + level.toUpperCase() + '] ' + message;
        return formatted;
    }
    
    function addToHistory(level, message) {
        logs.push({
            level: level,
            message: message,
            timestamp: Date.now()
        });
        
        // Keep only last maxLogs entries
        if (logs.length > settings.maxLogs) {
            logs.shift();
        }
    }
    
    // Public API
    return {
        debug: function(message) {
            if (shouldLog('debug')) {
                const formatted = formatMessage('debug', message);
                console.log(formatted);
                addToHistory('debug', message);
            }
        },
        
        info: function(message) {
            if (shouldLog('info')) {
                const formatted = formatMessage('info', message);
                console.log(formatted);
                addToHistory('info', message);
            }
        },
        
        warn: function(message) {
            if (shouldLog('warn')) {
                const formatted = formatMessage('warn', message);
                console.warn(formatted);
                addToHistory('warn', message);
            }
        },
        
        error: function(message) {
            if (shouldLog('error')) {
                const formatted = formatMessage('error', message);
                console.error(formatted);
                addToHistory('error', message);
            }
        },
        
        getHistory: function() {
            return [...logs];
        },
        
        clearHistory: function() {
            logs = [];
        },
        
        setLevel: function(level) {
            if (levels.hasOwnProperty(level)) {
                settings.level = level;
            }
        }
    };
})({
    prefix: '[MyApp]',
    timestamp: true,
    level: 'debug',
    maxLogs: 50
});

// Usage
Logger.debug("Application starting");     // Shows if level is debug
Logger.info("User logged in");            // Shows
Logger.warn("Deprecated API used");       // Shows
Logger.error("Connection failed");        // Shows

Logger.setLevel('warn');  // Now only warn and error show
Logger.debug("Won't show");  // Hidden
Logger.warn("Will show");    // Shows

console.log(Logger.getHistory());  // Get all logged messages
```

### **14.2 Factory Functions**

Factory functions create and return objects, using closures for private data.

#### **Basic Factory Function:**

```javascript
function createPerson(name, age) {
    // Private variables
    let _name = name;
    let _age = age;
    let _id = Math.random().toString(36).substr(2, 9);
    
    // Private methods
    function validateAge(newAge) {
        return typeof newAge === 'number' && newAge >= 0 && newAge <= 150;
    }
    
    // Return public interface
    return {
        getName: function() {
            return _name;
        },
        
        setName: function(newName) {
            if (typeof newName === 'string' && newName.length > 0) {
                _name = newName;
            }
        },
        
        getAge: function() {
            return _age;
        },
        
        setAge: function(newAge) {
            if (validateAge(newAge)) {
                _age = newAge;
            }
        },
        
        getId: function() {
            return _id;
        },
        
        toString: function() {
            return `Person(${_name}, ${_age}, ${_id})`;
        }
    };
}

const john = createPerson('John', 30);
const jane = createPerson('Jane', 25);

console.log(john.getName());  // "John"
console.log(jane.getName());  // "Jane"

john.setAge(31);
console.log(john.getAge());   // 31

// Private variables not accessible
console.log(john._name);  // undefined
console.log(john._age);   // undefined

/*
═══════════════════════════════════════════════════════════
FACTORY FUNCTION VS CONSTRUCTOR
═══════════════════════════════════════════════════════════

FACTORY FUNCTION:
function createPerson(name) {
    return {
        getName: () => name
    };
}
const p = createPerson('John');

✓ No 'new' keyword needed
✓ Easy to create private variables
✓ Flexible return values
✓ Clear syntax
✗ Methods recreated for each instance
✗ No shared prototype

CONSTRUCTOR FUNCTION:
function Person(name) {
    this.name = name;
}
Person.prototype.getName = function() {
    return this.name;
};
const p = new Person('John');

✓ Shared methods via prototype
✓ Less memory per instance
✓ Standard pattern
✗ Requires 'new'
✗ Harder to create true private variables
✗ 'this' can be tricky
*/
```

#### **Factory with Inheritance:**

```javascript
// Base factory
function createAnimal(name, species) {
    let _name = name;
    let _species = species;
    
    return {
        getName: function() {
            return _name;
        },
        
        getSpecies: function() {
            return _species;
        },
        
        makeSound: function() {
            return "Some generic sound";
        },
        
        toString: function() {
            return `${_species} named ${_name}`;
        }
    };
}

// Extended factory
function createDog(name, breed) {
    // Create animal
    const animal = createAnimal(name, 'Dog');
    
    // Private variables specific to dogs
    let _breed = breed;
    let _tricks = [];
    
    // Add/override methods
    return Object.assign({}, animal, {
        getBreed: function() {
            return _breed;
        },
        
        makeSound: function() {
            return "Woof!";
        },
        
        learnTrick: function(trick) {
            _tricks.push(trick);
        },
        
        getTricks: function() {
            return [..._tricks];
        },
        
        toString: function() {
            return `${_breed} dog named ${animal.getName()}`;
        }
    });
}

const dog = createDog('Buddy', 'Golden Retriever');

console.log(dog.getName());      // "Buddy"
console.log(dog.getSpecies());   // "Dog"
console.log(dog.getBreed());     // "Golden Retriever"
console.log(dog.makeSound());    // "Woof!"

dog.learnTrick('sit');
dog.learnTrick('fetch');
console.log(dog.getTricks());    // ['sit', 'fetch']

/*
Composition over inheritance:
- createDog includes createAnimal
- Adds new methods
- Overrides existing methods
- Both have their own closures
- Flexible and maintainable
*/
```

#### **Factory with State Machine:**

```javascript
function createConnection(url) {
    let _state = 'disconnected';
    let _url = url;
    let _retryCount = 0;
    const _maxRetries = 3;
    
    // State machine
    const states = {
        disconnected: ['connecting'],
        connecting: ['connected', 'disconnected'],
        connected: ['disconnecting'],
        disconnecting: ['disconnected']
    };
    
    // Private methods
    function canTransitionTo(newState) {
        return states[_state].includes(newState);
    }
    
    function transition(newState) {
        if (canTransitionTo(newState)) {
            console.log(`State: ${_state} -> ${newState}`);
            _state = newState;
            return true;
        }
        console.error(`Invalid transition: ${_state} -> ${newState}`);
        return false;
    }
    
    function simulateConnection() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                if (Math.random() > 0.3) {
                    resolve();
                } else {
                    reject(new Error('Connection failed'));
                }
            }, 1000);
        });
    }
    
    // Public API
    return {
        connect: async function() {
            if (_state !== 'disconnected') {
                console.error('Already connected or connecting');
                return false;
            }
            
            transition('connecting');
            
            try {
                await simulateConnection();
                transition('connected');
                _retryCount = 0;
                console.log(`Connected to ${_url}`);
                return true;
            } catch (error) {
                console.error(error.message);
                transition('disconnected');
                
                if (_retryCount < _maxRetries) {
                    _retryCount++;
                    console.log(`Retrying... (${_retryCount}/${_maxRetries})`);
                    return this.connect();
                }
                
                return false;
            }
        },
        
        disconnect: function() {
            if (_state !== 'connected') {
                console.error('Not connected');
                return false;
            }
            
            transition('disconnecting');
            setTimeout(() => {
                transition('disconnected');
                console.log('Disconnected');
            }, 500);
            
            return true;
        },
        
        getState: function() {
            return _state;
        },
        
        isConnected: function() {
            return _state === 'connected';
        }
    };
}

const conn = createConnection('ws://example.com');

// Usage
// conn.connect().then(() => {
//     console.log('Connected!');
// });

/*
State machine with closures:
- Private state management
- Controlled state transitions
- Retry logic
- Clean public API
*/
```

### **14.3 Private Variables Pattern**

#### **Complete Privacy Example:**

```javascript
const SecureStore = (function() {
    // Truly private - using WeakMap
    const privateData = new WeakMap();
    
    // Private counter (shared across all instances)
    let instanceCount = 0;
    
    function SecureStore(key) {
        instanceCount++;
        
        // Store private data using WeakMap
        privateData.set(this, {
            key: key,
            data: new Map(),
            instanceId: instanceCount
        });
    }
    
    // Private helper methods
    function getPrivateData(instance) {
        return privateData.get(instance);
    }
    
    function validateKey(key) {
        if (typeof key !== 'string' || key.length === 0) {
            throw new Error('Invalid key');
        }
    }
    
    // Public methods
    SecureStore.prototype.set = function(key, value) {
        validateKey(key);
        const data = getPrivateData(this);
        data.data.set(key, value);
    };
    
    SecureStore.prototype.get = function(key) {
        validateKey(key);
        const data = getPrivateData(this);
        return data.data.get(key);
    };
    
    SecureStore.prototype.has = function(key) {
        const data = getPrivateData(this);
        return data.data.has(key);
    };
    
    SecureStore.prototype.delete = function(key) {
        const data = getPrivateData(this);
        return data.data.delete(key);
    };
    
    SecureStore.prototype.getInstanceId = function() {
        const data = getPrivateData(this);
        return data.instanceId;
    };
    
    SecureStore.prototype.toString = function() {
        const data = getPrivateData(this);
        return `SecureStore #${data.instanceId} (${data.data.size} items)`;
    };
    
    // Static method
    SecureStore.getInstanceCount = function() {
        return instanceCount;
    };
    
    return SecureStore;
})();

const store1 = new SecureStore('secret-key-1');
const store2 = new SecureStore('secret-key-2');

store1.set('username', 'john');
store1.set('password', 'secret');

console.log(store1.get('username'));  // "john"
console.log(store1.getInstanceId());  // 1
console.log(store2.getInstanceId());  // 2
console.log(SecureStore.getInstanceCount());  // 2

// Cannot access private data
console.log(store1.key);    // undefined
console.log(store1.data);   // undefined

/*
═══════════════════════════════════════════════════════════
WEAKMAP FOR PRIVACY
═══════════════════════════════════════════════════════════

Why WeakMap?
1. Keys are objects (instances)
2. Private data not accessible
3. Automatic garbage collection
4. No memory leaks

Structure:
privateData (WeakMap)
├─ store1 → { key: '...', data: Map, instanceId: 1 }
├─ store2 → { key: '...', data: Map, instanceId: 2 }

When store1 is no longer referenced:
- WeakMap automatically removes entry
- Private data is garbage collected
*/
```

### **14.4 Currying**

Currying transforms a function with multiple arguments into a sequence of functions with single arguments.

#### **Basic Currying:**

```javascript
// Regular function
function add(a, b, c) {
    return a + b + c;
}
console.log(add(1, 2, 3));  // 6

// Curried function
function curriedAdd(a) {
    return function(b) {
        return function(c) {
            return a + b + c;
        };
    };
}
console.log(curriedAdd(1)(2)(3));  // 6

/*
═══════════════════════════════════════════════════════════
HOW CURRYING WORKS WITH CLOSURES
═══════════════════════════════════════════════════════════

curriedAdd(1)(2)(3)

Step 1: curriedAdd(1)
┌──────────────────────────┐
│ Returns function(b)      │
│ [[Scope]]: ────┐         │
└────────────────┼─────────┘
                 ↓
        ┌────────────┐
        │ a: 1       │
        └────────────┘

Step 2: (returned function)(2)
┌──────────────────────────┐
│ Returns function(c)      │
│ [[Scope]]: ────┐         │
└────────────────┼─────────┘
                 ↓
        ┌────────────┐
        │ b: 2       │
        │ outer: ──┐ │
        └──────────┼─┘
                   ↓
              ┌────────┐
              │ a: 1   │
              └────────┘

Step 3: (returned function)(3)
Executes: a + b + c = 1 + 2 + 3 = 6

Each function closes over its argument!
*/

// ES6 arrow function version
const curriedAddArrow = a => b => c => a + b + c;
console.log(curriedAddArrow(1)(2)(3));  // 6
```

#### **Generic Curry Function:**

```javascript
function curry(fn) {
    return function curried(...args) {
        if (args.length >= fn.length) {
            // All arguments provided
            return fn.apply(this, args);
        } else {
            // Partial application
            return function(...moreArgs) {
                return curried.apply(this, args.concat(moreArgs));
            };
        }
    };
}

// Regular function
function multiply(a, b, c) {
    return a * b * c;
}

// Curry it
const curriedMultiply = curry(multiply);

// Various ways to call
console.log(curriedMultiply(2)(3)(4));      // 24
console.log(curriedMultiply(2, 3)(4));      // 24
console.log(curriedMultiply(2)(3, 4));      // 24
console.log(curriedMultiply(2, 3, 4));      // 24

// Partial application
const double = curriedMultiply(2);
const triple = curriedMultiply(3);

console.log(double(5)(1));   // 10 (2 * 5 * 1)
console.log(triple(5)(1));   // 15 (3 * 5 * 1)

/*
Curry benefits:
1. Partial application
2. Function reuse
3. Composition
4. Flexible calling
*/
```

#### **Practical Currying Examples:**

```javascript
// Example 1: Logger with currying
const log = curry(function(level, timestamp, message) {
    console.log(`[${level}] ${timestamp}: ${message}`);
});

const errorLog = log('ERROR');
const errorLogNow = errorLog(Date.now());

errorLogNow('File not found');
errorLogNow('Connection failed');

// Example 2: Data processing
const map = curry(function(fn, array) {
    return array.map(fn);
});

const double = x => x * 2;
const mapDouble = map(double);

console.log(mapDouble([1, 2, 3]));  // [2, 4, 6]
console.log(mapDouble([4, 5, 6]));  // [8, 10, 12]

// Example 3: Validation
const validate = curry(function(regex, message, value) {
    if (!regex.test(value)) {
        throw new Error(message);
    }
    return value;
});

const validateEmail = validate(/^[^\s@]+@[^\s@]+\.[^\s@]+$/);
const validateEmailWithMsg = validateEmail('Invalid email');

try {
    console.log(validateEmailWithMsg('test@example.com'));  // Valid
    console.log(validateEmailWithMsg('invalid'));  // Throws
} catch (e) {
    console.error(e.message);
}
```

### **14.5 Function Composition**

Function composition combines multiple functions to create new functions.

#### **Basic Composition:**

```javascript
// Individual functions
const add10 = x => x + 10;
const multiply2 = x => x * 2;
const subtract5 = x => x - 5;

// Manual composition
const result = subtract5(multiply2(add10(5)));
console.log(result);  // ((5 + 10) * 2) - 5 = 25

// Compose function (right to left)
function compose(...fns) {
    return function(value) {
        return fns.reduceRight((acc, fn) => fn(acc), value);
    };
}

const calculate = compose(subtract5, multiply2, add10);
console.log(calculate(5));  // 25

// Pipe function (left to right)
function pipe(...fns) {
    return function(value) {
        return fns.reduce((acc, fn) => fn(acc), value);
    };
}

const calculate2 = pipe(add10, multiply2, subtract5);
console.log(calculate2(5));  // 25

/*
═══════════════════════════════════════════════════════════
COMPOSITION WITH CLOSURES
═══════════════════════════════════════════════════════════

compose(subtract5, multiply2, add10)
Returns a function that closes over [subtract5, multiply2, add10]

When calculate(5) is called:
┌──────────────────────────────┐
│ Returned function            │
│ [[Scope]]: ────┐             │
└────────────────┼─────────────┘
                 ↓
        ┌────────────────────┐
        │ fns: [            │
        │   subtract5,       │
        │   multiply2,       │
        │   add10            │
        │ ]                  │
        └────────────────────┘

Execution:
1. add10(5) = 15
2. multiply2(15) = 30
3. subtract5(30) = 25
*/
```

#### **Composition with Context:**

```javascript
function compose(...fns) {
    return function(...args) {
        // Call first function with all args
        let result = fns[fns.length - 1].apply(this, args);
        
        // Call remaining functions with result
        for (let i = fns.length - 2; i >= 0; i--) {
            result = fns[i].call(this, result);
        }
        
        return result;
    };
}

const obj = {
    multiplier: 2,
    
    add10: function(x) {
        return x + 10;
    },
    
    multiplyByProperty: function(x) {
        return x * this.multiplier;
    },
    
    subtract5: function(x) {
        return x - 5;
    }
};

const calculate = compose(
    obj.subtract5,
    obj.multiplyByProperty,
    obj.add10
);

// Call with context
console.log(calculate.call(obj, 5));  // ((5 + 10) * 2) - 5 = 25
```

#### **Practical Composition Examples:**

```javascript
// Example 1: Data transformation pipeline
const trim = str => str.trim();
const toLowerCase = str => str.toLowerCase();
const removeSpaces = str => str.replace(/\s+/g, '');
const addPrefix = str => `user_${str}`;

const createUsername = pipe(
    trim,
    toLowerCase,
    removeSpaces,
    addPrefix
);

console.log(createUsername('  John Doe  '));  // "user_johndoe"

// Example 2: Number validation and transformation
const toNumber = x => Number(x);
const roundToTwo = x => Math.round(x * 100) / 100;
const clamp = (min, max) => x => Math.max(min, Math.min(max, x));
const formatCurrency = x => `$${x.toFixed(2)}`;

const processPrice = pipe(
    toNumber,
    roundToTwo,
    clamp(0, 1000),
    formatCurrency
);

console.log(processPrice('45.6789'));   // "$45.68"
console.log(processPrice('1500'));      // "$1000.00"
console.log(processPrice('-10'));       // "$0.00"

// Example 3: Async composition
function composeAsync(...fns) {
    return function(value) {
        return fns.reduceRight((acc, fn) => {
            return acc.then(fn);
        }, Promise.resolve(value));
    };
}

const fetchUser = id => {
    return Promise.resolve({ id, name: 'John' });
};

const fetchPosts = user => {
    return Promise.resolve({
        ...user,
        posts: ['Post 1', 'Post 2']
    });
};

const formatData = data => {
    return {
        userName: data.name,
        postCount: data.posts.length
    };
};

const getUserInfo = composeAsync(formatData, fetchPosts, fetchUser);

// getUserInfo(1).then(info => {
//     console.log(info);  // { userName: 'John', postCount: 2 }
// });
```

### **14.6 Memoization**

Memoization caches function results to improve performance.

#### **Simple Memoization:**

```javascript
function memoize(fn) {
    const cache = new Map();
    
    return function(...args) {
        const key = JSON.stringify(args);
        
        if (cache.has(key)) {
            console.log('Cache hit:', key);
            return cache.get(key);
        }
        
        console.log('Computing:', key);
        const result = fn.apply(this, args);
        cache.set(key, result);
        return result;
    };
}

// Expensive fibonacci
function fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

const memoizedFib = memoize(fibonacci);

console.time('First call');
console.log(memoizedFib(35));  // Computing... ~2 seconds
console.timeEnd('First call');

console.time('Second call');
console.log(memoizedFib(35));  // Cache hit! Instant
console.timeEnd('Second call');

/*
Cache structure (closure):
┌──────────────────────────────┐
│ memoizedFib                  │
│ [[Scope]]: ────┐             │
└────────────────┼─────────────┘
                 ↓
        ┌────────────────────┐
        │ cache: Map {       │
        │   "[35]": 9227465  │
        │   "[34]": 5702887  │
        │   "[33]": 3524578  │
        │   ...              │
        │ }                  │
        │ fn: fibonacci      │
        └────────────────────┘

Closure preserves cache across calls!
*/
```

#### **Advanced Memoization with TTL:**

```javascript
function memoizeWithTTL(fn, ttl = 60000) {
    const cache = new Map();
    
    return function(...args) {
        const key = JSON.stringify(args);
        const now = Date.now();
        
        if (cache.has(key)) {
            const { value, timestamp } = cache.get(key);
            
            if (now - timestamp < ttl) {
                console.log('Cache hit (valid)');
                return value;
            }
            
            console.log('Cache expired');
            cache.delete(key);
        }
        
        console.log('Computing...');
        const value = fn.apply(this, args);
        cache.set(key, {
            value: value,
            timestamp: now
        });
        
        return value;
    };
}

function fetchData(id) {
    console.log(`Fetching data for id: ${id}`);
    return { id, data: 'Important data' };
}

const memoizedFetch = memoizeWithTTL(fetchData, 2000);  // 2 second TTL

memoizedFetch(1);  // Computing...
memoizedFetch(1);  // Cache hit (valid)

setTimeout(() => {
    memoizedFetch(1);  // Cache expired, computing...
}, 2500);
```

#### **LRU (Least Recently Used) Memoization:**

```javascript
function memoizeLRU(fn, maxSize = 100) {
    const cache = new Map();
    const accessOrder = [];
    
    return function(...args) {
        const key = JSON.stringify(args);
        
        if (cache.has(key)) {
            // Update access order (move to end)
            const index = accessOrder.indexOf(key);
            accessOrder.splice(index, 1);
            accessOrder.push(key);
            
            console.log('Cache hit');
            return cache.get(key);
        }
        
        console.log('Computing...');
        const result = fn.apply(this, args);
        
        // Check if cache is full
        if (cache.size >= maxSize) {
            // Remove least recently used (first in order)
            const lruKey = accessOrder.shift();
            cache.delete(lruKey);
            console.log('Evicted LRU item');
        }
        
        cache.set(key, result);
        accessOrder.push(key);
        
        return result;
    };
}

function expensiveOperation(n) {
    return n * 2;
}

const memoized = memoizeLRU(expensiveOperation, 3);

memoized(1);  // Computing...
memoized(2);  // Computing...
memoized(3);  // Computing...
memoized(1);  // Cache hit
memoized(4);  // Computing... (evicts 2, the LRU)
memoized(2);  // Computing... (was evicted)

/*
LRU tracking:
┌──────────────────────────────┐
│ memoized                     │
│ [[Scope]]: ────┐             │
└────────────────┼─────────────┘
                 ↓
        ┌──────────────────────┐
        │ cache: Map {         │
        │   "[1]": 2           │
        │   "[3]": 6           │
        │   "[4]": 8           │
        │ }                    │
        │ accessOrder: [       │
        │   "[3]",             │
        │   "[1]",             │
        │   "[4]"              │
        │ ]                    │
        │ maxSize: 3           │
        └──────────────────────┘

Most recently used at end
*/
```

### **14.7 Closure Performance Considerations**

#### **Memory Usage:**

```javascript
// PROBLEM: Unnecessary closure over large data
function createProcessor() {
    const hugeArray = new Array(1000000).fill('data');
    let counter = 0;
    
    return {
        // This function doesn't need hugeArray
        // But it keeps it in memory!
        incrementCounter: function() {
            counter++;
            return counter;
        },
        
        // This function needs hugeArray
        processArray: function() {
            return hugeArray.length;
        }
    };
}

const processor = createProcessor();
processor.incrementCounter();  // Keeps hugeArray in memory unnecessarily

/*
Memory issue:
┌──────────────────────────────┐
│ processor methods            │
│ [[Scope]]: ────┐             │
└────────────────┼─────────────┘
                 ↓
        ┌────────────────────────┐
        │ Lexical Env            │
        │ hugeArray: [...]       │ ← 1MB!
        │ counter: 1             │
        └────────────────────────┘

Both methods keep hugeArray alive!
*/

// SOLUTION: Separate closures
function createEfficientProcessor() {
    let counter = 0;
    
    // Process heavy data once, keep only result
    const processedResult = (function() {
        const hugeArray = new Array(1000000).fill('data');
        return hugeArray.length;  // Only keep the number
        // hugeArray is garbage collected!
    })();
    
    return {
        incrementCounter: function() {
            counter++;
            return counter;
        },
        
        getProcessedResult: function() {
            return processedResult;
        }
    };
}

const efficientProcessor = createEfficientProcessor();
efficientProcessor.incrementCounter();  // No hugeArray in memory!

/*
Better memory:
┌──────────────────────────────┐
│ processor methods            │
│ [[Scope]]: ────┐             │
└────────────────┼─────────────┘
                 ↓
        ┌────────────────────────┐
        │ Lexical Env            │
        │ counter: 1             │
        │ processedResult: 1000000│ ← Just a number!
        └────────────────────────┘

Saved ~1MB per instance!
*/
```

#### **Best Practices:**

```javascript
/*
═══════════════════════════════════════════════════════════
CLOSURE BEST PRACTICES
═══════════════════════════════════════════════════════════

DO:
✓ Use closures for data privacy
✓ Cache expensive computations
✓ Create specialized functions
✓ Maintain state in functional programming
✓ Return only what's needed from outer scope

DON'T:
✗ Create closures in tight loops unnecessarily
✗ Keep large objects in closure scope unnecessarily
✗ Over-complicate with deep nesting
✗ Forget to clean up event listeners
✗ Hold references to DOM nodes after removal
*/

// GOOD: Closure for counter
function createCounter() {
    let count = 0;
    return () => ++count;
}

// BAD: Closure in loop
const functions = [];
for (var i = 0; i < 1000; i++) {
    functions.push(function() { return i; });  // All reference same i
}

// GOOD: Use let or avoid closure
const functions2 = [];
for (let i = 0; i < 1000; i++) {
    functions2.push(function() { return i; });  // Each has own i
}

// Or better: Don't create functions if not needed
const values = Array.from({ length: 1000 }, (_, i) => i);

// GOOD: Minimal scope
function createLogger(prefix) {
    return function(message) {
        console.log(`${prefix}: ${message}`);
    };  // Only closes over 'prefix', not unnecessary variables
}

// BAD: Large scope
function createBadLogger(prefix) {
    const hugeConfig = loadHugeConfig();  // Kept in memory!
    const anotherUnused = 'unused';       // Also kept!
    
    return function(message) {
        console.log(`${prefix}: ${message}`);  // Only uses prefix
    };  // But keeps entire scope in memory
}

// GOOD: Clean up references
function attachHandler() {
    const element = document.getElementById('btn');
    
    function handleClick() {
        console.log('Clicked');
    }
    
    element.addEventListener('click', handleClick);
    
    // Return cleanup function
    return function cleanup() {
        element.removeEventListener('click', handleClick);
    };
}

const cleanup = attachHandler();
// Later:
cleanup();  // Remove listener, allow GC
```

---

# **PART 7: ADVANCED TOPICS**

## **15. EXECUTION CONTEXT IN ES6+**

### **15.1 Block Scoping with let and const**

ES6 introduced block-scoped variables with `let` and `const`.

#### **Block Scope Detailed:**

```javascript
{
    var functionScoped = 'accessible outside';
    let blockScoped = 'not accessible outside';
    const alsoBlockScoped = 'not accessible outside';
}

console.log(functionScoped);    // ✓ 'accessible outside'
// console.log(blockScoped);    // ✗ ReferenceError
// console.log(alsoBlockScoped);// ✗ ReferenceError

/*
═══════════════════════════════════════════════════════════
EXECUTION CONTEXT WITH BLOCK SCOPE
═══════════════════════════════════════════════════════════

Global Execution Context:
{
    VariableEnvironment: {
        functionScoped: 'accessible outside'  ← var hoisted here
    },
    
    LexicalEnvironment: {
        // Global let/const would go here
    }
}

Block Environment (temporary, destroyed after block):
{
    LexicalEnvironment: {
        blockScoped: 'not accessible outside',
        alsoBlockScoped: 'not accessible outside'
    },
    outer: → Global Lexical Environment
}

After block ends:
- Block environment destroyed
- blockScoped and alsoBlockScoped garbage collected
- functionScoped remains in global scope
*/
```

#### **Block Scope in Different Statements:**

```javascript
// for loop
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log('let:', i), 100);
}
// Output: 0, 1, 2

for (var j = 0; j < 3; j++) {
    setTimeout(() => console.log('var:', j), 100);
}
// Output: 3, 3, 3

// if statement
if (true) {
    let x = 'block';
    var y = 'function';
}
// console.log(x);  // ReferenceError
console.log(y);     // 'function'

// switch statement
switch (true) {
    case true: {  // Block needed for let/const
        let caseVar = 'case value';
        break;
    }
}
// console.log(caseVar);  // ReferenceError

// try-catch
try {
    throw new Error('test');
} catch (e) {
    let errorMsg = e.message;
    // errorMsg is block-scoped to catch
}
// console.log(errorMsg);  // ReferenceError

/*
Each block creates new Lexical Environment:

for loop (let):
┌──────────────────────────┐
│ Iteration 0              │
│ LexEnv: { i: 0 }         │
└──────────────────────────┘
┌──────────────────────────┐
│ Iteration 1              │
│ LexEnv: { i: 1 }         │
└──────────────────────────┘
┌──────────────────────────┐
│ Iteration 2              │
│ LexEnv: { i: 2 }         │
└──────────────────────────┘

for loop (var):
┌──────────────────────────┐
│ Function/Global Scope    │
│ VarEnv: { j: 3 }         │ ← Same j
└──────────────────────────┘
*/
```

### **15.2 Arrow Functions and Lexical This**

Arrow functions don't have their own `this` binding—they inherit it lexically.

#### **Arrow Function 'this' Behavior:**

```javascript
const obj = {
    name: 'Object',
    
    regularMethod: function() {
        console.log('Regular this:', this.name);
        
        // Regular function - new 'this'
        setTimeout(function() {
            console.log('Timeout regular:', this.name);  // undefined
        }, 100);
        
        // Arrow function - inherits 'this'
        setTimeout(() => {
            console.log('Timeout arrow:', this.name);  // 'Object'
        }, 100);
    },
    
    arrowMethod: () => {
        console.log('Arrow method this:', this.name);  // undefined
        // 'this' is from surrounding scope (global)
    }
};

obj.regularMethod();
// Regular this: Object
// Timeout regular: undefined
// Timeout arrow: Object

obj.arrowMethod();
// Arrow method this: undefined

/*
═══════════════════════════════════════════════════════════
EXECUTION CONTEXT WITH ARROW FUNCTIONS
═══════════════════════════════════════════════════════════

regularMethod() Execution Context:
{
    ThisBinding: obj  ← Method call
}

Arrow function inside setTimeout:
{
    ThisBinding: <INHERITED from regularMethod> = obj
    // No own 'this', uses parent's
}

Regular function inside setTimeout:
{
    ThisBinding: global/undefined  ← Function call
    // Has own 'this'
}

arrowMethod Execution Context:
{
    ThisBinding: <INHERITED from global> = global/undefined
    // Arrow as method gets global 'this'
}
*/
```

#### **Arrow Functions in Classes:**

```javascript
class Counter {
    constructor() {
        this.count = 0;
        
        // Arrow function property
        this.incrementArrow = () => {
            this.count++;
            console.log('Arrow:', this.count);
        };
    }
    
    // Regular method
    incrementRegular() {
        this.count++;
        console.log('Regular:', this.count);
    }
}

const counter = new Counter();

// Works as expected
counter.incrementArrow();   // Arrow: 1
counter.incrementRegular(); // Regular: 2

// Detached references
const arrowFn = counter.incrementArrow;
const regularFn = counter.incrementRegular;

arrowFn();    // Arrow: 3 (still works!)
regularFn();  // TypeError: Cannot read 'count' of undefined

/*
Why arrow function works when detached?

Arrow function created in constructor:
{
    [[Code]]: () => { this.count++; ... },
    [[Scope]]: {
        this: counter instance  ← Permanently bound!
    }
}

Regular method:
{
    [[Code]]: function() { this.count++; ... },
    this: determined at call time
}

Memory difference:
- Arrow function: Each instance gets own function copy
- Regular method: Shared on prototype

const c1 = new Counter();
const c2 = new Counter();

c1.incrementArrow === c2.incrementArrow  // false (different functions)
c1.incrementRegular === c2.incrementRegular  // true (same prototype method)
*/
```

### **15.3 Classes and Execution Context**

ES6 classes provide syntactic sugar over constructor functions.

#### **Class Execution Context:**

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    
    greet() {
        console.log(`Hello, I'm ${this.name}`);
    }
    
    static species = 'Homo sapiens';
    
    static describe() {
        console.log(`Species: ${this.species}`);
    }
}

const john = new Person('John', 30);
john.greet();  // Hello, I'm John

Person.describe();  // Species: Homo sapiens

/*
═══════════════════════════════════════════════════════════
CLASS EXECUTION CONTEXT
═══════════════════════════════════════════════════════════

new Person('John', 30) process:

Step 1: Create new empty object
  {} created

Step 2: Set prototype
  {}.__proto__ = Person.prototype

Step 3: Create constructor execution context
  {
      ThisBinding: {},  ← New object
      LexicalEnvironment: {
          name: 'John',
          age: 30
      }
  }

Step 4: Execute constructor
  this.name = 'John'
  this.age = 30
  
  Object now: {
      name: 'John',
      age: 30,
      __proto__: Person.prototype
  }

Step 5: Return this (implicit)

greet() method call:
When john.greet() is called:
{
    ThisBinding: john,  ← Instance
    LexicalEnvironment: {},
    outer: → Global
}

static describe() call:
When Person.describe() is called:
{
    ThisBinding: Person,  ← Class itself
    LexicalEnvironment: {},
    outer: → Global
}
*/
```

#### **Class Fields and Private Fields:**

```javascript
class BankAccount {
    // Public field
    accountType = 'checking';
    
    // Private field (ES2022)
    #balance = 0;
    #transactions = [];
    
    constructor(initialBalance) {
        this.#balance = initialBalance;
    }
    
    deposit(amount) {
        if (amount > 0) {
            this.#balance += amount;
            this.#recordTransaction('deposit', amount);
        }
    }
    
    withdraw(amount) {
        if (amount > 0 && amount <= this.#balance) {
            this.#balance -= amount;
            this.#recordTransaction('withdraw', amount);
        }
    }
    
    getBalance() {
        return this.#balance;
    }
    
    // Private method
    #recordTransaction(type, amount) {
        this.#transactions.push({
            type,
            amount,
            timestamp: Date.now()
        });
    }
    
    getTransactions() {
        return [...this.#transactions];
    }
}

const account = new BankAccount(1000);
account.deposit(500);
console.log(account.getBalance());  // 1500

// Cannot access private fields
// console.log(account.#balance);  // SyntaxError
// console.log(account.#recordTransaction);  // SyntaxError

/*
Execution Context with Private Fields:

Instance structure:
{
    accountType: 'checking',  ← Public
    #balance: 1500,           ← Private (truly inaccessible)
    #transactions: [...]      ← Private
}

Private fields are internally managed:
- Not accessible via this['#balance']
- Not accessible via Object.keys()
- Not inherited by subclasses
- Syntax error if accessed outside class

Traditional approach (naming convention):
class OldAccount {
    constructor() {
        this._balance = 0;  // "private" by convention
    }
}
// But this._balance is still accessible!

New private fields:
- Truly private
- Syntax enforced
- Better encapsulation
*/
```

### **15.4 Modules and Module Scope**

ES6 modules have their own execution context.

#### **Module Execution Context:**

```javascript
// math.js
console.log('math.js executing');
console.log('Module this:', this);  // undefined

let moduleCount = 0;
export function increment() {
    return ++moduleCount;
}

export const PI = 3.14159;

// main.js
console.log('main.js executing');
import { increment, PI } from './math.js';

console.log(increment());  // 1
console.log(increment());  // 2
console.log(PI);           // 3.14159

/*
═══════════════════════════════════════════════════════════
MODULE EXECUTION CONTEXT
═══════════════════════════════════════════════════════════

When module loads:
1. Module code executes ONCE (first import)
2. Creates Module Environment Record
3. Subsequent imports reuse same module instance

math.js Module Execution Context:
{
    VariableEnvironment: {},  // Strict mode, no var hoisting to global
    
    LexicalEnvironment: {
        EnvironmentRecord: {
            moduleCount: 0,
            increment: <function>,
            PI: 3.14159
        },
        outer: null  // Modules have no outer scope
    },
    
    ThisBinding: undefined  // Always undefined in modules
}

Export bindings:
- Live bindings (not copies)
- Read-only from importing module
- Changes in exporting module reflect in importing module

main.js Module Execution Context:
{
    LexicalEnvironment: {
        EnvironmentRecord: {
            increment: <reference to math.js export>,
            PI: <reference to math.js export>
        }
    },
    
    ThisBinding: undefined
}

Import resolution:
increment() → math.js Module → moduleCount
Changes to moduleCount in math.js are visible to main.js
*/
```

#### **Module Scope vs Script Scope:**

```javascript
// script.js (traditional <script>)
var scriptVar = 'script';
console.log(window.scriptVar);  // 'script'
console.log(this);              // Window

// module.js (type="module")
var moduleVar = 'module';
console.log(window.moduleVar);  // undefined
console.log(this);              // undefined

/*
╔════════════════╦═══════════════╦══════════════════╗
║    Feature     ║    Script     ║     Module       ║
╠════════════════╬═══════════════╬══════════════════╣
║ 'this'         ║ window/global ║ undefined        ║
║ var scope      ║ Global        ║ Module           ║
║ Strict mode    ║ Optional      ║ Always           ║
║ Top-level await║ No            ║ Yes (ES2022)     ║
║ Imports        ║ No            ║ Yes              ║
║ Exports        ║ No            ║ Yes              ║
╚════════════════╩═══════════════╩══════════════════╝
*/
```

### **15.5 Async/Await and Execution Context**

Async functions create special execution contexts.

#### **Async Function Execution:**

```javascript
async function fetchUserData(userId) {
    console.log('1. Start fetching');
    
    const response = await fetch(`/api/users/${userId}`);
    console.log('2. Response received');
    
    const data = await response.json();
    console.log('3. Data parsed');
    
    return data;
}

// fetchUserData(1);

/*
═══════════════════════════════════════════════════════════
ASYNC FUNCTION EXECUTION CONTEXT
═══════════════════════════════════════════════════════════

Call: fetchUserData(1)

Step 1: Create execution context
{
    LexicalEnvironment: {
        userId: 1
    },
    ThisBinding: <depends on call>
}

Execute: console.log('1. Start fetching')
Output: "1. Start fetching"

Step 2: Hit 'await fetch(...)'
- fetch() returns Promise
- Function PAUSES (suspends execution context)
- Returns Promise to caller immediately
- Execution context saved

Call Stack:
[Global EC]  ← Returns here

(Time passes... fetch completes)

Step 3: Promise resolves
- Execution context RESTORED
- Continue from after await

Call Stack:
[fetchUserData EC]  ← Restored
[Global EC]

Execute: console.log('2. Response received')
Output: "2. Response received"

Step 4: Hit 'await response.json()'
- Function PAUSES again
- Saves context again

(Time passes... json() completes)

Step 5: Promise resolves
- Context restored again
- Continue execution

Execute: console.log('3. Data parsed')
Output: "3. Data parsed"

Execute: return data
- Returns resolved Promise
- Context destroyed

═══════════════════════════════════════════════════════════
KEY POINTS
═══════════════════════════════════════════════════════════

1. async function returns Promise immediately
2. Execution context can be suspended and restored
3. 'await' pauses function, not entire program
4. Other code can run while function is paused
5. Variables persist across await (via saved context)
*/
```

#### **Async Context Preservation:**

```javascript
async function demonstrateContext() {
    const localVar = 'preserved';
    let counter = 0;
    
    console.log('Before await:', localVar, counter);
    
    await new Promise(resolve => setTimeout(resolve, 1000));
    
    // Context preserved!
    console.log('After await:', localVar, counter);
    counter++;
    
    await new Promise(resolve => setTimeout(resolve, 1000));
    
    // Still preserved!
    console.log('After second await:', localVar, counter);
}

// demonstrateContext();
// Output:
// Before await: preserved 0
// (1 second pause)
// After await: preserved 0
// (1 second pause)
// After second await: preserved 1

/*
How context is preserved:

Initial execution context:
{
    LexicalEnvironment: {
        localVar: 'preserved',
        counter: 0
    }
}

At first await:
- Context saved in memory
- Function suspended

After 1 second:
- Context restored from memory
- localVar still 'preserved'
- counter still 0
- Continue execution

At second await:
- Context saved again (now counter: 1)
- Function suspended

After another second:
- Context restored
- All variables intact
*/
```

### **15.6 Generators and Execution Context**

Generator functions can pause and resume execution.

#### **Generator Execution Context:**

```javascript
function* generatorFunction() {
    console.log('Start');
    const a = 1;
    
    yield a;
    console.log('After first yield');
    const b = 2;
    
    yield a + b;
    console.log('After second yield');
    
    return a + b + 3;
}

const generator = generatorFunction();

console.log('Created generator');
console.log(generator.next());  // { value: 1, done: false }
console.log('Between yields');
console.log(generator.next());  // { value: 3, done: false }
console.log('Before final');
console.log(generator.next());  // { value: 6, done: true }

/*
═══════════════════════════════════════════════════════════
GENERATOR EXECUTION FLOW
═══════════════════════════════════════════════════════════

generatorFunction() call:
- Does NOT execute function body
- Returns generator object
- Execution context NOT created yet

generator.next() - First call:
┌─────────────────────────────────┐
│ Generator Execution Context     │
│ Created                         │
│ LexicalEnvironment: { a: 1 }    │
└─────────────────────────────────┘

Output: "Start"
Hits: yield a
- Context SUSPENDED
- Value 1 returned
- Context saved

generator.next() - Second call:
┌─────────────────────────────────┐
│ Generator Execution Context     │
│ RESTORED                        │
│ LexicalEnvironment: {           │
│   a: 1,                         │
│   b: 2                          │
│ }                               │
└─────────────────────────────────┘

Output: "After first yield"
Hits: yield a + b
- Context SUSPENDED again
- Value 3 returned
- Context saved with b

generator.next() - Third call:
┌─────────────────────────────────┐
│ Generator Execution Context     │
│ RESTORED again                  │
│ LexicalEnvironment: {           │
│   a: 1,                         │
│   b: 2                          │
│ }                               │
└─────────────────────────────────┘

Output: "After second yield"
Hits: return a + b + 3
- Context completed
- Value 6 returned
- done: true
- Context destroyed

Variables persist across yields because
context is suspended, not destroyed!
*/
```

#### **Generator with Closure:**

```javascript
function* createCounter() {
    let count = 0;
    
    while (true) {
        const increment = yield count;
        if (increment) {
            count += increment;
        } else {
            count++;
        }
    }
}

const counter = createCounter();

console.log(counter.next());      // { value: 0, done: false }
console.log(counter.next());      // { value: 1, done: false }
console.log(counter.next(5));     // { value: 6, done: false }
console.log(counter.next());      // { value: 7, done: false }

/*
Generator maintains closure over 'count':

┌──────────────────────────────────┐
│ counter (generator object)       │
│                                  │
│ [[GeneratorState]]: suspended    │
│ [[GeneratorContext]]: ────┐      │
└───────────────────────────┼──────┘
                            ↓
                ┌─────────────────────┐
                │ Suspended Context   │
                │ count: 7            │
                │ increment: undefined│
                │ (from last yield)   │
                └─────────────────────┘

Each next() call:
1. Restores context
2. Continues from last yield
3. Updates count
4. Suspends at next yield
5. Saves context

Context persists between next() calls!
*/
```



