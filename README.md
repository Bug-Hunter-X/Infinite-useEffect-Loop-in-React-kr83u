# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency array in the `useEffect` hook. The `useEffect` hook, without a dependency array, runs after every render, leading to an infinite loop and performance degradation. The solution adds a dependency array to the `useEffect` hook to resolve this issue.

## Bug
The `bug.js` file contains the buggy code.  The `useEffect` hook logs the count to the console after every render. Because `count` changes on every click, the `useEffect` hook runs infinitely.

## Solution
The `bugSolution.js` file shows how to fix the bug. Adding `[count]` as a dependency array ensures that the `useEffect` hook only runs when the `count` value changes.