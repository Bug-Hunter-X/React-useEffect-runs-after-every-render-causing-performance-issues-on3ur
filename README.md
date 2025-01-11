# React useEffect Runs on Every Render

This example demonstrates an issue with the React `useEffect` hook running after every render, resulting in performance problems. The `console.log` statement inside the effect clearly shows that the effect runs excessively often.  This repository shows the problematic code and its efficient solution.

## Problem
The original `MyComponent` uses `useEffect` without specifying dependencies, causing the effect to execute after every render. This is inefficient and can lead to performance degradation, especially in components with frequent updates.

## Solution
The improved code utilizes dependency array in the `useEffect` hook, limiting execution only when the `count` changes. This optimization improves performance and addresses the unnecessary rerenders.