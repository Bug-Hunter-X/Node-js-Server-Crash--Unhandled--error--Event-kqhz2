# Node.js Server Crash: Unhandled 'error' Event

This repository demonstrates a common error in Node.js servers: unhandled errors causing the server to crash.  The example shows a basic HTTP server that fails to handle potential errors, such as connection issues.  The solution implements robust error handling to prevent crashes and maintain server stability.

## Bug

The `bug.js` file contains a simple HTTP server.  However, it lacks error handling. If any error occurs during the request handling (e.g., network issues), the server will crash without providing informative logs or graceful shutdown.

## Solution

The `bugSolution.js` file demonstrates how to properly handle errors in a Node.js server using the 'error' event listener. This approach ensures that errors are logged, preventing unexpected crashes and allowing for graceful error handling, like sending an appropriate response to clients or attempting a retry.