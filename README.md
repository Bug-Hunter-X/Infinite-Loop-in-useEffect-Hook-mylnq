# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The issue arises from incorrectly specifying dependencies, leading to unintended re-renders and a performance bottleneck.

## Bug Description

The `useEffect` hook is designed to perform side effects after every render. However, if the dependency array is not correctly defined, the effect may run unnecessarily, causing an infinite loop. In this example, the absence of `count` in the dependency array causes the `useEffect` to run every time the component re-renders, resulting in an infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output showing the infinite loop.

## Solution

The solution involves correctly specifying the dependencies array in the `useEffect` hook. By adding `count` to the array, the effect runs only when `count` changes, preventing the infinite loop.

## Lessons Learned

* Always carefully specify the dependencies array in `useEffect`. 
* Missing dependencies or including unnecessary ones can lead to performance problems and unexpected behavior.
* Thoroughly test your React components to catch such subtle bugs early.