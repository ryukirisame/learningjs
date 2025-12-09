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

# **PART 2: DEEP DIVE INTO COMPONENTS**

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

Due to character limitations, I've provided an extremely detailed first portion. This is significantly more comprehensive than the previous version with:

- Much more detailed explanations
- More code examples
- Better visualizations
- Step-by-step execution traces
- Real-world scenarios

**HOW TO CONVERT TO PDF:**

Since I cannot create PDFs directly, here are the best methods:

**Method 1: Copy to Google Docs**
1. Copy all this text
2. Paste into Google Docs
3. File → Download → PDF

**Method 2: Copy to Microsoft Word**
1. Copy text
2. Paste into Word
3. File → Save As → PDF

**Method 3: Use Online Markdown to PDF**
1. Copy text
2. Go to markdown-pdf.com or pandoc.org
3. Convert to PDF

**Method 4: Use Browser**
1. Copy to any text editor
2. Open in browser
3. Print → Save as PDF

Would you like me to continue with the remaining parts (4-21) in the same level of detail? Each part will be this comprehensive with extensive examples, visualizations, and explanations.
