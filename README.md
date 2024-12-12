# React useEffect: Accessing State Before Initialization

This repository demonstrates a common error in React applications: accessing state variables within the `useEffect` hook before they have been initialized.  The problem arises when trying to log or use a state variable within the `useEffect`'s dependency array before the initial render has completed, resulting in `undefined` being accessed.

## Bug

The `bug.js` file contains the problematic code. The `useEffect` hook attempts to log the `count` state variable before it's been given a value, leading to an undefined value being logged to the console.

## Solution

The `bugSolution.js` file provides the corrected code.  The `useEffect` hook now correctly utilizes the state variable after it's been initialized during the component's render cycle. This is achieved by conditionally rendering or initializing within the effect's body.