# Node.js Server Hang on Long Request

This repository demonstrates a common Node.js issue: server hangs due to long-running synchronous operations blocking the event loop.  The example uses a simple `while` loop to simulate a long task, causing the server to become unresponsive to other requests.  The solution shows how to implement asynchronous programming to avoid blocking.

## How to reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Open your browser and navigate to `http://localhost:3000`. You will notice the server responds, but further requests will be delayed or ignored.
4. Examine the network tab in your browser's developer tools to see the request being processed over 5 seconds. 
5. Run `node bugSolution.js` for a fix that uses `setTimeout`.