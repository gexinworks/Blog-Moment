---
title: Understanding JavaScript Closures
date: 2026-04-01
tags: [JavaScript, Engineering, Tutorial]
---

Closures are one of those concepts that every JavaScript developer uses daily — often without realizing it.

## What Is a Closure?

A closure is a function that **remembers the variables from its outer scope** even after the outer function has returned.

```javascript
function createCounter() {
  let count = 0;
  return {
    increment: () => ++count,
    decrement: () => --count,
    getCount: () => count,
  };
}

const counter = createCounter();
counter.increment(); // 1
counter.increment(); // 2
counter.getCount();  // 2
```

The inner functions `increment`, `decrement`, and `getCount` all *close over* the `count` variable. This is a closure.

## Practical Use Cases

### 1. Data Privacy

Closures create private variables — something JavaScript didn't have natively until `#private` fields:

```javascript
function createUser(name) {
  let _password = null;
  return {
    setPassword: (pw) => { _password = pw; },
    authenticate: (pw) => pw === _password,
    getName: () => name,
  };
}
```

### 2. Function Factories

```javascript
function multiply(factor) {
  return (number) => number * factor;
}

const double = multiply(2);
const triple = multiply(3);

double(5);  // 10
triple(5);  // 15
```

### 3. Event Handlers

```javascript
function setupButton(buttonId, message) {
  document.getElementById(buttonId)
    .addEventListener('click', () => {
      alert(message); // 'message' is closed over
    });
}
```

## The Classic Pitfall

The infamous loop variable problem:

```javascript
// Bug: all callbacks log 5
for (var i = 0; i < 5; i++) {
  setTimeout(() => console.log(i), 100);
}

// Fix: use let (block scoping)
for (let i = 0; i < 5; i++) {
  setTimeout(() => console.log(i), 100);
}
```

---

*Closures aren't magic — they're just functions with good memory.*
