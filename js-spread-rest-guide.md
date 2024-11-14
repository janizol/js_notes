
# Understanding JavaScript Spread and Rest Operators

## Spread Operator (`...`)

The **spread operator** is used to "spread out" elements of an **array** or **object**.

### Example: Copying an Array

```javascript
const fruits = ["🍎", "🍌", "🍇"];
const newFruits = [...fruits];
console.log(newFruits); // ["🍎", "🍌", "🍇"]
```

### Example: Merging Arrays

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
console.log([...arr1, ...arr2]); // [1, 2, 3, 4]
```

---

## Rest Operator (`...`)

The **rest operator** is used to collect multiple elements into an array.

### Example: Using Rest in Function Parameters

```javascript
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3)); // Output: 6
```

### Example: Extracting Remaining Elements

```javascript
const colors = ["red", "green", "blue"];
const [first, ...rest] = colors;
console.log(rest); // ["green", "blue"]
```
