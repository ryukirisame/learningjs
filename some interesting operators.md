
# Nullish Coalescing Operator (??)

The nullish coalescing operator (??) in JavaScript is a logical operator that provides a way to assign a default value when dealing with null or undefined. It returns the right-hand operand when the left-hand operand is null or undefined; otherwise, it returns the left-hand operand.

```
let result = a ?? b;
```

### How It Works:
- If a is not null or undefined, result will be a.
- If a is null or undefined, result will be b.

### Example
```
let user;
let defaultName = "Guest";

// Using the nullish coalescing operator
let name = user ?? defaultName;

console.log(name); // Output: "Guest"
```

### Comparison with the Logical OR (||) Operator

Before the nullish coalescing operator was introduced, developers often used the logical OR (||) operator for similar purposes.

However, the || operator considers any falsy value (like 0, "", false, NaN, null, and undefined) as false. This can lead to unintended results when dealing with values like "" or 0.

The nullish coalescing operator ?? is different because it only considers null and undefined as "nullish" values, allowing other falsy values like 0 or "" to pass through.


# Nullish coalescing assignment (??=)

The nullish coalescing assignment (??=) is a shorthand operator in JavaScript that allows you to assign a value to a variable only if the current value of that variable is null or undefined. This is similar to the nullish coalescing operator (??), but it directly assigns the value to the variable.

```
variable ??= value;
```

### How It Works:
- If variable is null or undefined, it assigns value to variable.
- If variable is not null or undefined, it retains its original value.





