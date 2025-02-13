# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrectly defined dependency array, causing an infinite re-rendering loop.

## Bug Description

The `useEffect` hook is intended to perform side effects based on changes to specific values.  If a dependency is omitted, the effect will run on every render, potentially creating an infinite loop. This example showcases this scenario where a counter variable is unintentionally omitted from the dependency array.

## How to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the infinite loop in the React component.

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array. By adding `count` to the array, the effect now runs only when the `count` value changes. 
