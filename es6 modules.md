# What are ES6 Modules?

**ES6 modules** (also called **ECMAScript modules** or **ESM**) are the official, standardized way to **import and export JavaScript code** between files. They were introduced in **ECMAScript 2015 (ES6)**.


### 🧩 Key Features

#### Exporting:

```js
// math.js
export const add = (a, b) => a + b;
export const multiply = (a, b) => a * b;
```

#### Importing:

```js
// main.js
import { add, multiply } from './math.js';
console.log(add(2, 3)); // 5
```

#### Default export:

```js
// logger.js
export default function log(message) {
  console.log(message);
}

// main.js
import log from './logger.js';
```

---

### Do Browsers Support ES6 Modules?

Yes, **modern browsers fully support ES6 modules**, including:

* Chrome
* Firefox
* Edge
* Safari

But there are a few important things to keep in mind when using ES modules in the browser:

### How to Use ES Modules in HTML

Use `type="module"` in your `<script>` tag:

```html
<script type="module" src="main.js"></script>
```

This enables module syntax (`import`/`export`) and has these behaviors:

* Module scripts are **deferred** (like `defer` attribute).
* They run in **strict mode**.
* Each module has its own **scope**.
* Modules are **loaded via CORS** (so use a server, not `file://`).


### Example:

**index.html**

```html
<!DOCTYPE html>
<html>
  <body>
    <script type="module" src="main.js"></script>
  </body>
</html>
```

**math.js**

```js
export function add(a, b) {
  return a + b;
}
```

**main.js**

```js
import { add } from './math.js';
console.log(add(2, 3)); // 5
```

---

### ❗ Caution:

If you're serving files locally with `file://`, browser modules might not work due to CORS restrictions. Use a local server (like `vite`, `http-server`, `live-server`, etc.).


### Static Structure
All import/export statements must be at the top level — you can’t conditionally import like this:
```js
if (condition) {
  import './some-module.js'; // ❌ SyntaxError (in ES modules)
}
```
You must use `import()` (dynamic import) instead.



## Dynamic Imports

Dynamic imports in JavaScript allow you to **import modules at runtime**, instead of at the top of your file like static imports. They're incredibly useful for **code-splitting, lazy loading, conditional loading, and on-demand logic**.

### 1. What is Dynamic Import?

Dynamic import uses the `import()` function:

```js
import('./math.js').then((module) => {
  console.log(module.add(2, 3));
});
```

Unlike static `import`, which is hoisted and must be at the top level, `import()` is:

* A **function**
* **Asynchronous**
* Returns a **Promise** that resolves to the module object

### 2. Syntax and Usage

```js
// Static import (must be at the top)
import { add } from './math.js';

// Dynamic import (can be anywhere)
const module = await import('./math.js');
module.add(2, 3);
```

Or with `.then()`:

```js
import('./math.js').then((mod) => {
  mod.add(1, 2);
});
```


#### ✅ Use Cases:

| Use Case                | Example                                          |
| ----------------------- | ------------------------------------------------ |
| **Code splitting**      | Load large modules only when needed              |
| **Conditional imports** | Import only in specific situations               |
| **Lazy-loaded routes**  | In React or Vue routing                          |
| **Plugin systems**      | Load user extensions or tools at runtime         |
| **SSR optimization**    | Avoid server-side loading of client-only modules |


### 4. Example: Conditional Import

```js
if (user.role === 'admin') {
  const adminTools = await import('./admin-tools.js');
  adminTools.showDashboard();
}
```

### 5. Error Handling

Since `import()` returns a Promise, use `try/catch`:

```js
try {
  const module = await import('./some-module.js');
  module.run();
} catch (e) {
  console.error('Failed to load module:', e);
}
```


### 6. Dynamic Path Building

You **can** build paths dynamically, but the path must still resolve at runtime.

```js
const lang = 'en';
const messages = await import(`./locales/${lang}.js`);
```

> ⚠️ Note: For bundlers like Webpack or Vite, dynamic paths may require extra configuration (e.g., [magic comments](https://webpack.js.org/api/module-methods/#magic-comments)).



### 7. `import()` vs `require()`

| Feature              | `import()`                      | `require()`         |
| -------------------- | ------------------------------- | ------------------- |
| Syntax               | ES Module                       | CommonJS            |
| Asynchronous         | ✅ (Promise-based)               | ❌ (sync)            |
| Where you can use it | Anywhere                        | Only in Node        |
| Use case             | Code-splitting, dynamic loading | Legacy Node.js code |



### 8. Top-level `await` with Dynamic Import

In ESM environments (like `<script type="module">` in browsers), you can use top-level `await`:

```js
const { add } = await import('./math.js');
console.log(add(3, 4));
```

> ⚠️ Works only in ESM — not in CommonJS scripts or older browsers.



### 9. Browser & Node Support

| Environment                    | Support                                 |
| ------------------------------ | --------------------------------------- |
| Modern Browsers                | ✅ Full support                          |
| Node.js (v13.2+)               | ✅ With `"type": "module"` or `.mjs`     |
| Bundlers (Webpack/Vite/Rollup) | ✅ Supports code splitting with import() |



### 10. Example with React Lazy Loading

```js
import React, { lazy, Suspense } from 'react';

const LazyComponent = lazy(() => import('./HeavyComponent'));

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <LazyComponent />
    </Suspense>
  );
}
```





