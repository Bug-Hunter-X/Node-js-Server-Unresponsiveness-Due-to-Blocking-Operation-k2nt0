# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem
The `bug.js` example uses a `while` loop to simulate a long-running task. This blocks the event loop, preventing it from processing other requests or events.  As a result, the server appears to freeze and becomes unresponsive to new connections.

## Solution
The `bugSolution.js` file demonstrates how to solve this by using asynchronous operations. Instead of blocking the event loop, the task is performed asynchronously, allowing the event loop to continue processing other requests.