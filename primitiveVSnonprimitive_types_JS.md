
# JavaScript: Primitive and Non-Primitive Types

---

## Primitive Types in JavaScript

In JavaScript, a **primitive type** is a basic data type that represents a single value and is not an object. Primitive values are **immutable**, meaning their values cannot be changed after they are created. JavaScript has seven primitive types:

1. **String**
2. **Number**
3. **BigInt**
4. **Boolean**
5. **Undefined**
6. **Null**
7. **Symbol**

Let's go through each type:

### 1. String
- Represents text data and is enclosed in quotes: single (`'...'`), double (`"..."`), or backticks (`` `...` ``).
- Example:
  ```javascript
  const greeting = "Hello, world!";
  ```

### 2. Number
- Represents both integers and floating-point numbers.
- Example:
  ```javascript
  const age = 30;
  const price = 99.99;
  ```
- Special numeric values like `NaN` (Not-a-Number) and `Infinity` also fall under `Number`.

### 3. BigInt
- Allows you to work with integers of arbitrary precision, making it suitable for very large numbers.
- BigInt values are created by adding `n` at the end of an integer.
- Example:
  ```javascript
  const largeNumber = 123456789012345678901234567890n;
  ```

### 4. Boolean
- Represents a logical entity and can have only two values: `true` or `false`.
- Example:
  ```javascript
  const isMember = true;
  const hasPaid = false;
  ```

### 5. Undefined
- A variable that has been declared but has not been assigned a value holds the value `undefined`.
- Example:
  ```javascript
  let name;
  console.log(name); // undefined
  ```

### 6. Null
- Represents the intentional absence of any object value and is explicitly set by the developer.
- Example:
  ```javascript
  const car = null;
  ```

### 7. Symbol
- A unique and immutable value, often used as identifiers for object properties.
- Useful when you want to avoid naming conflicts in your code.
- Example:
  ```javascript
  const id = Symbol("id");
  ```

### Key Characteristics of Primitives
- **Immutability**: The actual value of a primitive cannot be changed. When you manipulate a primitive, you are creating a new value rather than altering the existing one.
- **Copy by Value**: When you assign a primitive to another variable, it copies the value itself, not a reference.

---

## Non-Primitive Types in JavaScript

In JavaScript, **non-primitive types** refer to **objects** and **arrays**, which are collections of values and do not store a single immutable value like primitive types. Non-primitives are sometimes called **reference types** because they store references to values rather than the actual values themselves.

### Types of Non-Primitive Data

1. **Object**
2. **Array**
3. **Function**

### 1. Object
- An object is a collection of key-value pairs, where each key is a string (or a `Symbol`) and each value can be any data type, including other objects or functions.
- Example:
  ```javascript
  const person = {
    name: "Alice",
    age: 30,
    greet: function() {
      console.log("Hello!");
    },
  };
  ```

### 2. Array
- An array is a special type of object used to store an ordered list of values, called elements.
- Example:
  ```javascript
  const numbers = [1, 2, 3, 4, 5];
  const names = ["Alice", "Bob", "Charlie"];
  ```

### 3. Function
- A function is a callable object that allows you to define reusable blocks of code.
- Example:
  ```javascript
  function greet(name) {
    return `Hello, ${name}!`;
  }
  ```

### Key Characteristics of Non-Primitives

- **Mutability**: Non-primitive types are mutable, meaning their contents can be modified even if the variable itself is `const`.
  ```javascript
  const person = { name: "Alice" };
  person.name = "Bob";
  ```

- **Reference-Based Storage**: When you assign or pass a non-primitive type, you are passing a reference to the location in memory where that data is stored, not a copy of the data itself.

---

## Primitive vs. Non-Primitive Side-by-Side Example

### Primitive Types: Copy by Value (Immutable)

```javascript
let age = 30;
let newAge = age; // Copy by value
newAge = 35;

console.log(age);     // Output: 30
console.log(newAge);  // Output: 35
```

### Non-Primitive Types: Copy by Reference (Mutable)

```javascript
const person = { name: "Alice", age: 30 };
const anotherPerson = person; // Copy by reference
anotherPerson.age = 35;

console.log(person);         // Output: { name: "Alice", age: 35 }
console.log(anotherPerson);  // Output: { name: "Alice", age: 35 }
```

---

In summary, **primitive types** are immutable and copied by value, while **non-primitive types** are mutable and copied by reference.
