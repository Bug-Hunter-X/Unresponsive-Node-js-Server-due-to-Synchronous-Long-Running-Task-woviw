# Unresponsive Node.js Server: A Case Study

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `bug.js` file showcases the problem, while `bugSolution.js` provides a corrected version using asynchronous operations.

## The Problem

In `bug.js`, the request handler contains a `while` loop that keeps the CPU busy for 5 seconds.  During this time, no other requests can be processed. This blocks the event loop, leading to unresponsiveness and potential timeouts.

## The Solution

`bugSolution.js` demonstrates the correct approach using asynchronous operations. This prevents blocking the event loop and allows the server to handle multiple requests concurrently.