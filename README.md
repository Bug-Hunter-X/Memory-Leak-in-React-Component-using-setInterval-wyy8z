# React Memory Leak with setInterval

This repository demonstrates a common error in React: using `setInterval` within a `useEffect` hook without proper cleanup.  This leads to a memory leak as the interval continues to run even after the component unmounts.

The `bug.js` file contains the problematic code. The `bugSolution.js` shows the corrected version using `clearInterval` for cleanup.

## How to reproduce

1. Clone the repo.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter increasing.  The memory leak will only be apparent after several component mounts and unmounts.