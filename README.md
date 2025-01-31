# React SetInterval Memory Leak
This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook without proper cleanup.  This can lead to memory leaks and unpredictable behavior.

## The Problem
The `setInterval` function continues to execute indefinitely unless explicitly stopped.  Without a cleanup function in `useEffect`, the interval continues even after the component unmounts, resulting in a memory leak.

## The Solution
The solution involves returning a cleanup function from `useEffect`.  This function will clear the interval when the component unmounts, preventing the memory leak.