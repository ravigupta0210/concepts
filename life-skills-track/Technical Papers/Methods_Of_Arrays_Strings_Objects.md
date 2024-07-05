# Methods of Arrays, Strings and Objects in JavaScript
### JSON

**What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. It is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999. JSON is built on two structures:

- A collection of name/value pairs (often referred to as an object, dictionary, hash table, keyed list, or associative array).

- An ordered list of values (often referred to as an array, vector, list, or sequence).

**Different methods in JSON:**

- `JSON.parse()`: Parses a JSON string and constructs the JavaScript value or object described by the string. An optional reviver function can be provided to perform a transformation on the resulting object before it is returned.

- `JSON.stringify()`: Converts a JavaScript object or value to a JSON string. An optional replacer function can be provided to perform a transformation on the object before stringifying.

**Difference between a normal object and a JSON object:**

- A normal object in JavaScript is a collection of properties and methods.

- A JSON object is a string representation of a JavaScript object that follows the JSON format.

**How to convert a normal object to a JSON object and vice versa:**

- To convert a normal object to a JSON string, use `JSON.stringify()`.

```javascript

const obj = { name: 'Alice', age: 25 };

const jsonString = JSON.stringify(obj);

console.log(jsonString); // {"name":"Alice","age":25}

```

- To convert a JSON string to a normal object, use `JSON.parse()`.

```javascript

const jsonString = '{"name":"Alice","age":25}';

const obj = JSON.parse(jsonString);

console.log(obj); // { name: 'Alice', age: 25 }

```

### Higher Order Functions

**What is a Higher Order Function?**

A higher-order function is a function that either takes one or more functions as arguments or returns a function as its result. Higher-order functions allow you to abstract over actions, not just values.

**What is a callback function?**

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

### Array Methods

- **forEach**: Executes a provided function once for each array element.

```javascript

const arr = [1, 2, 3];

arr.forEach((num) => console.log(num));

```

- **map**: Creates a new array populated with the results of calling a provided function on every element in the calling array.

```javascript

const arr = [1, 2, 3];

const newArr = arr.map((num) => num * 2);

console.log(newArr); // [2, 4, 6]

```

- **filter**: Creates a new array with all elements that pass the test implemented by the provided function.

```javascript

const arr = [1, 2, 3];

const filteredArr = arr.filter((num) => num > 1);

console.log(filteredArr); // [2, 3]

```

- **find**: Returns the value of the first element in the array that satisfies the provided testing function.

```javascript

const arr = [1, 2, 3];

const found = arr.find((num) => num > 1);

console.log(found); // 2

```

- **reduce**: Executes a reducer function (that you provide) on each element of the array, resulting in a single output value.

```javascript

const arr = [1, 2, 3];

const sum = arr.reduce((acc, num) => acc + num, 0);

console.log(sum); // 6

```

- **every**: Tests whether all elements in the array pass the test implemented by the provided function.

```javascript

const arr = [1, 2, 3];

const allGreaterThanZero = arr.every((num) => num > 0);

console.log(allGreaterThanZero); // true

```

- **some**: Tests whether at least one element in the array passes the test implemented by the provided function.

```javascript

const arr = [1, 2, 3];

const someGreaterThanTwo = arr.some((num) => num > 2);

console.log(someGreaterThanTwo); // true

```

- **splice**: Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

```javascript

const arr = [1, 2, 3];

arr.splice(1, 1, 5); // replaces 2 with 5

console.log(arr); // [1, 5, 3]

```

- **shift**: Removes the first element from an array and returns that removed element. This method changes the length of the array.

```javascript

const arr = [1, 2, 3];

const firstElement = arr.shift();

console.log(firstElement); // 1

console.log(arr); // [2, 3]

```

- **flat**: Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.

```javascript

const arr = [1, [2, [3, [4]]]];

const flatArr = arr.flat(2);

console.log(flatArr); // [1, 2, 3, [4]]

```

- **reverse**: Reverses an array in place. The first array element becomes the last, and the last array element becomes the first.

```javascript

const arr = [1, 2, 3];

arr.reverse();

console.log(arr); // [3, 2, 1]

```

- **includes**: Determines whether an array includes a certain value among its entries, returning true or false as appropriate.

```javascript

const arr = [1, 2, 3];

const includesTwo = arr.includes(2);

console.log(includesTwo); // true

```

- **unshift**: Adds one or more elements to the beginning of an array and returns the new length of the array.

```javascript

const arr = [1, 2, 3];

arr.unshift(0);

console.log(arr); // [0, 1, 2, 3]

```

### String Methods

- **toLowerCase**: Converts the entire string to lower case.

```javascript

const str = "Hello World";

console.log(str.toLowerCase()); // hello world

```

- **trim**: Removes whitespace from both ends of a string.

```javascript

const str = " Hello World ";

console.log(str.trim()); // "Hello World"

```

- **trimEnd**: Removes whitespace from the end of a string.

```javascript

const str = " Hello World ";

console.log(str.trimEnd()); // " Hello World"

```

- **trimStart**: Removes whitespace from the beginning of a string.

```javascript

const str = " Hello World ";

console.log(str.trimStart()); // "Hello World "

```

- **concat**: Combines the text of two (or more) strings and returns a new string.

```javascript

const str1 = "Hello";

const str2 = "World";

console.log(str1.concat(" ", str2)); // "Hello World"

```

- **endsWith**: Determines whether a string ends with the characters of a specified string.

```javascript

const str = "Hello World";

console.log(str.endsWith("World")); // true

```

- **includes**: Determines whether one string may be found within another string.

```javascript

const str = "Hello World";

console.log(str.includes("World")); // true

```

- **indexOf**: Returns the index within the calling String object of the first occurrence of the specified value.

```javascript

const str = "Hello World";

console.log(str.indexOf("World")); // 6

```

- **lastIndexOf**: Returns the index within the calling String object of the last occurrence of the specified value.

```javascript

const str = "Hello World World";

console.log(str.lastIndexOf("World")); // 12

```

- **padEnd**: Pads the current string with a given string (repeated, if needed) so that the resulting string reaches a given length.

```javascript

const str = "Hello";

console.log(str.padEnd(10, "!")); // "Hello!!!!!"

```

- **padStart**: Pads the current string with a given string (repeated, if needed) so that the resulting string reaches a given length.

```javascript

const str = "Hello";

console.log(str.padStart(10, "!")); // "!!!!!Hello"

```

- **repeat**: Constructs and returns a new string which contains the specified number of copies of the string on which it was called.

```javascript

const str = "Hello";

console.log(str.repeat(3)); // "HelloHelloHello"

```

**replace**: Returns a new string with some or all matches of a pattern replaced by a replacement. The pattern can be a string or a RegExp, and the replacement can be a string or a function.

```javascript

const str = "Hello World";

console.log(str.replace("World", "Universe")); // "Hello Universe"

```

**slice**: Extracts a section of a string and returns it as a new string, without modifying the original string.

```javascript

const str = "Hello World";

console.log(str.slice(6)); // "World"

console.log(str.slice(0, 5)); // "Hello"

```

**split**: Splits a string into an array of substrings based on a specified separator and returns the array.

```javascript

const str = "apple, banana, cherry";

console.log(str.split(", ")); // ["apple", "banana", "cherry"]

```

**substring**: Returns the part of the string between the start and end indexes, or to the end of the string.

```javascript

const str = "Hello World";

console.log(str.substring(6)); // "World"

console.log(str.substring(0, 5)); // "Hello"

```

### Object Methods

**Object.values**: Returns an array of the object's own enumerable property values.

```javascript

const obj = { name: 'Alice', age: 25 };

console.log(Object.values(obj)); // ["Alice", 25]

```

**Object.keys**: Returns an array of the object's own enumerable property names.

```javascript

const obj = { name: 'Alice', age: 25 };

console.log(Object.keys(obj)); // ["name", "age"]

```

**Object.entries**: Returns an array of the object's own enumerable string-keyed property [key, value] pairs.

```javascript

const obj = { name: 'Alice', age: 25 };

console.log(Object.entries(obj)); // [["name", "Alice"], ["age", 25]]

```

**Object.fromEntries**: Transform an array of key-value pairs into an object.

```javascript

const entries = [["name", "Alice"], ["age", 25]];

console.log(Object.fromEntries(entries)); // { name: "Alice", age: 25 }

```
