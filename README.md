# Uncontrolled Re-renders in React useEffect Hook

This example demonstrates a common React bug involving the `useEffect` hook.  The `useEffect` hook, without a dependency array, runs after every render, leading to an infinite loop and significant performance problems. The console will show 'Component re-rendered' repeatedly.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server. 
4. Observe the rapid logging and potential browser slowdown.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. This ensures it only runs when specified dependencies change.