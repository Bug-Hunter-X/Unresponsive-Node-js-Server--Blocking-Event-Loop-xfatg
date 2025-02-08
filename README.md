# Unresponsive Node.js Server: Blocking the Event Loop

This repository demonstrates a common Node.js issue: blocking the event loop with a long-running synchronous operation.  The server becomes unresponsive to new requests while the operation is running.

The `server.js` file contains the problematic code. The `serverSolution.js` file demonstrates how to fix it using asynchronous operations.

## How to Reproduce

1. Clone this repository.
2. Run `node server.js`.
3. Try to access the server in your browser.  You'll notice that it's very slow to respond or might not respond at all while the CPU-intensive task is running.  This is because the event loop is blocked.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop.  See the `serverSolution.js` file for an example.