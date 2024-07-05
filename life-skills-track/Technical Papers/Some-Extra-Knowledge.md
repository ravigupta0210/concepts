# Some Extra Knowledge:
### Using Arrays as Stacks

Stacks follow the Last-In-First-Out (LIFO) principle. In JavaScript, arrays can be used as stacks by utilizing the `push` and `pop` methods.

- **Push**: Adds an element to the end of the array.

- **Pop**: Removes the last element of the array.

```javascript

let stack = [];

stack.push(1); // [1]

stack.push(2); // [1, 2]

console.log(stack.pop()); // 2, stack is now [1]

console.log(stack); // [1]

```

### Using Arrays as Queues

Queues follow the First-In-First-Out (FIFO) principle. In JavaScript, arrays can be used as queues by utilizing the `push` and `shift` methods.

- **Push**: Adds an element to the end of the array.

- **Shift**: Removes the first element of the array.

```javascript

let queue = [];

queue.push(1); // [1]

queue.push(2); // [1, 2]

console.log(queue.shift()); // 1, queue is now [2]

console.log(queue); // [2]

```

### Truthy and Falsy Values

**Falsy values** in JavaScript are values that are considered false when encountered in a Boolean context. These values are:

- `false`

- `0`

- `-0`

- `0n` (BigInt zero)

- `""` (empty string)

- `null`

- `undefined`

- `NaN`

**Truthy values** are all values that are not falsy. They include:

- Non-zero numbers (e.g., `42`, `-42`)

- Non-empty strings (e.g., `"hello"`, `"false"`)

- Objects (e.g., `{}`, `[]`)

- Functions

### Difference between `===` and `==`

- **`===` (Strict Equality)**: Compares both the value and the type. It does not perform type coercion.

```javascript

console.log(1 === 1); // true

console.log(1 === '1'); // false

```

- **`==` (Loose Equality)**: Compares only the value, performing type coercion if necessary.

```javascript

console.log(1 == 1); // true

console.log(1 == '1'); // true

```

### Time Complexity of Sort Operation in JavaScript

The time complexity of the `sort` method in JavaScript depends on the implementation, but most modern engines use an efficient algorithm called Timsort, which has the following complexities:

- **Worst-case time complexity**: `O(n log n)`

- **Average-case time complexity**: `O(n log n)`

- **Best-case time complexity**: `O(n)`

Timsort is a hybrid sorting algorithm derived from merge sort and insertion sort, designed to perform well on many kinds of real-world data.
