# Unhandled Promise Rejection in Express.js

This repository demonstrates a common but easily overlooked error in Express.js applications: unhandled promise rejections.  Asynchronous operations within request handlers can fail, and without proper error handling, the entire application may crash silently.

The `bug.js` file contains the problematic code. The `bugSolution.js` file demonstrates the correct way to handle these rejections.

## Bug
The `bug.js` file showcases an Express.js server with an asynchronous operation (`someAsyncOperation`) within a route handler. This operation can either succeed or fail randomly.  If it fails, the error is unhandled, leading to a crash.

## Solution
The `bugSolution.js` file addresses this issue by properly handling potential errors using a `.catch` block within the promise chain. This ensures that errors are gracefully handled and the server remains operational.