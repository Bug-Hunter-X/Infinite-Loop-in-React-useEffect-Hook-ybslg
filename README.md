# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The issue arises from incorrectly specifying the dependency array, leading to an infinite loop of re-renders.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file provides the corrected version.  Understanding this bug is crucial for writing efficient and stable React components.

## Bug Description

The bug is caused by omitting the `count` variable from the dependency array in the `useEffect` hook.  This causes the effect to run after every render, triggering a state update and thus another render, resulting in an infinite loop.  The browser's console will show repeated log messages.