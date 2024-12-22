# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input parameters.  Specifically, the `/users/:id` route fails to handle cases where `:id` is not a valid integer.

The `bug.js` file shows the problematic code. The `bugSolution.js` provides a corrected version with robust error handling. 

## How to Reproduce the Bug

1. Clone this repository.
2. Run `npm install` to install express.
3. Run `node bug.js`.
4. Send a GET request to `/users/abc` (or any non-numeric ID).  The server will likely crash or return an unexpected error.

## Solution

The solution involves adding proper input validation and error handling. The `bugSolution.js` demonstrates the correct implementation.