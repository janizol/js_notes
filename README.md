# Programming Paradigms Overview

Here’s a brief explanation of different programming paradigms, along with typical use cases and code examples.

---

## 1. Imperative Programming
- **Focus**: Giving the computer explicit instructions on how to perform tasks step-by-step.
- **Use Case**: Simple algorithms and scripts where precise control over each step is essential, like iterating through an array and calculating a total.

```javascript
let sum = 0;
const numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
  sum += numbers[i];
}
console.log(sum); // Outputs: 15
```

**Explanation**: Each step is explicitly defined—initializing `sum`, iterating through the array, and adding each element. Imperative programming is useful for basic tasks that require precise control.

---

## 2. Procedural Programming
- **Focus**: Structuring code into procedures or functions to handle specific tasks, making it modular and reusable.
- **Use Case**: Applications with repeated operations, like utility libraries or scripting tasks, where functions need to be reused.

```javascript
function calculateArea(width, height) {
  return width * height;
}
function calculatePerimeter(width, height) {
  return 2 * (width + height);
}

console.log(calculateArea(5, 3)); // Outputs: 15
console.log(calculatePerimeter(5, 3)); // Outputs: 16
```

**Explanation**: Functions `calculateArea` and `calculatePerimeter` handle specific tasks. Procedural programming is a good fit for organizing code into modular, reusable parts.

---

## 3. Object-Oriented Programming (OOP)
- **Focus**: Organizing code around "objects" that represent entities with attributes and methods.
- **Use Case**: Applications with complex data relationships and behaviors, like e-commerce platforms or content management systems.

```javascript
class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  login() {
    console.log(`${this.name} has logged in.`);
  }

  logout() {
    console.log(`${this.name} has logged out.`);
  }
}

const user = new User("Alice", "alice@example.com");
user.login();  // Outputs: Alice has logged in.
user.logout(); // Outputs: Alice has logged out.
```

**Explanation**: `User` is a class representing a user with `name` and `email` properties and `login` and `logout` methods. OOP is great for applications with entities that have a defined state and behavior.

---

## 4. Functional Programming
- **Focus**: Writing functions that avoid changing states or data directly and focus on pure transformations.
- **Use Case**: Data processing tasks, like filtering and transforming lists in applications that handle large data sets, as in financial software or data analytics.

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((n) => n * 2);
console.log(doubled); // Outputs: [2, 4, 6, 8, 10]
```

**Explanation**: `map` is a pure function that returns a new array without changing `numbers`. Functional programming is useful when you need predictable, testable code without side effects.

---

## 5. Declarative Programming
- **Focus**: Describing the desired result rather than defining the steps to achieve it.
- **Use Case**: User interfaces or data queries where you specify *what* you want to see rather than *how* to get it.

```javascript
// React (a declarative UI framework)
function App() {
  return (
    <div>
      <h1>Hello, world!</h1>
    </div>
  );
}
```

**Explanation**: In this React component, we declare the structure of the UI without specifying how it should render. Declarative programming is ideal for UI design, database queries, and configuration files, where we care about the end result rather than the process.

---

## 6. Event-Driven Programming
- **Focus**: Writing code that responds to events, such as user actions or data changes.
- **Use Case**: Interactive applications like web apps, games, or GUIs where actions trigger responses, such as clicking a button or receiving a network request.

```javascript
document.getElementById("myButton").addEventListener("click", () => {
  console.log("Button was clicked!");
});
```

**Explanation**: Here, the code listens for a "click" event on `myButton` and responds by logging a message. Event-driven programming is fundamental to interactive applications where user actions trigger specific responses.

---

Each paradigm offers different benefits, so the choice depends on the problem you’re solving and the structure best suited for it.

Janizol edited on 5 November for students