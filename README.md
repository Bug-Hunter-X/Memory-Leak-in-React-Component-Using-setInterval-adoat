# React setInterval Memory Leak

This repository demonstrates a common memory leak in React components that use `setInterval` without proper cleanup.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The `setInterval` function, if not handled correctly, will continue to run even after the component is unmounted.  This causes memory leaks, as the interval continues to consume resources in the background.

## Solution

The solution involves using the cleanup function provided by the `useEffect` hook's return value. This cleanup function will clear the interval when the component unmounts.