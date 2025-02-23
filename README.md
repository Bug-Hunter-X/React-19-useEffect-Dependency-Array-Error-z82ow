# React 19 useEffect Dependency Array Bug

This repository demonstrates a common error in React 19 related to the useEffect hook and its dependency array.  Forgetting to include relevant state variables in the dependency array can lead to unexpected behavior, infinite loops, or stale closures.

## Bug Description
The `bug.js` file contains a component that increments a counter. The `useEffect` hook logs the count to the console.  However, if the `count` variable is omitted from the dependency array, the effect will run only once, and the log will not reflect subsequent changes in count value, thus creating a stale closure.

## Solution
The `bugSolution.js` file provides the corrected version. Adding `count` to the dependency array ensures the effect runs whenever the `count` value changes, providing the expected behavior.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs in the `bug.js` example and compare it to `bugSolution.js`
