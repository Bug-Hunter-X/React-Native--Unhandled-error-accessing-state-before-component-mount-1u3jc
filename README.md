# React Native: Accessing State Before Component Mount

This repository demonstrates a common error in React Native: attempting to access a component's state or props before it has fully mounted.  The example showcases this problem and provides a solution using useEffect for properly handling asynchronous operations.

## Problem

The `bug.js` file contains a component that tries to fetch and display data before the component's state has been initialized.  This results in an error because `this.setState` is called on an undefined state object.

## Solution

The `bugSolution.js` file provides a corrected implementation that uses the `useEffect` hook.  This ensures that the API call is made only after the component has mounted, avoiding the undefined state error.

## How to run

1. Clone the repository.
2. `npm install`
3. `npx react-native run-android` or `npx react-native run-ios`