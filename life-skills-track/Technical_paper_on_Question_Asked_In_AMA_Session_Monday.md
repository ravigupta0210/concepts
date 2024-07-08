# Technical Paper: AMA Session Questions (July 6, 2024)

### 1. Difference Between `==` and `===` Operator

The `==` (equality) and `===` (strict equality) operators are used in JavaScript to compare values, but they behave differently.

- **`==` Operator**:

- Performs type coercion if the types of the two operands are different.

- Converts the operands to the same type before making the comparison.

- Example: `5 == '5'` returns `true` because the string `'5'` is coerced to the number `5`.

- **`===` Operator**:

- Does not perform type coercion.

- Returns `true` only if the operands are of the same type and have the same value.

- Example: `5 === '5'` returns `false` because the operands are of different types (number and string).

### 2. Why `console.log(typeof [])` Returns 'object'

In JavaScript, arrays are a type of object. The `typeof` operator is used to identify the type of a variable or value, and it returns a string indicating the type. When you create an array using square brackets `[]`, JavaScript treats this array as an object with additional properties and methods that are designed for working with ordered data.

The `typeof` operator returns 'object' for arrays because:

1. Arrays are objects with a special prototype that provides methods and properties specific to array operations.

2. JavaScript's type system does not have a distinct type for arrays; they are considered a specialized form of objects.

Example:

```javascript

let arr = [];

console.log(typeof arr); // Output: 'object'

```

To check if a variable is an array, you can use `Array.isArray()`:

```javascript

let arr = [];

console.log(Array.isArray(arr)); // Output: true

```

### 3. Disadvantages of Using Closures

Closures are powerful features in JavaScript, but they have some disadvantages:

- **Memory Leaks**: Closures can lead to memory leaks if they capture variables that are no longer needed, causing those variables to remain in memory.

- **Debugging Difficulty**: Debugging code that uses closures can be challenging because it may not be clear which variables are in scope.

- **Performance Overhead**: Closures can create a performance overhead if not used properly, as they may keep references to variables that would otherwise be garbage collected.

### 4. Why Using Global Variables is Bad in JavaScript

Global variables can lead to several issues:

- **Name Collisions**: Global variables can be overwritten by other scripts, leading to unexpected behavior.

- **Maintainability**: Code that relies on global variables is harder to maintain and debug because the state of global variables can be modified from anywhere in the code.

- **Testing Difficulty**: Testing code that uses global variables is more complex, as tests may need to manage the global state.

### 5. How to Extract Certain Properties from an Array of Objects

To extract certain properties from an array of objects and create a new array, you can use the `map` method. For example:

```javascript

const users = [

{ name: 'Alice', age: 25 },

{ name: 'Bob', age: 30 },

{ name: 'Charlie', age: 35 }

];

const names = users.map(user => user.name);

console.log(names); // ['Alice', 'Bob', 'Charlie']

```

### 6. Difference Between `charAt()` and `at()` Method in JavaScript

- **`charAt(index)`**:

- Returns the character at the specified index.

- Does not support negative indexing.

- Example: `'hello'.charAt(1)` returns `'e'`.

- **`at(index)`**:

- Returns the character at the specified index.

- Supports negative indexing, where `-1` refers to the last character.

- Example: `'hello'.at(-1)` returns `'o'`.

### 7. How to Reset Initial or First Commit in Git

To reset the initial or first commit in Git, you can use an interactive rebase:

```bash

git rebase -i --root

```

In the interactive rebase screen, change `pick` to `edit` for the first commit. Make the necessary changes, then amend the commit:

```bash

git commit --amend

```

Finally, continue the rebase:

```bash

git rebase --continue

```

### 8. Why Can't We Use the Dot (.) Operator in Arrays to Access Values

Even though `console.log(typeof [])` returns 'object', arrays in JavaScript are a special type of object designed for ordered data. The dot operator is used to access properties by name, but arrays use numeric indices to access elements. The bracket notation (`[]`) is used for this purpose because it allows dynamic access using variables.

### 9. Why `forEach` Loop Skips 'not defined' Values While `for` Loop Gives 'undefined'

The behavior of `forEach` and `for` loops differs when dealing with sparse arrays (arrays with missing elements).

- **`forEach` Loop**:

- The `forEach` method iterates over array elements and applies a function to each element.

- It skips unassigned (empty) elements in the array, often referred to as "holes."

- It does not execute the provided function for array indexes that have been deleted or never assigned a value.

Example:

```javascript

let arr = [1, , 3]; // Sparse array with a hole at index 1

arr.forEach(element => {

console.log(element);

});

// Output:

// 1

// 3

```

- **`for` Loop**:

- The `for` loop iterates over all indexes in the array, whether they are defined or not.

- If an element is not defined at a particular index, it will return `undefined`.

Example:

```javascript

let arr = [1, , 3]; // Sparse array with a hole at index 1

for (let i = 0; i < arr.length; i++) {

console.log(arr[i]);

}

// Output:

// 1

// undefined

// 3

```

### 10. Mimicking `Array.splice` and `Array.slice` on Objects

While arrays and objects have different structures and purposes, you can still perform similar operations to `Array.splice` and `Array.slice` on objects by manipulating their properties.

- **Mimicking `Array.splice`**:

- `Array.splice` changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

- To mimic `splice` on an object, you would need to delete or add properties.

Example of mimicking `splice`:

```javascript

let obj = {a: 1, b: 2, c: 3, d: 4};

// Mimic removing properties 'b' and 'c'

delete obj.b;

delete obj.c;

// Adding a new property

obj.e = 5;

console.log(obj);

// Output: {a: 1, d: 4, e: 5}

```

- **Mimicking `Array.slice`**:

- `Array.slice` returns a shallow copy of a portion of an array into a new array.

- To mimic `slice` on an object, you can create a new object containing a subset of the original object's properties.

Example of mimicking `slice`:

```javascript

let obj = {a: 1, b: 2, c: 3, d: 4};

// Mimic extracting properties 'a' and 'b'

let newObj = {};

newObj.a = obj.a;

newObj.b = obj.b;

console.log(newObj);

// Output: {a: 1, b: 2}

```

Using destructuring and the spread operator to mimic `slice`:

```javascript

let obj = {a: 1, b: 2, c: 3, d: 4};

// Mimic extracting properties 'a' and 'b'

let {a, b, ...rest} = obj;

let newObj = {a, b};

console.log(newObj);

// Output: {a: 1, b: 2}

```

In this approach, you can create new objects by selectively copying properties from the original object, effectively mimicking the behavior of `slice`.

### 11. What is "Callback Hell" and How to Avoid It

**Callback Hell** refers to the situation where callbacks are nested within other callbacks, leading to hard-to-read and maintainable code. It can be avoided by:

- **Using Promises**: Promises help manage asynchronous code more cleanly.

- **Async/Await**: Simplifies the syntax for using promises.

- **Modularization**: Breaking down code into smaller, reusable functions.

### 12. Explanation of Output in file1.js and file2.js Example

In the given example:

**file1.js**:

```javascript

let ar = [1, 2, 3];

console.log("Hello");

module.exports.ar = ar;

```

**file2.js**:

```javascript

const { ar } = require('./file1.js');

let print = ar;

console.log(print);

```

The `console.log("Hello")` statement in `file1.js` executes when `file1.js` is required in `file2.js`. This is because requiring a module runs its code. Therefore, "Hello" is printed before the exported value is logged in `file2.js`.
