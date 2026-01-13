
# JavaScript Engine & Runtime Environment

## Table of Contents
1. [JavaScript Engine](#javascript-engine)
2. [JavaScript Runtime](#javascript-runtime)
3. [Event Loop & Task Queues](#how-every-component-works-together)
4. [Examples](#examples)
5. [Promises & Microtasks](#microtasks--promises-deep-dive)
6. [async/await](#asyncawait)
7. [Memory Management](#storing-context-in-heap)

---

# JavaScript Engine
A JavaScript engine is simply a computer program that executes JavaScript code. It's responsible for translating human-readable JavaScript code into machine-readable instructions that the computer's hardware can execute.

## How JS engine works

- Any JS engine always contains a call stack and a heap.
- The call stack is where our code gets executed with the help of the execution context.
- And the heap is an unstructured memory pool that stores all the objects in the memory that our application needs. (Should not be confused with heap data structure. That's a completely different thing.)

<img width="600" alt="image" src="https://github.com/user-attachments/assets/0c004537-5502-4246-bda1-dd4b7193054c" />



The question is how the code gets compiled to machine code so that it can execute afterwards.

### Compilation vs Interpretation

<img width="1034" height="161" alt="image" src="https://github.com/user-attachments/assets/8a441ae9-cb4f-43af-899e-3829c750262c" />
<img width="1032" height="205" alt="image" src="https://github.com/user-attachments/assets/9a37e2cf-2ab6-49e9-b89a-f2af21cbfc12" />

- JS used to be a purely interpreted language. But since interpretation is slow, a mix of compilation and interpretation is used which is called JIT (Just-in-time) compilation.
- In JIT, "selective compilation" happens at runtime, on a demand basis. Only parts of the code that are executed frequently or are performance-critical are compiled, while less frequently executed code may remain interpreted.
- Execution typically starts with interpretation or lightweight bytecode execution for fast startup. During runtime, the engine identifies hot code paths (hotspots) and recompiles them into highly optimized machine code, allowing direct CPU execution and significantly improving performance for repeated operations.

#### Wait a minute, bytecode in JS???
- Yes, modern JavaScript engines use bytecode.
- JavaScript does not have a standardized bytecode, but modern JavaScript engines internally compile JavaScript into engine-specific bytecode before interpretation and JIT compilation.

The correct mental model: 
```
JavaScript source
   ↓
Parsing → AST
   ↓
Engine-specific bytecode
   ↓
Interpreter executes bytecode
   ↓
Hot paths → JIT → machine code
```

### JS code execution process

<img width="600" alt="image" src="https://github.com/user-attachments/assets/2a151478-1bf6-48ba-9bc4-4b8320d53256" />

#### 1. Parsing
As a piece of code enters the engine, the engine first needs to understand the structure of the code. 
- **Lexical Analysis (Tokenization)**: A Lexer or Tokenizer reads your code and breaks it down into small, meaningful units called tokens (e.g., keywords, identifiers, operators).
- Syntax Parsing: The tokens are used to build an Abstract Syntax Tree (AST), a hierarchical, tree-like representation of the code's structure. This step also catches syntax errors. The grammar is checked as the AST is being built. If a grammar rule fails, parsing stops and AST construction is aborted with a syntax error.

#### 2. Compilation & Optimization
- After the AST is built, the bytecode compiler component of the JS engine generates the engine-specific bytecode out of the AST. This bytecode is then **interpreted** by the interpreter.
- NOTE: Our JS code can run without ever being converted into machine code. Compiling the code up to bytecode is sufficient for execution.
- Why this works:
   -  The interpreter itself is a native program (written in C/C++ and already compiled into machine code), so it can execute bytecode instructions by translating them into machine-level operations internally.
   -  Think of bytecode like instructions written in a language the interpreter understands.
- Since interpretation is slow, so modern JS engines "optimize" execution through JIT compiler at runtime - which does convert bytecode into machine code.
   -  While interpreting bytecode, the engine may identify frequently executed ("hot") code paths and JIT-compile them into optimized machine code to improve performance.
   -  JIT compilation is an optimization step, not required for correctness.

```js
AST
 → Bytecode (engine-specific)
 → Interpreter executes bytecode (step-by-step)
 → Hot bytecode → JIT compiler → machine code
 → CPU executes machine code directly
```

#### 3. Execution
- Before executing any bytecode, the JavaScript engine creates an execution context.
- During execution context creation:
   - Memory is allocated for variables and functions
   - Scope (lexical environment) is established
   - Hoisting rules are applied
- The interpreter then executes the bytecode line by line using the call stack.


# Javascript Runtime
A runtime is the environment in which a programming language executes. JavaScript runtime environment is like a container, that has all the things to run a JavaScript Code.There are two types of JavaScript runtime environment:
- The runtime environment of a `Browser` (like Google Chrome).
- The `Node` runtime environment.

Every browser has it's own JS Runtime Environment. The heart of any JavaScript Runtime is always JavaScript Engine.

## JS Runtime Components
1. The JS Engine
2. Web/Global APIs
3. Callback Queue/Macrotask Queue
4. Microtask Queue
5. Event Loop

<img width="2171" height="1239" alt="image" src="https://github.com/user-attachments/assets/38032c26-02f5-4575-b53f-f72b1b1a799d" />

### 1. JS Engine
- The heart of JS Runtime.
- This component is the one that actually executes our JS code.
- It is single-threaded, so it can only do one task at a time.
- JS Engine components includes: Call stack, heap, parser, bytecode/interpreter/JIT, Garbage collector etc.
- Every browser has its own engine.
- Chrome's engine is V8, Firefox has SpiderMonkey, Safari has JavaScriptCore (Nitro).

### 2. Web APIs / Global APIs
- The host environment (browser or Node) supplies APIs (timers, network, DOM, fs, etc). These live outside the engine.
- JavaScript uses these APIs to perform tasks outside the core language capabilities.
- This enables the execution of tasks in the background, creating the illusion of a mult-threaded environment.
- These APIs, provided by the browser or the operating system, allow JavaScript to interact with external resources and perform operations asynchronously.
- Browser Environment: "Web APIs"
   -  DOM manipulation (`document`, `window`)
   - Timers (`setTimeout`, `setInterval`)
   - Network (`fetch`, `XMLHttpRequest`)
   - Storage (`localStorage`, `sessionStorage`)
- Node.js environment: "Global APIs" or "Node APIs"
   - File system (`fs`)
   - Network (`http`, `https`)
   - Operating system (`os`)
   - Process (`process`)


### 3. Macrotask Queue
- Since the async task and its callback is handed over to the Web APIs, how does the callback function associated with the operation gets placed back to JavaScript engine to continue execution? This is where callback queues comes into picture.
- Macrotask queue is a queue data structure in the JavaScript runtime environment that holds the callback functions of asynchronous operations performed by the browser.
- **Examples of Macrotasks:**
  - `setTimeout` / `setInterval`
  - `setImmediate` (Node.js)
  - I/O operations
  - UI rendering (browser)

### 4. Microtask Queue
- Microtask queue is a type of task queue that has a higher priority than the macrotask queue. All the callback functions in the microtask queue are first processed (dequeued and pushed onto the call stack) before the ones in the macrotask queue.
- JavaScript promises and the Mutation Observer API callbacks are queued in the microtask queue.
- **Examples of Microtasks:**
  - `Promise.then()` / `Promise.catch()` / `Promise.finally()`
  - `queueMicrotask()`
  - `MutationObserver` (browser)
  - `process.nextTick()` (Node.js - even higher priority)
- If microtasks keep enqueuing microtasks, macrotasks (and rendering) are starved. 

### 5. Event Loop
- A scheduler which schedules execution of callbacks from the Microtask/Macrotask Queue in the call stack.
- It continuously monitors the JS Call Stack and the callback queues. If the call stack is empty (JS is done with synchronous code), it does the following:
   - If there is any task in the microtask queue, it starts scheduling them to the JS engine one by one until all microtasks are run and microtask queue is empty.
   - Once microtask queue is empty, it starts scheduling Macrotask queue callbacks to the JS engine.

- Note: After each macrotask, the event loop checks the microtask queue again before moving to the next macrotask.
- Event Loop Priority:
   - Execute all synchronous code (call stack)
   - Process ALL microtasks (until microtask queue is empty)
   - Process ONE macrotask
   - Render (if in browser)
   - Repeat steps 2-4

## How every component works together
- JS engine starts executing JS code line by line (synchronous execution).
- **Synchronous code** is executed immediately on the call stack.
- When it encounters a code that is provided by Web API, like timer, fetch, or any other API, the engine hands over the task to the Web/Global API. The callback function associated with the task is also handed over to the Web/Global API.
- Once the task is handed over, JS continues executing the next task while the async task is being performed by the browser/node in the backgound.
- When the Web/Global API is done with the task, it enques the callback associated with it to the queue (micro/macro queue depending on the nature of the task). 
- The event loop then schedules the callbacks in the queue to be run by JS engine.
   -  **Event loop checks**:
      - Is the call stack empty?
      - If yes, process all microtasks first
      - Then process one macrotask
      - Repeat
- This is how asynchronous operation is supported by JS.
- So basically, its the host(browser/node) that takes care of the asynchrous task, while JS engine executes synchronous code.

## Key Takeaway
JavaScript itself is **synchronous and single-threaded**, but the **runtime environment** (browser/Node.js) provides APIs and mechanisms (event loop, task queues) that enable **asynchronous, non-blocking** behavior.


## Examples
### Example A - browser: microtask vs macrotask

```js
console.log('Start');

setTimeout(() => console.log('Timeout'), 0);     // macrotask
Promise.resolve().then(() => console.log('Promise')); // microtask

console.log('End');
```
Trace:

1. `Start` (sync)
2. schedule timer with host (returns immediately)
3. schedule Promise `.then` as microtask
4. `End` (sync)
5. call stack empty → event loop drains microtasks → prints `Promise`
6. event loop takes next macrotask → prints `Timeout`

Output: `Start`, `End`, `Promise`, `Timeout`

### Example B - async/await (microtask semantics)

```js
console.log('1');

async function f() {
  console.log('2');
  await null;
  console.log('3');
}
f();

console.log('4');
```
- `await null` causes the remainder of `f()` to run as a microtask (like `.then`).
- Order: 1, 2, 4, 3


### Example C - fetch / network + microtasks (browser)
```js
console.log('A');
fetch('/x').then(()=> console.log('C')); // fetch handled by host
Promise.resolve().then(()=> console.log('B'));
console.log('D');
```
Trace
1. `A`
2. start fetch (host handles network)
3. schedule Promise microtask → `.then` queued
4. `D`
5. call stack empty → drain microtasks → prints `B`
6. if/when fetch responds → host resolves promise → its `.then` becomes microtask → drained in next microtask checkpoint → prints `C`

Possible output (if fetch slow): `A`, `D`, `B`, ...later `C`

### Example D - microtask starvation
```js
Promise.resolve().then(function loop(){
  console.log('tick');
  Promise.resolve().then(loop);
});
```
This enqueues `loop` repeatedly in microtask queue. The microtask queue never empties — macrotasks and rendering are starved. Browser UI freezes. Don't do this.

### Example E - Node ordering: `process.nextTick` vs Promises vs setImmediate
```js
console.log('start');

process.nextTick(() => console.log('nextTick'));
Promise.resolve().then(() => console.log('promise'));
setImmediate(() => console.log('setImmediate'));

console.log('end');
```
Trace in Node:

1. `start` (sync)
2. schedule nextTick (nextTick queue)
3. schedule promise job (microtask queue)
4. schedule setImmediate (check phase)
5. `end` (sync)
6. call stack empty → Node runs `process.nextTick` queue → prints `nextTick`
7. then runs microtasks → prints `promise`
8. then proceeds through libuv phases; at `check` phase runs `setImmediate` → prints `setImmediate`

Output: start, end, nextTick, promise, setImmediate

- In Node, process.nextTick runs before promise microtasks and can starve the event loop; setImmediate runs in the check phase after poll.
- Long microtask chains can starve rendering and macrotasks — avoid them.


## Who enques what 

| Operation | Handled By | Queue | Notes |
|-----------|------------|-------|-------|
| `Promise.then()` | JS Engine | Microtask | Engine directly enqueues when Promise resolves |
| `queueMicrotask()` | JS Engine | Microtask | Direct microtask scheduling |
| `setTimeout()` | Browser/Node | Macrotask | Timer runs in Web API, callback enqueued after delay |
| DOM events | Browser | Macrotask | Event listeners triggered by user actions |
| `fetch()` | Browser + Engine | Microtask | Browser does network request, engine handles `.then()` |
| `process.nextTick()` | Node.js | Special Microtask | Highest priority (Node.js only) |

### 1. Promise.then()
- JS engine handles it.
- When a Promise resolves, the engine doesn't need the browser's help. It directly queues the `.then` callback into the microtask queue.
- No browser involvement needed (unless the Promise itself was created by a browser API like `fetch`).

### 2. queueMicrotask(...)
- Handled by JS engine.
- Where does the callback go? Microtask queue
- This is literally a direct command: "Put this in the microtask queue now."
- No external APIs involved.

```js
queueMicrotask(() => {
  console.log('Microtask!');
});
```

### 3. setTimeout(...) / setInterval(...)
- Who handles it? The host (browser/node)
- Where does the callback go? Macrotask queue

**Flow:**
1. JS engine sees `setTimeout(fn, 1000)`
2. Engine tells the browser: "Start a 1-second timer"
3. Browser runs the timer in the background
4. After 1 second, browser enqueues `fn` into the **macrotask queue**
5. Event loop picks it up when ready

### 4. DOM events (clicks, scroll etc)
- Who handles it? The browser
- Where does the callback go? Macrotask queue
- User interactions are monitored by the browser
- When an event occurs, the browser enqueues the registered callback into the macrotask queue

### 5. fetch(...)
- Who handles it? The browser (network) + JS Engine (Promise)
- **Queue:** Microtask (for `.then()`)

```js
fetch('/data').then(() => {
  console.log('Data received!');
});
```
- JS calls fetch() — the browser takes over.
- The browser does the network request (asynchronously, in background), not JS.
- When response comes back, the browser resolves the Promise.
- Resolving the Promise automatically triggers the engine to queue the `.then(...)` callback as a microtask.

**Key Point:** The browser does the network work, but the `.then()` callback is handled by the engine as a microtask.

## Microtasks & Promises: Deep Dive

### How Promises Work Internally

When you create a Promise:
```js
new Promise((resolve, reject) => {
  console.log("Inside executor");
  resolve("done");
}).then(result => {
  console.log("Resolved with:", result);
});
```

Step-by-step:

1. `new Promise` is called
   - JS engine creates a new Promise object
   - The executor function `(resolve, reject) => { ... }` is run immediately, synchronously, inside the JS engine.
2. `console.log("Inside executor")` runs right away
   - This is synchronous code inside the executor. 
3. `resolve("done")` is called
   - Engine changes Promise status from `"pending"` to `"fulfilled"`
   - Engine takes all stored `.then()` callbacks and schedules them into the **microtask queue**
4. **Current synchronous code finishes**
   - Event loop processes microtasks
   - `.then()` callback runs → prints `"Resolved with: done"`

     
**All of this is handled by the JS engine** — creating the Promise, running the executor, managing state, scheduling `.then()`.

---

### Promise Object Internal Structure

Conceptual model of a Promise object (stored in the heap):
```js
Promise {
  [[PromiseState]]: "pending",        // "pending" | "fulfilled" | "rejected"
  [[PromiseResult]]: undefined,       // The resolved/rejected value
  [[PromiseFulfillReactions]]: [ callback1, callback2, ... ],    // .then() callbacks
  [[PromiseRejectReactions]]: []      // .catch() callbacks
}
```
- While the Promise is still pending, JS engine needs to hold onto the callback until the Promise resolves or rejects. The callbacks of `then` and `catch` are stored in the Promise object itself. 
- When the Promise is resolved or rejected:
   - The engine updates its status
   - It schedules all stored callbacks into the microtask queue.
   - Event loop will execute them when the call stack is empty

- The Promise is handled by the JS engine because its callback is executed immediately.

### Example: setTimeout + Promise
```js
  const p = new Promise((resolve) => {
  setTimeout(() => resolve('ok'), 1000);
});

p.then((val) => {
  console.log('Resolved with:', val);
});
```
**Flow:**

1. `new Promise(...)` → Engine creates Promise (status: `"pending"`)
2. Executor runs immediately → `setTimeout` is called
3. Browser starts 1-second timer (async)
4. `.then(...)` → Callback stored in Promise's `[[PromiseFulfillReactions]]`
5. **1 second later:** Timer expires → Browser runs the callback → `resolve('ok')` is called
6. `resolve('ok')`:
   - Changes Promise status to `"fulfilled"`
   - Sets result to `"ok"`
   - Moves `.then()` callback from Promise to **microtask queue**
7. Event loop processes microtask → Prints `"Resolved with: ok"`

### SUMMARY
Here's the flow:
1. JS engine executes code in the call stack.
2. If it encounters a Promise, it executes its callback. If there are then/catch callbacks, they are basically stored inside the Promise object itself. 
3. When the callback resolves/rejects later, it triggers JS Engine to take out the then/catch callbacks from the Promise object and enque them into the MicroTask queue

## Promises & fetch(): Complete Picture

```js
console.log('1');

fetch('https://api.example.com')
  .then(() => console.log('2'));

console.log('3');
```
1. JS engine runs `console.log('1')` → prints `1`
2. JS calls `fetch()` (Synchronous):
   - JS engine gives the network request to the browser (Web API layer)
   - Browser (fetch implementation written in C++) immediately returns a Promise (status: "pending"). The Promise's executor function is handled internally by the browser's fetch implementation. Unlike `new Promise((resolve, reject) => {...})` where we write the executor, `fetch()` creates the Promise and manages its resolution internally.
   - Browser starts network request in background.
   - ```cpp
         // Pseudocode (browser's C++ implementation)
      JSPromise* fetch(const char* url) {
        // 1. Create a new Promise object in the JS engine
        JSPromise* promise = createNewPromise();
        
        // 2. Start the network request (async, in background)
        NetworkRequest* request = startNetworkRequest(url);
        
        // 3. Attach a callback for when the request completes
        request->onComplete = [promise](Response response) {
          // This callback will be invoked later when the request finishes
          resolvePromiseWithResponse(promise, response);
        };
        
        // 4. Return the Promise immediately (still pending)
        return promise;
      }
      ```
3. **`.then(() => console.log('2'))`** is executed (Synchronous):
   - Callback is stored in the Promise's `[[PromiseFulfillReactions]]`
   - **Not executed yet**
4. JS engine runs `console.log('3')` → prints `3`
5. Synchronous code done -> call stack empty.
6. Some time later... the browser gets the HTTP response:
   - Browser has a direct reference to the Promise object it created earlier. When the network request completes, browser resolves the Promise.
   - ```cpp
         // Browser's network layer (C++ pseudocode)
      void onNetworkRequestComplete(Response httpResponse) {
        // 1. Browser has the Promise object reference
        JSPromise* promise = /* the Promise from earlier */;
        
        // 2. Browser calls directly into JS engine's Promise resolution
        //    This is a DIRECT FUNCTION CALL, not a queued task!
        JSEngine::resolvePromise(promise, httpResponse);
      }

      // JS Engine's Promise resolution (C++ pseudocode)
      void JSEngine::resolvePromise(JSPromise* promise, JSValue value) {
        // 1. Update Promise state
        promise->state = "fulfilled";
        promise->result = value;
        
        // 2. Get all stored .then() callbacks
        Array<JSFunction*> reactions = promise->fulfillReactions;
        
        // 3. For each callback, schedule as microtask
        for (JSFunction* callback : reactions) {
          microtaskQueue.enqueue([callback, value]() {
            callback->call(value);  // Execute: callback(response)
          });
        }
        
        // 4. Clear the reactions
        promise->fulfillReactions.clear();
      }
      
      ```
   - The browser **directly calls** the JS engine's `resolvePromise()` function, which immediately updates the Promise state, stores the result, and schedules callbacks in the microtask queue. (Note: Both the browser and JS engine are written in C++, which allows them to communicate via direct C++ function calls. The browser has direct access to the engine's internal Promise resolution mechanism.)
   - The engine then moves the `.then()` callbacks in the microtask queue.
7. Event loop processes microtask → prints `2`

So, `fetch()` is a hybrid — handled partly by the Web API layer, and partly by the engine

## Final Mental Model

**Flow of Promise Resolution:**
```
1. Promise created → stored in heap
2. .then() called → callback stored in Promise object
3. Something resolves the Promise:
   - Browser API completes (fetch, setTimeout callback, etc.)
   - OR direct resolve() call in executor
4. JS engine is notified → moves callbacks to microtask queue
5. Event loop processes microtasks → callbacks execute
```

```js
console.log('Start');

setTimeout(() => {
  console.log('setTimeout 1');
  Promise.resolve().then(() => console.log('Promise 1'));
}, 0);

Promise.resolve().then(() => {
  console.log('Promise 2');
  setTimeout(() => console.log('setTimeout 2'), 0);
});

console.log('End');
```
```
Start
End
Promise 2
setTimeout 1
Promise 1
setTimeout 2
```

## async/await

- At its core, async/await is just syntactic sugar over Promises.
- It does not change the underlying mechanics — it just makes code easier to read and write.
- Async functions **always return a Promise**, even if you don't explicitly return one. 

```js
console.log('1');

async function fetchData() {
  console.log('2');
  await null; // the engine automatically wraps this in Promise.resolve(null) because await always works with Promises
  console.log('3');
}

fetchData();

console.log('4');
```

**Execution Flow**

| Step                                                                     | What happens                                   |
| ------------------------------------------------------------------------ | ---------------------------------------------- |
| `console.log('1')`                                                       | prints `1`                                     |
| `fetchData()` is called                                                  | enters the async function, prints `2`          |
| `await null`                                                             | this is treated like `Promise.resolve(null)`   |
| Function **pauses** here                                                 | the rest of it is scheduled as a **microtask** |
| `console.log('4')`                                                       | prints `4`                                     |
| Call stack now empty → event loop runs microtask → resumes `fetchData()` | prints `3`                                     |

**Output**
```
1
2
4
3
```


### How does the function gets "paused" and "resumed" 

#### What happens under the hood

```js
async function run() {
  console.log('A');
  await fetch('/api');
  console.log('B');
}
```
is conceptually equivalent to (though the actual engine implementation is more complex):
```js
function run() {
  console.log('A');
  fetch('/api').then(() => {
    console.log('B');
  });
}
```

**Key Points**

- The code after await becomes a callback passed to `.then()`. That's why its scheduled as a microtask - because `.then()` callbacks always are.
- The async function itself runs synchronously up to the first `await`.
   - Everything before `await` executes immediately.
   - `await` is where the function pauses. 
- At `await`, the engine:
   - Suspends/pauses the function execution.
   - Saves the execution context (local variables, position in code) in heap.
   - Registers the rest of the function as a callback.
   - That callback is stored like a `.then()` and queued as a microtask once the Promise resolves.
- Later, the engine resumes the function via event loop/microtask processing.

**Example with preserved state:**
```js
async function example() {
  const x = 10;
  console.log('Before await:', x); // 10
  
  await Promise.resolve();
  
  console.log('After await:', x);  // Still 10 - variables preserved!
}
```

### Multiple awaits
```js
async function multipleAwaits() {
  console.log('1');
  await Promise.resolve();
  console.log('2');
  await Promise.resolve();
  console.log('3');
}

multipleAwaits();
console.log('4');
```

**Output:**
```
1
4
2
3
```

**Why:**
- Synchronous code runs first: `1`, `4`
- First `await` schedules "log 2 + second await" as microtask
- Microtask runs: logs `2`, then second `await` schedules "log 3" as another microtask
- Second microtask runs: logs `3`

**Each `await` creates a new microtask boundary.**

### try/catch around await
When you use await inside a try/catch, you're telling the JavaScript engine:

> "If the Promise I'm awaiting gets rejected, treat it as if it threw an error, and let me catch it here."

Basically, this:
```js
async function fetchData() {
  try {
    const data = await fetch('/api');
    console.log('Success:', data);
  } catch (error) {
    console.log('Error caught:', error);
  }
}
```

**Conceptually equivalent to:**
```js
function fetchData() {
  return fetch('/api')
    .then((data) => {
      console.log('Success:', data);
    })
    .catch((error) => {
      console.log('Error caught:', error);
    });
}
```

#### How It Works

1. **If the Promise resolves:**
   - Execution continues after `await`
   - Code in `try` block runs normally

2. **If the Promise rejects:**
   - The rejection is converted into a thrown error
   - `catch` block catches it
   - You can handle it like any synchronous error

**Key difference:** With `await` + `try/catch`, the code **looks synchronous** and reads top-to-bottom, while `.then()/.catch()` chains can become deeply nested and harder to follow. This is the main benefit of async/await syntax.


- The engine handles the transformation, preserving the look and feel of synchronous code.


### Extra Points
1. **Async functions always return a Promise:**
   ```js
      async function example() {
        return 42;
      }
      
      // Equivalent to:
      function example() {
        return Promise.resolve(42);
      }
      
      example().then(value => console.log(value)); // 42
   ```

2. **`await` converts any value to a Promise:**
   ```js
      async function example() {
        await 42;        // → Promise.resolve(42)
        await 'hello';   // → Promise.resolve('hello')
        await null;      // → Promise.resolve(null)
        await Promise.resolve(10); // Already a Promise
      }
   ```

### Advanced Example: Understanding Execution Order
```js
console.log('1');

async function async1() {
  console.log('2');
  await async2();
  console.log('3');
}

async function async2() {
  console.log('4');
}

async1();

new Promise((resolve) => {
  console.log('5');
  resolve();
}).then(() => {
  console.log('6');
});

console.log('7');
```

**Output:**
```
1
2
4
5
7
3
6
```

**Explanation:**

1. `console.log('1')` → Prints `1` (sync)
2. `async1()` called → Prints `2` (sync)
3. `await async2()` → Enters `async2`, prints `4` (sync)
4. `await` pauses `async1`, schedules "print 3" as microtask
5. Promise executor runs (sync) → Prints `5`
6. `.then()` schedules "print 6" as microtask
7. `console.log('7')` → Prints `7` (sync)
8. Call stack empty → Event loop processes microtasks:
   - First microtask: prints `3` (from `async1`)
   - Second microtask: prints `6` (from Promise)

**Key insight:** Microtasks run in the order they were scheduled.

# Storing context in heap

## 1. Async Functions: Execution Context in Heap

The execution context is saved in Heap so that when the function resumes, the context can be loaded back from the heap and the function can then resume.

```js
async function example() {
  const x = 10;
  await Promise.resolve(); // Pause: save {x: 10} to heap
  console.log(x);          // Resume: load {x: 10} from heap
}
```

**Flow:**
```
Start → Stack has context
  ↓
await → Save context to HEAP, clear stack
  ↓
Resume → Load context from HEAP back to stack
  ↓
Complete → Heap state garbage collected
```

---

## 2. Closures: Lexical Environment in Heap

The lexical environment of the parent scope is saved in heap and not destroyed when the parent function returns.

### Example

```js
function outer() {
  const x = 10;
  const y = 20;
  
  return function inner() {
    console.log(x + y); // Needs x and y from outer
  };
}

const fn = outer(); // outer() returns, but...
fn(); // Still prints 30! How?
```

### What Happens

#### **Step 1: `outer()` Executes**

```
Call Stack:
┌─────────────────┐
│ outer()         │
│ - x = 10        │
│ - y = 20        │
└─────────────────┘
```

#### **Step 2: `outer()` Returns**

**Normally**, when a function returns:
- Its execution context is **destroyed**
- Local variables are **gone**

**But with closures:**
- Engine detects that `inner()` references `x` and `y`
- **Saves the lexical environment to the heap**
- `inner()` gets a hidden reference to this saved environment

```
Heap:
┌──────────────────────────────────┐
│ LexicalEnvironment (outer) {    │
│   x: 10,                         │
│   y: 20                          │
│ }                                │
│          ↑                       │
│          │ (reference)           │
│     ┌────┴────┐                  │
│     │ inner() │                  │
│     └─────────┘                  │
└──────────────────────────────────┘

Call Stack:
┌─────────────────┐
│ (empty)         │
└─────────────────┘
```

#### **Step 3: `fn()` is Called (Calls `inner()`)**

```
Call Stack:
┌─────────────────────────────────┐
│ inner()                         │
│ - Looks up x, y from heap       │
│ - Finds: x=10, y=20             │
│ - Prints 30                     │
└─────────────────────────────────┘

Heap:
┌──────────────────────────────────┐
│ LexicalEnvironment (outer) {    │
│   x: 10,    ← Still here!        │
│   y: 20     ← Still here!        │
│ }                                │
└──────────────────────────────────┘
```

**The lexical environment survives because:**
- It's stored in the **heap**
- `inner()` holds a reference to it
- Garbage collector **won't delete it** while `inner()` exists

---

## Side-by-Side Comparison

| Aspect | Async Functions | Closures |
|--------|----------------|----------|
| **What's saved** | Current execution context (local vars, resume point) | Parent's lexical environment (outer scope vars) |
| **Where saved** | **Heap** | **Heap** |
| **When saved** | When function pauses at `await` | When inner function is created |
| **When loaded** | When function resumes (microtask runs) | When inner function executes |
| **Why needed** | To resume execution later | To access outer scope after parent returns |
| **When GC'd** | When async function completes | When no references to inner function exist |

---

## Visual Summary

### Normal Function (No Closure, No Async)
```
function normal() {
  const x = 10;
  console.log(x);
}

Stack:         Heap:
┌────────┐     ┌────────┐
│ normal │     │ (none) │
│ x: 10  │     └────────┘
└────────┘
    ↓
Returns → Stack cleared, x destroyed ✓
```

### Closure
```
function outer() {
  const x = 10;
  return function inner() {
    console.log(x);
  };
}

Stack:              Heap:
┌────────┐          ┌─────────────────────┐
│ outer  │ ──────→  │ LexicalEnvironment  │
│ x: 10  │          │ { x: 10 }           │
└────────┘          │      ↑              │
    ↓               │      │ (reference)  │
Returns             │  ┌────────┐         │
Stack cleared       │  │ inner()│         │
BUT x survives! ✓   │  └────────┘         │
                    └─────────────────────┘
```

### Async Function
```
async function example() {
  const x = 10;
  await Promise.resolve();
  console.log(x);
}

Stack:              Heap:
┌────────┐          ┌─────────────────────┐
│example │ ──────→  │ AsyncFunctionState  │
│ x: 10  │          │ { x: 10,            │
└────────┘          │   resumePoint: ... }│
    ↓               └─────────────────────┘
await pauses                ↓
Stack cleared        Later resumed with x ✓
BUT x survives! ✓
```

---

## Both Use Heap for Same Reason

**Why heap, not stack?**

| Stack | Heap |
|-------|------|
| Destroyed when function returns | Persists until garbage collected |
| Cannot survive function exit | Can survive function exit ✓ |
| Fast but temporary | Slower but persistent ✓ |

**Both closures and async functions need:**
- Data to **survive beyond function execution**
- Ability to **access that data later**
- **Heap is the only option!**

---

## Advanced Example: Async + Closure Combined

```js
function createAsyncCounter() {
  let count = 0; // Closure variable
  
  return async function increment() {
    const localValue = count; // Local variable
    await Promise.resolve();
    count++;
    console.log(`Was ${localValue}, now ${count}`);
  };
}

const counter = createAsyncCounter();
counter(); // Was 0, now 1
counter(); // Was 1, now 2
```

**What's in heap:**
1. **Closure:** `count` variable from `createAsyncCounter`
2. **Async state:** `localValue` saved across `await`

```
Heap:
┌──────────────────────────────────────────────┐
│ LexicalEnvironment (createAsyncCounter) {   │
│   count: 2  ← Shared across all calls       │
│ }                                            │
│     ↑                                        │
│     │ (reference)                            │
│ ┌───┴──────────────────────────────┐        │
│ │ increment() function             │        │
│ └──────────────────────────────────┘        │
│                                              │
│ AsyncFunctionState (first call) {           │
│   localValue: 0  ← Saved for first call     │
│ }                                            │
│                                              │
│ AsyncFunctionState (second call) {          │
│   localValue: 1  ← Saved for second call    │
│ }                                            │
└──────────────────────────────────────────────┘
```

---

## Memory Management

### When is Heap Data Garbage Collected?

**For Closures:**
```js
function outer() {
  const x = 10;
  return function inner() {
    console.log(x);
  };
}

let fn = outer();
// Lexical environment with x=10 is in heap

fn = null;
// Now no reference to inner() exists
// → Lexical environment can be garbage collected ✓
```

**For Async Functions:**
```js
async function example() {
  const x = 10;
  await Promise.resolve();
  console.log(x);
} // Function completes here

example();
// AsyncFunctionState created in heap
// When function completes:
// → No more resume needed
// → State can be garbage collected ✓
```

---

## Key Takeaways

1. **Async functions save execution context in heap** to resume later
2. **Closures save parent lexical environment in heap** to access after parent returns
3. **Both use heap** because data must survive beyond normal function lifecycle
4. **Stack is temporary**, heap is persistent

### The Pattern

```
Need data to survive function exit?
        ↓
   Store in HEAP
        ↓
   ┌─────────────┬─────────────┐
   │             │             │
Async/await   Closures    Generators
(resume)   (outer scope)  (yield/next)
```

All three mechanisms use the heap for the same fundamental reason: **data persistence beyond function execution**.
