# Infinite Rendering Bug in React

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook. The `MyComponent` renders infinitely because the effect runs after every render, causing a continuous update cycle.

## Bug

The `bug.js` file contains the buggy component. The `useEffect` hook lacks a dependency array, leading to the infinite loop.  The console will show continuous messages 'Component rendered'.

## Solution

The `bugSolution.js` file provides the solution.  Adding an empty dependency array `[]` to the `useEffect` hook ensures it only runs once after the initial render, fixing the infinite loop.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`. Observe the infinite rendering in your browser's console and potentially the browser crash.
5. View `bugSolution.js` for the corrected code.