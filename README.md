# React useEffect setInterval Memory Leak
This repository demonstrates a common mistake when using `setInterval` within the `useEffect` hook in React, leading to a memory leak.  The example shows the incorrect implementation and a corrected version.

## Bug Description
The `setInterval` function within the `useEffect` hook does not include a cleanup function to clear the interval when the component unmounts. This results in the interval continuing indefinitely, causing a memory leak.

## Solution
The solution involves returning a cleanup function from the `useEffect` callback, which uses `clearInterval` to stop the interval when the component unmounts. 
