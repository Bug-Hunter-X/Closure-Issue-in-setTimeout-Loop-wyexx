# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The problem arises because the `setTimeout` callback function doesn't capture the value of the loop variable `i` at the time it's set, but rather captures a reference to `i`. By the time the `setTimeout` functions finally execute, the loop has already completed, and `i` is its final value (10). 

The solution demonstrates how to properly capture the value of `i` using an immediately invoked function expression (IIFE) or `let` within the loop.

## How to run

1. Clone the repository.
2. Open `bug.js` to see the buggy code and `bugSolution.js` to see the corrected version.
3. Run each file in a JavaScript environment (e.g., node.js) to see the difference in output.