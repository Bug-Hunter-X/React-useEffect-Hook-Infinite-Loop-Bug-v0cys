# React useEffect Hook Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug occurs when the `useEffect` hook lacks a dependency array, causing it to run infinitely, leading to performance issues or application crashes.

## Bug Description

The `useEffect` hook is intended to perform side effects, such as data fetching or subscriptions, after the component renders.  When a dependency array is omitted or incorrect, the effect runs after every render, creating an infinite loop. This typically occurs when the effect updates a state variable that is also used in the effect's logic.

## Bug Solution

The solution is to provide an empty dependency array `[]` to the `useEffect` hook. This ensures that the effect runs only once after the initial render, preventing the infinite loop.  If the effect needs to run based on specific state variable changes, those variables should be included in the dependency array.

## How to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs in the browser's developer tools to see the effect's execution