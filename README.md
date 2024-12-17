# React Memory Leak: Uncontrolled setInterval in useEffect

This repository demonstrates a common React memory leak caused by improper usage of `setInterval` within a `useEffect` hook.  The provided code lacks a cleanup function to stop the interval, leading to an ever-increasing number of intervals if the component is unmounted and remounted. This can result in significant performance issues and memory exhaustion.

## Bug Description
The bug is an uncontrolled `setInterval`.  The interval isn't cleared when the component unmounts.  This causes a memory leak because the interval continues to run even after the component is no longer in the DOM.