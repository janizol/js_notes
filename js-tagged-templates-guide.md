
# Understanding JavaScript Tagged Templates

## What Are Tagged Templates?

Tagged templates allow you to **attach a function** to a **template literal** to modify the string or process it in some way.

### Example: Emphasizing Words

```javascript
function emphasize(strings, ...values) {
  return strings.reduce((result, str, i) => {
    return result + str + (values[i] ? \`**\${values[i]}**\` : '');
  }, '');
}

const name = "Alice";
const activity = "coding";
console.log(emphasize\`Hello, \${name}! You are great at \${activity}.\`);
// Output: Hello, **Alice**! You are great at **coding**.
```

**Explanation**:
- The function receives strings and placeholders separately.
- It emphasizes the placeholders by wrapping them in `**`.

---

## Use Cases
1. **Sanitizing user input** to prevent XSS attacks.
2. **Formatting strings** for localization or styling.
