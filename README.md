# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to become unresponsive.  The `bug.js` file contains the problematic code, and `bugSolution.js` shows how to fix it using asynchronous operations.

## Bug

The server in `bug.js` simulates a long-running task that blocks the event loop. This prevents the server from responding to new requests while the task is executing.  This is a classic example of how to create a bottleneck in your Node.js application.

## Solution

The `bugSolution.js` file demonstrates the correct approach using asynchronous techniques. By using asynchronous operations, the event loop remains free to process other requests while long-running tasks are handled in the background, thereby avoiding blocking the main thread of execution.  This ensures a much more responsive and efficient application.