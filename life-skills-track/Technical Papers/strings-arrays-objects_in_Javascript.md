# Strings, Arrays & Objects in JavaScript
### Strings in JavaScript:

1. **Representation of Strings:**

- Strings can be represented with single quotes (''), double quotes ("") or backticks (``).

2. **String Template Literals:**

- Template literals allow embedded expressions and multiline strings using backticks (`).

- Example:

```javascript

const name = 'Alice';

const greeting = `Hello, ${name}!`;

console.log(greeting); // Output: Hello, Alice!

```

3. **Iterating Over Characters:**

- You can iterate over characters in a string using a for loop or for..of loop.

- Example:

```javascript

const message = 'Hello';

for (let char of message) {

console.log(char); // Outputs each character in 'Hello' on a new line

}

```

4. **ASCII:**

- ASCII (American Standard Code for Information Interchange) represents characters using numbers.

- JavaScript provides methods to get ASCII values using `charCodeAt()` and to convert ASCII values back to characters using `String.fromCharCode()`.

### Arrays in JavaScript:

1. **Creating Arrays:**

- Arrays can be created using square brackets `[]`.

- Example:

```javascript

const numbers = [1, 2, 3, 4];

```

2. **Reading and Updating Values:**

- Access elements using index notation (`array[index]`) to read or update values.

- Example:

```javascript

const fruits = ['Apple', 'Banana', 'Cherry'];

console.log(fruits[0]); // Output: Apple

fruits[1] = 'Orange';

console.log(fruits); // Output: ['Apple', 'Orange', 'Cherry']

```

3. **Iterating Over Arrays:**

- Use for loop or for..of loop to iterate over arrays.

- Example:

```javascript

const colors = ['Red', 'Green', 'Blue'];

for (let color of colors) {

console.log(color); // Outputs each color on a new line

}

```

4. **Accessing Objects Inside Arrays:**

- Arrays can contain objects as elements. Access object properties using dot notation or array notation.

- Example:

```javascript

const students = [

{ name: 'Alice', age: 20 },

{ name: 'Bob', age: 22 }

];

console.log(students[0].name); // Output: Alice

```

5. **Passing Arrays as Parameters:**

- Arrays can be passed as parameters to functions.

- Example:

```javascript

function processArray(arr) {

// Function logic

}

const numbers = [1, 2, 3];

processArray(numbers);

```

6. **Cloning Arrays:**

- Use spread operator (`...`) for shallow copy or use methods like `Array.from()` or `slice()` for deep copy.

- Example:

```javascript

const original = [1, 2, 3];

const shallowCopy = [...original];

```

### Objects in JavaScript:

1. **Creating Objects:**

- Objects are created using curly braces `{}`.

- Example:

```javascript

const person = { name: 'Alice', age: 30 };

```

2. **Adding and Removing Keys:**

- Add or remove keys using dot notation or bracket notation.

- Example:

```javascript

person.city = 'New York'; // Adding a new key

delete person.age; // Removing a key

```

3. **Using Nested Objects:**

- Objects can contain other objects as values.

- Example:

```javascript

const employee = {

name: 'Bob',

address: {

city: 'San Francisco',

country: 'USA'

}

};

```

4. **Updating Values in Objects:**

- Update values of keys using assignment.

- Example:

```javascript

person.name = 'Alice Smith'; // Updating name

```

5. **Cloning Objects:**

- Use spread operator (`...`) for shallow copy or use `Object.assign()` for deep copy.

- Example:

```javascript

const originalObj = { a: 1, b: 2 };

const clone = { ...originalObj };

```

6. **Passing Objects as Parameters:**

- Objects can be passed as parameters to functions.

- Example:

```javascript

function processObject(obj) {

// Function logic

}

processObject(person);

```

7. **Returning Objects from Functions:**

- Functions can return objects as their return value.

- Example:

```javascript

function createPerson(name, age) {

return { name, age };

}

```

8. **Handling Nested Objects with Loops:**

- Use for..in loops to iterate over object properties, including nested objects.

- Example:

```javascript

for (let key in employee) {

if (typeof employee[key] === 'object') {

for (let nestedKey in employee[key]) {

console.log(`${nestedKey}: ${employee[key][nestedKey]}`);

}

} else {

console.log(`${key}: ${employee[key]}`);

}

}

```

9. **Handling Arrays Inside Objects:**

- Arrays inside objects are accessed similarly to standalone arrays using index notation or methods like forEach, map, etc.

- Example:

```javascript

const company = {

name: 'ABC Inc.',

employees: ['Alice', 'Bob', 'Charlie']

};

console.log(company.employees[0]); // Output: Alice

```

### Practice Example:

- Try creating, updating, iterating over strings, arrays, and objects using the above concepts. Use console.log() to verify your results and understand the behavior of different operations.
