# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrectly updating state within a useEffect hook's dependency array.

## Bug Description

The `bug.js` file contains a component that uses the `useEffect` hook to increment a state variable. However, the state variable is also used as a dependency in the `useEffect` hook, creating an infinite loop. Each time the state updates, the `useEffect` hook runs again, causing the state to update again, and so on.

## Solution

The `bugSolution.js` file shows the corrected code. The solution is to remove the dependency on the state variable in the `useEffect` hook. By removing the dependency, the effect runs only once after the component mounts.