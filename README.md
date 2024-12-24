# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug where the `useEffect` hook causes unnecessary re-renders. The issue stems from a missing dependency array in the `useEffect` hook, leading to the effect running on every render, rather than only when a specific dependency changes.

## Bug Description
The `MyComponent` function uses `useEffect` to log the current count to the console.  Because there's no dependency array, this runs on every render, which is inefficient and potentially problematic for complex components. The infinite loop doesn't occur here because of the simple nature of the example, but in more complex situations, this can definitely lead to issues.  

## Bug Solution
The solution involves adding the `count` variable to the dependency array. This ensures the effect only runs whenever the `count` value changes, preventing unnecessary re-renders and console logs.
