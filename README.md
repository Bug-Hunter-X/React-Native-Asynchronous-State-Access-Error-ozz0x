# React Native Asynchronous State Access Error

This repository demonstrates a common error in React Native applications: attempting to access a state variable before it's been initialized due to asynchronous operations. The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides a solution.

## Problem

When fetching data asynchronously, there's a delay between the API call and the state update.  If you try to access the state variable before the update completes, you'll encounter a runtime error because the variable might still be `null` or `undefined`.

## Solution

The solution involves using optional chaining (`?.`) to safely access properties or conditional rendering to only display components once the data has been fetched.