
# Errors

Errors in JavaScript are **objects** that represent runtime exceptions. They are typically thrown when the JavaScript engine encounters a problem while executing the code.

An error, if not caught or handled, will **terminate the script execution** and may crash your application. Handling errors gracefully is crucial for building robust applications.


## Error Constructor

```js
new Error(message?: string)
new Error(message?: string, options?: { cause?: any })
```


###  Properties of an Error Object
An `Error` object in JavaScript typically has the following properties:

1. **name:** The name of the error (e.g., `"Error"`, `"TypeError"`). Default is `Error`.
2. **message:** A description of the error.
3. **stack:** A stack trace that shows where the error occurred.
4. **cause:** (ES2022) Represents the underlying reason for the error. You can pass another error or any other value. (if specified).

#### Example
```javascript
try {
    throw new Error("Something went wrong");
} catch (error) {
    console.log("Name:", error.name);       // "Error"
    console.log("Message:", error.message); // "Something went wrong"
    console.log("Stack:", error.stack);     // Stack trace
}
```

##  Creating and Throwing Errors
You can explicitly throw errors using the `throw` keyword:

```javascript
function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero is not allowed");
    }
    return a / b;
}

try {
    console.log(divide(10, 0));
} catch (error) {
    console.error(error.message); // "Division by zero is not allowed"
}
```

### Using the `cause` Option
The cause property is useful for error chaining, where one error causes another.

```js
const innerError = new Error("Database connection failed.");
const error = new Error("User login failed.", { cause: innerError });

console.log(error.message); // "User login failed."
console.log(error.cause);   // Error: Database connection failed.
```

##  **Built-in Error Types**

JavaScript provides several built-in error types that help categorize different error scenarios.

| Error Type       | When It Occurs                                                 |
| --------------- | ---------------------------------------------------------------- |
| `Error`          | Generic error (base class for all errors).                        |
| `SyntaxError`    | Syntax errors detected while parsing code.                        |
| `ReferenceError` | Trying to reference a variable that is not declared or initialized. |
| `TypeError`      | Trying to perform an operation on a value of the wrong type.       |
| `RangeError`     | A number is outside an allowable range.                           |
| `URIError`       | Issues with `encodeURI()` or `decodeURI()`.                        |
| `EvalError`      | Problems with the `eval()` function. (Rarely encountered)          |
| `AggregateError` | Used to wrap multiple errors (e.g., with `Promise.any()`).          |


##  **Custom Error Classes**

It’s a good practice to define custom error types for domain-specific errors. You can extend the `Error` class to create your own error types:

```javascript
class ValidationError extends Error {
    constructor(message, field) {
        super(message);
        this.name = "ValidationError";
        this.field = field;
    }
}

try {
    throw new ValidationError("Invalid username", "username");
} catch (error) {
    console.error(`${error.name}: ${error.message}`); // ValidationError: Invalid username
    console.error("Field:", error.field);              // Field: username
}
```

## ⚙️ **Error Handling Patterns**

### 1. **Try-Catch-Finally**
The most common way to handle errors is using `try`, `catch`, and `finally`.

```javascript
try {
    // Code that may throw an error
    let data = JSON.parse('{"name": "John"}');
    console.log(data.name);
} catch (error) {
    console.error("Error parsing JSON:", error.message);
} finally {
    console.log("Execution completed.");
}
```

####  **Best Practices:**
- Only wrap **critical code** that might throw errors.
- Avoid using empty catch blocks (`catch {}`) as they **suppress errors**.


### 2. **Throwing Errors in Asynchronous Code**

Handling errors with asynchronous code can be tricky, especially with **promises and async/await**.

####  **Using Promises:**
```javascript
fetch("https://api.example.com/data")
    .then(response => response.json())
    .catch(error => console.error("Fetch failed:", error.message));
```

####  **Using Async/Await:**
```javascript
async function fetchData(url) {
    try {
        const response = await fetch(url);
        if (!response.ok) throw new Error("Network response was not ok");
        const data = await response.json();
        return data;
    } catch (error) {
        console.error("Error fetching data:", error.message);
        throw error; // Re-throw the error to propagate it
    }
}
```

##  **Error Propagation**

Errors bubble up through the call stack if not caught.

#### Example:
```javascript
function level1() {
    level2();
}

function level2() {
    level3();
}

function level3() {
    throw new Error("Something broke!");
}

try {
    level1();
} catch (error) {
    console.error("Caught:", error.message); // Caught: Something broke!
}
```

---

## 🔗 **Error Chaining with the `cause` Property (ES2022)**

The `cause` property allows you to attach the underlying reason for an error.

#### Example:
```javascript
try {
    try {
        throw new Error("Original error");
    } catch (e) {
        throw new Error("Higher-level error", { cause: e });
    }
} catch (e) {
    console.error(e.message); // Higher-level error
    console.error("Cause:", e.cause.message); // Original error
}
```

##  **When to Throw vs. When to Return Null/Undefined**

- **Throwing Errors:** Use when something unexpected happens and you need to **force the caller to handle the situation**.
- **Returning Null/Undefined:** Use when the absence of a result is expected and should not interrupt the program flow.







