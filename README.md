# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid inputs.  Specifically, the `/users/:id` route fails to handle cases where a user with the given ID does not exist.  The `bug.js` file shows the problematic code.  The corrected code is provided in `bugSolution.js`.

## Problem

The original code attempts to access a user from a `users` array using the ID passed in the request parameter.  However, it lacks error handling for the scenario where no user with that ID is found. This can lead to errors or unexpected behavior, potentially crashing the server.

## Solution

The solution involves adding a check to verify the existence of the user before attempting to access it.  If the user is not found, a 404 Not Found status code is returned to the client.