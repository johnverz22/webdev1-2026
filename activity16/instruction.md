# Activity: Advanced JavaScript Challenges

In this activity, you will solve five challenging pure JavaScript problems. These tasks will test your understanding of object references, complex logic, algorithms, higher-order functions, and functional array methods. Test your code using your browser's Developer Console. Use the `answer.md` as template for answers.

## Task 1: Data Structures & References
**Problem:** 
Create an object representing a `library` that contains an array of `books`. Each book should be an object with `title`, `author`, and `isAvailable` (boolean) properties. 
1. Create a shallow copy of the `library` object.
2. Change the `isAvailable` status of one of the books in the **copied** library.
3. `console.log` both the original and the copied library. In a code comment, explain why the original library's book availability also changed (or didn't change) and how you would prevent this by creating a "deep copy" instead.

## Task 2: Advanced Conditional Logic (Validation)
**Problem:** 
Write a function `validatePassword(password)` that evaluates a password string based on the following rules:
- Must be at least 8 characters long.
- Must contain at least one uppercase letter.
- Must contain at least one number.
- Must not contain the word "password" (case-insensitive).

If the password meets all criteria, return `"Strong Password"`. If it fails, return a string explaining the **first** condition it failed (e.g., `"Error: Password must be at least 8 characters long."`).

## Task 3: Complex Iteration (Algorithms)
**Problem:** 
Write a function `generateFibonacci(n)` that uses a loop to generate and return an array of the first `n` numbers in the Fibonacci sequence. 
*Note:* The sequence starts with `0` and `1`, and each subsequent number is the sum of the previous two. 
For example, `generateFibonacci(7)` should return `[0, 1, 1, 2, 3, 5, 8]`.

## Task 4: Higher-Order Functions & Callbacks
**Problem:** 
Write a function `processData(dataArray, callback)` that takes an array of numbers and a callback function. The `processData` function should apply the callback to each element and return a completely new array containing the results. 
Test your function by passing in an array of numbers and an anonymous arrow function that squares each number.

## Task 5: Functional Array Methods (Map, Filter, Reduce)

**Quick Reference:**
- **`map()`**: Creates a *new array* by transforming every element in the original array. Use it when you want to change each item (e.g., converting an array of prices to discounted prices).
- **`filter()`**: Creates a *new array* with only the elements that pass a test (a condition returning `true`). Use it when you want a subset of the original array (e.g., finding all numbers greater than 10).
- **`reduce()`**: Iterates through an array and *accumulates* the values down to a single final value (like a number sum or an object). Use it when you need to calculate a total or combine elements.

**Problem:** 
You are given the following array of transaction objects:
```javascript
const transactions = [
  { type: "deposit", amount: 150 },
  { type: "withdrawal", amount: 50 },
  { type: "deposit", amount: 200 },
  { type: "withdrawal", amount: 80 }
];
```
Using **only** modern array methods (`map`, `filter`, and/or `reduce`), calculate the final total balance of the account. Deposits should increase the balance, and withdrawals should decrease it. 
*Constraint:* You are not allowed to use `for`, `for...of`, or `while` loops.
