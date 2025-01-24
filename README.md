# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop. The component updates infinitely because the `useEffect` hook lacks a dependency array or has an incorrect dependency array causing it to re-run on every render, leading to unintended behavior.

## Bug Description
The `useEffect` hook in the `MyComponent` function has incorrect logic within its dependency array, causing it to execute on every render. This results in an infinite loop of log messages and potentially crashes the application, due to the infinite loop caused by the unintended infinite render cycle.

## Solution
The solution involves correctly specifying the dependency array within the `useEffect` hook, so that it only executes when the `count` state variable changes.