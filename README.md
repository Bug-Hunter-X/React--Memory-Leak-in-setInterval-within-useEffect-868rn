# React useEffect setInterval Memory Leak

This example demonstrates a common memory leak in React applications caused by the improper use of `setInterval` within the `useEffect` hook.

## Problem

The `setInterval` function, when used inside `useEffect` without proper cleanup, continues to run even after the component unmounts.  This leads to memory leaks and potential unexpected behavior.

## Solution

The solution involves using the cleanup function provided by `useEffect` to `clearInterval` when the component unmounts. This ensures that the `setInterval` is stopped and no memory leaks occur.
