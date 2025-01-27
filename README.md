# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to the improper use of dependencies in `useEffect`. The component continuously re-renders because the effect triggers a state update that, in turn, triggers another render.

## Bug Description

The `useEffect` hook is used without specifying dependencies.  This means the effect runs after every render of the component, causing an infinite loop.  The `console.log` statement helps illustrate this by logging a message on each render. 

## Solution

The solution is to add the correct dependencies in the useEffect hook's array.  In this case, the effect only needs to run when the `count` state variable changes, so `[count]` is added as the dependencies array.