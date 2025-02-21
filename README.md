# React useEffect Hook Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug stems from a missing dependency in the `useEffect` dependency array, leading to unexpected re-renders and, in some cases, infinite loops.

## Bug Description

The provided `MyComponent` uses `useState` to manage a counter. The `useEffect` hook logs the current count.  However, if a dependency is missing from the dependency array, the effect will run on every render, even if the dependencies haven't changed, leading to unintended consequences and potentially an infinite loop of re-renders.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs – you will see that the message "Count: " appears multiple times with each click, even though the dependency array was supposedly correctly specified.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook.  By including `count` in the dependency array, the effect runs only when the value of `count` changes.

## Learning Outcomes

This example highlights the importance of correctly specifying dependencies in the `useEffect` hook to prevent unexpected behavior and performance issues in your React applications.  Understanding dependency arrays is crucial for writing efficient and predictable React components.