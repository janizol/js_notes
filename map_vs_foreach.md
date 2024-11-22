
# JavaScript `map` vs `forEach`

JavaScript's **`map`** and **`forEach`** methods are both used to iterate over arrays, but they serve different purposes and have distinct features. Let's break down the differences:

---

## **Key Differences**

| Feature                        | **`map`**                                  | **`forEach`**                             |
|--------------------------------|--------------------------------------------|-------------------------------------------|
| **Return Value**               | Returns a **new array** with transformed elements. | Returns `undefined`. Does not create a new array. |
| **Purpose**                    | Used when you want to **transform** or **map** each element to a new value. | Used for **side effects** (e.g., logging, modifying external variables). |
| **Chaining**                   | Can be chained with other array methods (e.g., `.filter`, `.reduce`). | Cannot be chained directly because it returns `undefined`. |
| **Mutation**                   | Does not modify the original array.         | Does not modify the original array, but side effects can cause mutations. |
| **Performance**                | Slightly slower than `forEach` if the returned array is not used. | Faster if no new array is needed. |

---

## **When to Use `map`**
Use **`map`** when you:
1. Need to create a **new array** based on the original array.
2. Want to **transform** each element into something else.

### Example: Transforming Array Values
\`\`\`javascript
const numbers = [1, 2, 3, 4];

// Square each number using map
const squares = numbers.map(num => num * num);

console.log(squares); // Output: [1, 4, 9, 16]
console.log(numbers); // Original array remains unchanged: [1, 2, 3, 4]
\`\`\`

---

## **When to Use `forEach`**
Use **`forEach`** when you:
1. Don't need a **new array**.
2. Want to perform **side effects**, such as logging or modifying external variables.

### Example: Logging Each Element
\`\`\`javascript
const numbers = [1, 2, 3, 4];

// Log each number using forEach
numbers.forEach(num => console.log(num));

// Output:
// 1
// 2
// 3
// 4
\`\`\`

---

## **Side-By-Side Example**

Here’s an example to highlight their differences:

### Task: Add 5 to Each Element
#### Using `map`:
\`\`\`javascript
const numbers = [10, 20, 30, 40];

// Create a new array with each element increased by 5
const incremented = numbers.map(num => num + 5);

console.log(incremented); // Output: [15, 25, 35, 45]
console.log(numbers);     // Original array: [10, 20, 30, 40]
\`\`\`

#### Using `forEach`:
\`\`\`javascript
const numbers = [10, 20, 30, 40];

// Modify an external array
const incremented = [];
numbers.forEach(num => incremented.push(num + 5));

console.log(incremented); // Output: [15, 25, 35, 45]
console.log(numbers);     // Original array remains unchanged: [10, 20, 30, 40]
\`\`\`

---

## **Common Mistakes**

1. **Using `forEach` when `map` is more appropriate**:
   \`\`\`javascript
   // Inefficient and less clean
   const doubled = [];
   numbers.forEach(num => doubled.push(num * 2));
   \`\`\`

   Instead, use `map`:
   \`\`\`javascript
   const doubled = numbers.map(num => num * 2);
   \`\`\`

2. **Using `map` without utilizing the returned array**:
   \`\`\`javascript
   numbers.map(num => console.log(num)); // Misuse of map
   \`\`\`

   Instead, use `forEach`:
   \`\`\`javascript
   numbers.forEach(num => console.log(num)); // Correct use of forEach
   \`\`\`

---

## **Key Takeaway**
- Use **`map`** for **transformation** (when you need a new array).
- Use **`forEach`** for **side effects** (when you’re performing actions like logging or updating external variables).

Both are great tools, but picking the right one ensures cleaner and more efficient code. Let me know if you'd like further examples!
