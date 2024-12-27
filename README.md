# React Native useEffect Asynchronous Update Bug

This repository demonstrates a common issue in React Native where updating state within a `useEffect` hook with an asynchronous function call fails to trigger a re-render. The component's display does not update accordingly. 

The `bug.js` file contains the buggy code, showcasing the problem. The `bugSolution.js` file provides a corrected version demonstrating how to effectively update state within asynchronous operations using functional updates and ensuring the component re-renders properly.

## Problem

The initial implementation updates state asynchronously using `setTimeout`. However, React doesn't automatically re-render when state changes via an asynchronous operation without proper handling. 

## Solution

The solution utilizes a functional update within `setCount`.  The functional update receives the previous state as an argument, ensuring the update is always based on the latest state value. This guarantees correct state handling in asynchronous scenarios.