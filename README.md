# React useEffect Dependency Array Bug

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can result in unexpected behavior, including infinite render loops and incorrect updates.

## The Bug
The `bug.js` file contains a component with a `useEffect` hook that's missing a crucial dependency.  This causes the effect to run on every render, leading to a continuous log output of the component rendering even if the count isn't changing. 

## The Solution
The `bugSolution.js` file shows the corrected component.  By adding `count` to the dependency array, the effect only runs when the `count` state variable changes, fixing the issue. 

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the component.