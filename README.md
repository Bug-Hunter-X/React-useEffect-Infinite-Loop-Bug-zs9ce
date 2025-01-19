# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving infinite loops caused by incorrect usage of the `useEffect` hook. The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug Description

The bug stems from an improper dependency array in the `useEffect` hook.  When the `count` variable is updated within the effect, it causes the component to re-render, leading to a never-ending loop of renders and effect executions.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console.

## Solution

The solution lies in correctly specifying the dependency array within `useEffect`.  By only adding `count` to the dependency array, it will re-render only when `count` changes.