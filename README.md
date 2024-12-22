# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies in the dependency array. The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` is designed to log the current `count` value to the console.  However, because `count` is not included in the dependency array, the effect runs after every render. This, coupled with the state update within the effect, creates an infinite render loop.

## Solution

The `bugSolution.js` file fixes the issue by correctly including `count` in the dependency array. This ensures that the effect only runs when the `count` value changes.