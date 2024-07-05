# Initial Concepts in JavaScript

## Node.js Installation and Setup

Before diving into JavaScript, ensure you have Node.js installed. Node.js allows you to run JavaScript outside of a web browser. You can download Node.js from [here](https://nodejs.org/). Once installed, you can run JavaScript files using the `node` command in your terminal.

## Values

### Primitive Values

1. **Number**: Represents numeric values. Example:

```js

let age = 25;

```

2. **String**: Represents textual data. Strings can be defined using single quotes (`'`), double quotes (`"`), or backticks (`` ` ``). Example:

```js

let name = 'John Doe';

let greeting = `Hello, ${name}!`;

```

3. **Boolean**: Represents logical entities and can have two values: `true` or `false`. Example:

```js

let isStudent = true;

```

4. **Null**: Represents the intentional absence of any object value. Example:

```js

let emptyValue = null;

```

5. **Undefined**: Indicates that a variable has not been assigned a value. Example:

```js

let notAssigned;

```

6. **NaN (Not-a-Number)**: Represents a value that is not a valid number. Example:

```js

let result = 'a' / 2; // result is NaN

```

### Non-Primitive Values

1. **Array**: Used to store multiple values in a single variable. Example:

```js

let fruits = ['Apple', 'Banana', 'Cherry'];

console.log(fruits[0]); // Output: Apple

fruits[1] = 'Blueberry';

```

2. **Object**: Used to store collections of data and more complex entities. Example:

```js

let person = {

name: 'Alice',

age: 30

};

console.log(person.name); // Output: Alice

person.age = 31;

```

## Utility Methods

### console.log

The `console.log` method is used to output messages to the console. It is useful for debugging and displaying information.

[More info on console.log](https://developer.mozilla.org/en-US/docs/Web/API/console)

## Variable Declarations in JavaScript

### var, let, const

- `var`: Function-scoped variable declaration.

- `let`: Block-scoped variable declaration.

- `const`: Block-scoped constant declaration.

Example:

```js

var a = 10;

let b = 20;

const c = 30;

```

### Primitive vs. Non-Primitive Values

Primitive values are immutable, meaning they cannot be altered. Non-primitive values are mutable, meaning they can be modified.

### Variable Naming Rules

- Variables must begin with a letter, underscore (`_`), or dollar sign (`$`).

- Subsequent characters can be letters, digits, underscores, or dollar signs.

- JavaScript is case-sensitive.

## Loops

### for Loop

Used to iterate over arrays and strings.

```js

for (let i = 0; i < 5; i++) {

console.log(i);

}

```

### while Loop

Executes as long as the specified condition is true.

```js

let i = 0;

while (i < 5) {

console.log(i);

i++;

}

```

### for..of Loop

Used to iterate over iterable objects like arrays.

```js

let array = ['a', 'b', 'c'];

for (let item of array) {

console.log(item);

}

```

### for..in Loop

Used to iterate over the properties of an object.

```js

let object = { a: 1, b: 2, c: 3 };

for (let key in object) {

console.log(key);

}

```

## Conditionals

### if..else

Used to execute code based on a condition.

```js

if (true) {

console.log('True');

} else {

console.log('False');

}

```

### switch

Selects one of many code blocks to be executed.

```js

let color = 'red';

switch (color) {

case 'red':

console.log('Color is red');

break;

case 'blue':

console.log('Color is blue');

break;

default:

console.log('Color is unknown');

}

```

### Ternary Operator

A shorthand for if..else.

```js

let isAdult = age >= 18 ? 'Yes' : 'No';

```

## Operators

### Mathematical Operators

```js

let sum = 1 + 2; // Addition

let difference = 5 - 3; // Subtraction

let product = 2 * 3; // Multiplication

let quotient = 10 / 2; // Division

```

### Logical Operators

```js

let and = true && false; // AND

let or = true || false; // OR

let not = !true; // NOT

```

### Comparison Operators

```js

let isEqual = 1 == '1'; // Equal to (true)

let isStrictEqual = 1 === '1'; // Strict equal to (false)

let isNotEqual = 1 != 2; // Not equal to (true)

```

### Operator Precedence

Defines the order in which operators are evaluated.

[More info on operator precedence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

## Functions

### Declaring a Function

```js

function greet() {

return 'Hello';

}

```

### Parameters and Arguments

```js

function add(a, b) {

return a + b;

}

add(2, 3); // Arguments: 2 and 3

```

### Return Statement

```js

function multiply(a, b) {

return a * b;

}

```

### Calling a Function

```js

let result = multiply(2, 3);

console.log(result); // Output: 6

```

### Types of Functions

- **Function Declaration**: Defined with the `function` keyword.

- **Function Expression**: Defined with a variable.

- **Arrow Function**: Shorter syntax with the `=>` operator.

## References

- [MDN Web Docs](https://developer.mozilla.org/en-US/)

- [JavaScript Info](https://javascript.info/)

- [W3Schools JavaScript Tutorial](https://www.w3schools.com/js/)

- [Eloquent JavaScript](https://eloquentjavascript.net/)

---
