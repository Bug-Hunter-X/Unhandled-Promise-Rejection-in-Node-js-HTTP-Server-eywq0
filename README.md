# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js applications involving unhandled promise rejections within asynchronous operations of an HTTP server.  The server includes an asynchronous function (`someAsyncOperation`) that randomly fails.  The bug lies in the lack of robust error handling for the promise rejection, leading to intermittent server errors and unexpected behavior.

## Bug Description
The provided `bug.js` file contains a simple HTTP server with an asynchronous operation. This operation randomly fails, simulating a real-world scenario where external dependencies or internal logic might malfunction.  The initial implementation lacks proper error handling for the rejected promise, causing the server to become unstable.

## Solution
The solution in `bugSolution.js` addresses the issue by properly handling the promise rejection using a `.catch` block.  This prevents the unhandled rejection from propagating and crashing the server.  The solution also ensures that an appropriate error response is sent to the client, enhancing the application's robustness and user experience.