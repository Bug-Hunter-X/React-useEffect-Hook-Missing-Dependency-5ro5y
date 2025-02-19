# React useEffect Hook Missing Dependency
This repo demonstrates a common issue in React applications involving the `useEffect` hook.  The example showcases an infinite loop caused by omitting a necessary dependency from the dependency array of `useEffect`.  The solution illustrates the correct usage of the dependency array to prevent this problem.

## Bug
The initial code has a `useEffect` hook that logs the current `count` state.  However, because `count` is not included in the dependency array, the effect runs after every render, causing an infinite loop and excessive console logging.

## Solution
The solution shows how to add `count` to the dependency array of the `useEffect` hook. Now the effect only runs when the `count` state changes, solving the infinite loop issue. The code also includes a clear explanation of why including the `count` variable in the dependency array is crucial for preventing this common mistake.